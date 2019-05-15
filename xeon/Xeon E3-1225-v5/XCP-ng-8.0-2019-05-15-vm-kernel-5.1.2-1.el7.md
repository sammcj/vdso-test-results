# Host

- Virtual
- Host Intel(R) Xeon(R) CPU E3-1225 v5 @ 3.30GHz
- Host Dell T30, 32GiB RAM, shared NFS SR
- All host XCP-ng updates installed as of 15/05/2019
- VM PVHVM running on XCP-ng 8.0
- VM 4 vCPU
- VM Kernel 5.1.2-1.el7
- VM 4GB Memory provisioned
- VM OS CentOS 7, All updates as of 15/05/2019

# vdsotest-all

```
clock-gettime-monotonic: syscall: 817 nsec/call
clock-gettime-monotonic:    libc: 837 nsec/call
clock-gettime-monotonic:    vdso: 822 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic: syscall: 775 nsec/call
clock-getres-monotonic:    libc: 772 nsec/call
clock-getres-monotonic:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-coarse: syscall: 782 nsec/call
clock-gettime-monotonic-coarse:    libc: 3 nsec/call
clock-gettime-monotonic-coarse:    vdso: 3 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-coarse: syscall: 780 nsec/call
clock-getres-monotonic-coarse:    libc: 775 nsec/call
clock-getres-monotonic-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-raw: syscall: 825 nsec/call
clock-gettime-monotonic-raw:    libc: 828 nsec/call
clock-gettime-monotonic-raw:    vdso: 828 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-raw: syscall: 802 nsec/call
clock-getres-monotonic-raw:    libc: 791 nsec/call
clock-getres-monotonic-raw:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-tai: syscall: 805 nsec/call
clock-gettime-tai:    libc: 816 nsec/call
clock-gettime-tai:    vdso: 809 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-tai: syscall: 776 nsec/call
clock-getres-tai:    libc: 776 nsec/call
clock-getres-tai:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-boottime: syscall: 807 nsec/call
clock-gettime-boottime:    libc: 833 nsec/call
clock-gettime-boottime:    vdso: 814 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-boottime: syscall: 782 nsec/call
clock-getres-boottime:    libc: 789 nsec/call
clock-getres-boottime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime: syscall: 806 nsec/call
clock-gettime-realtime:    libc: 818 nsec/call
clock-gettime-realtime:    vdso: 824 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime: syscall: 794 nsec/call
clock-getres-realtime:    libc: 789 nsec/call
clock-getres-realtime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime-coarse: syscall: 787 nsec/call
clock-gettime-realtime-coarse:    libc: 3 nsec/call
clock-gettime-realtime-coarse:    vdso: 3 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime-coarse: syscall: 786 nsec/call
clock-getres-realtime-coarse:    libc: 774 nsec/call
clock-getres-realtime-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
getcpu: syscall: 723 nsec/call
getcpu:    libc: 12 nsec/call
getcpu:    vdso: 11 nsec/call
gettimeofday: syscall: 815 nsec/call
gettimeofday:    libc: 802 nsec/call
gettimeofday:    vdso: 804 nsec/call
```


# `/proc/cpuinfo`

```
processor	: 1
vendor_id	: GenuineIntel
cpu family	: 6
model		: 94
model name	: Intel(R) Xeon(R) CPU E3-1225 v5 @ 3.30GHz
stepping	: 3
microcode	: 0xc6
cpu MHz		: 3312.373
cache size	: 8192 KB
physical id	: 2
siblings	: 1
core id		: 0
cpu cores	: 1
apicid		: 2
initial apicid	: 2
fpu		: yes
fpu_exception	: yes
cpuid level	: 13
wp		: yes
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush acpi mmx fxsr sse sse2 ss syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch cpuid_fault invpcid_single pti ssbd ibrs ibpb stibp fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx rdseed adx smap clflushopt xsaveopt xsavec xgetbv1 xsaves flush_l1d
bugs		: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf mds
bogomips	: 6655.64
clflush size	: 64
cache_alignment	: 64
address sizes	: 39 bits physical, 48 bits virtual
power management:
```