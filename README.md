# vdso-test-results

Results of running vDSO tests on various hosts

- Thanks to [@nlynch-mentor](https://github.com/nlynch-mentor) for [vdsotest](https://github.com/nlynch-mentor/vdsotest.git)

Tests can be found [under the various CPU types in this repo](https://github.com/sammcj/vdso-test-results).

## Why care about vDSO performance?

If vDSO isn’t working as intended / effectively then fixing that could have HUGE performance gains on highly multithreaded applications.

This started with me trying to get to the bottom of why Puppet Enterprise Master / Server runs so poorly on Xen VMs, Puppet thinks that vDSO isn’t being properly utilised.
However vDSO was added to Xen quite a while ago, so getting some comparisons will prove useful.

## Install and Testing

_Note on testing Xen / XenServer / XCP-ng physical hosts:_ You can't do this on the dom0 as it _is_ a VM with Xen, you can easily do so by booting from a OS on an ISO image such as [CentOS 7.6](https://www.centos.org/download/) or [Fedora](https://getfedora.org/en/workstation/download/) (Because it has a newer Kernel much like those provided by Kernel-ML / ELRepo).


1. Install pre-reqs

_Note: Assumes [kernel-ml](https://elrepo.org/tiki/kernel-ml) is installed from [elrepo](https://elrepo.org/tiki/tiki-index.php)_ on CentOS 7.

```
yum clean all
yum update -y; grub2-mkconfig -o /boot/grub2/grub.cfg
yum install -y automake make libtool gcc autogen git
reboot now
```

2. Clone and build [vdsotest](https://github.com/nlynch-mentor/vdsotest.git)

```
mkdir git
cd git
git clone --depth=1 https://github.com/nlynch-mentor/vdsotest.git
cd vdsotest
./autogen.sh && ./configure && make -j 4 && make install
```

3. Run all tests

```
./vdsotest-all
```

4. Record CPU info

```
cat /proc/cpuinfo
```

## vDSO and Timekeeping Information and Links

- https://en.wikipedia.org/wiki/VDSO
- https://lwn.net/Articles/615809/
- http://man7.org/linux/man-pages/man7/vdso.7.html
- https://www.linuxjournal.com/content/creating-vdso-colonels-other-chicken
- https://github.com/torvalds/linux/blob/v4.19/Documentation/virtual/kvm/timekeeping.txt
- http://oliveryang.net/2015/09/pitfalls-of-TSC-usage/ (Note: Dated)

### Xen Specific

- https://xenproject.org/2016/12/07/whats-new-with-xen-project-hypervisor-4-8/ (See PVCLOCK_TSC_STABLE_BIT)
- https://lkml.org/lkml/2017/11/8/627
- https://blog.packagecloud.io/eng/2017/03/08/system-calls-are-much-slower-on-ec2/
- http://xenbits.xen.org/docs/4.2-testing/misc/tscmode.txt
