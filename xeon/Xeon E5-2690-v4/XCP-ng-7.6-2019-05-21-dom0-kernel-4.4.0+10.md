# Host

- XCP-ng 7.6 dom0
- Host Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz
- Host HPE BL460 Gen9, 256GB DDR4 ECC, Latest Firmware as of 14/05/2019
- All host XCP-ng updates installed as of 21/05/2019
- dom0 16 CPU (standard XCP-ng dom0)
- dom0 Kernel 4.4.0+10 (standard XCP-ng dom0)
- dom0 4GB Memory (standard XCP-ng dom0)
- No VMs / other domains running (fresh install, xcp-ng updates installed, rebooted)

# vdsotest-all

```
clock-gettime-monotonic: syscall: 1509 nsec/call
clock-gettime-monotonic:    libc: 16 nsec/call
clock-gettime-monotonic:    vdso: 22 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic: syscall: 1477 nsec/call
clock-getres-monotonic:    libc: 1488 nsec/call
clock-getres-monotonic:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-coarse: syscall: 1498 nsec/call
clock-gettime-monotonic-coarse:    libc: 6 nsec/call
clock-gettime-monotonic-coarse:    vdso: 6 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-coarse: syscall: 1496 nsec/call
clock-getres-monotonic-coarse:    libc: 2268 nsec/call
clock-getres-monotonic-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-raw: syscall: 1508 nsec/call
clock-gettime-monotonic-raw:    libc: 1524 nsec/call
clock-gettime-monotonic-raw:    vdso: 2174 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-raw: syscall: 1511 nsec/call
clock-getres-monotonic-raw:    libc: 1994 nsec/call
clock-getres-monotonic-raw:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-tai: syscall: 1496 nsec/call
clock-gettime-tai:    libc: 1780 nsec/call
clock-gettime-tai:    vdso: 2233 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-tai: syscall: 1492 nsec/call
clock-getres-tai:    libc: 2122 nsec/call
clock-getres-tai:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-boottime: syscall: 1509 nsec/call
clock-gettime-boottime:    libc: 1529 nsec/call
clock-gettime-boottime:    vdso: 2061 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-boottime: syscall: 1477 nsec/call
clock-getres-boottime:    libc: 1923 nsec/call
clock-getres-boottime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime: syscall: 1497 nsec/call
clock-gettime-realtime:    libc: 16 nsec/call
clock-gettime-realtime:    vdso: 22 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime: syscall: 1485 nsec/call
clock-getres-realtime:    libc: 1934 nsec/call
clock-getres-realtime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime-coarse: syscall: 1493 nsec/call
clock-gettime-realtime-coarse:    libc: 5 nsec/call
clock-gettime-realtime-coarse:    vdso: 7 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime-coarse: syscall: 1496 nsec/call
clock-getres-realtime-coarse:    libc: 1967 nsec/call
clock-getres-realtime-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
getcpu: syscall: 1486 nsec/call
getcpu:    libc: 11 nsec/call
getcpu:    vdso: 15 nsec/call
gettimeofday: syscall: 1507 nsec/call
gettimeofday:    libc: 15 nsec/call
gettimeofday:    vdso: 21 nsec/call
```

# `/proc/cpuinfo`

```
processor : 15
vendor_id : GenuineIntel
cpu family  : 6
model   : 79
model name  : Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz
stepping  : 1
microcode : 0xb000036
cpu MHz   : 2597.006
cache size  : 35840 KB
physical id : 0
siblings  : 16
core id   : 8
cpu cores : 8
apicid    : 17
initial apicid  : 17
fpu   : yes
fpu_exception : yes
cpuid level : 20
wp    : yes
flags   : fpu de tsc msr pae mce cx8 apic sep mca cmov pat clflush acpi mmx fxsr sse sse2 ht syscall nx lm constant_tsc arch_perfmon rep_good nopl nonstop_tsc eagerfpu pni pclmulqdq monitor est ssse3 fma cx16 sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch ida arat epb pln pts dtherm fsgsbase bmi1 hle avx2 bmi2 erms rtm rdseed adx xsaveopt cqm_llc cqm_occup_llc
bugs    : l1tf
bogomips  : 5194.01
clflush size  : 64
cache_alignment : 64
address sizes : 46 bits physical, 48 bits virtual
power management:

```
