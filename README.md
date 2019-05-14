# vdso-test-results

Results of running vDSO tests on various hosts

- Thanks to [@nlynch-mentor](https://github.com/nlynch-mentor) for [vdsotest](https://github.com/nlynch-mentor/vdsotest.git)

Tests can be found [under the various CPU types in this repo](https://github.com/sammcj/vdso-test-results).

## Why care about vDSO?

If vDSO isn’t working as intended / effectively then fixing that could have HUGE performance gains on highly multithreaded applications.

This started with me trying to get to the bottom of why Puppet Enterprise Master / Server runs so poorly on Xen VMs, Puppet thinks that vDSO isn’t being properly utilised.
However vDSO was added to Xen quite a while ago, so getting some comparisons will prove useful.

## Test Method

1. Install pre-reqs

_Note: Assumes [kernel-ml](https://elrepo.org/tiki/kernel-ml) is installed from [elrepo](https://elrepo.org/tiki/tiki-index.php)_.

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
./vdsotest-all.sh
```

4. Record CPU info

```
cat /proc/cpuinfo
```

## vDSO Information and Links

- https://en.wikipedia.org/wiki/VDSO
- https://lwn.net/Articles/615809/
- http://man7.org/linux/man-pages/man7/vdso.7.html

### Xen Specific

- https://xenproject.org/2016/12/07/whats-new-with-xen-project-hypervisor-4-8/ (See PVCLOCK_TSC_STABLE_BIT)
- https://lkml.org/lkml/2017/11/8/627
