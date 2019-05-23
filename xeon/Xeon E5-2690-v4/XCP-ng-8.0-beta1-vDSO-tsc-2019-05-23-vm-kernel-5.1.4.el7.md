# Host

- Virtual
- Host Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz
- Host HPE BL460 Gen9, 256GB DDR4 ECC, Latest Firmware as of 23/05/2019
- All host XCP-ng updates installed as of 23/05/2019
- VM PVHVM running on XCP-ng 8.0 Beta 1
- VM 16 vCPU
- VM Kernel 5.1.4-1.el7
- VM 8GB Memory provisioned, SWAP only VRAM (unused)
- VM OS CentOS 7, All updates as of 23/05/2019
- No VMs / other applications running (fresh install, CentOS updates installed, Kernel updated, rebooted)
- vDSO and tsc clocksource enabled on host: `/opt/xensource/libexec/xen-cmdline --set-xen clocksource=tsc && /opt/xensource/libexec/xen-cmdline --set-xen tsc=stable:socket` (and reboot)
- VM clocksource set to tsc: `echo tsc > /sys/devices/system/clocksource/clocksource0/current_clocksource`

Note: The above two xen-cmdline set's the clocksource to tsc allowing for vDSO which is available as of Xen 4.8, XCP-ng 8.0 ships with 4.11 (7.6 shipped with 4.7).

# vdsotest-all

```
clock-gettime-monotonic: syscall: 487 nsec/call
clock-gettime-monotonic:    libc: 19 nsec/call
clock-gettime-monotonic:    vdso: 18 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic: syscall: 461 nsec/call
clock-getres-monotonic:    libc: 624 nsec/call
clock-getres-monotonic:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-coarse: syscall: 450 nsec/call
clock-gettime-monotonic-coarse:    libc: 4 nsec/call
clock-gettime-monotonic-coarse:    vdso: 5 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-coarse: syscall: 450 nsec/call
clock-getres-monotonic-coarse:    libc: 453 nsec/call
clock-getres-monotonic-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-raw: syscall: 504 nsec/call
clock-gettime-monotonic-raw:    libc: 507 nsec/call
clock-gettime-monotonic-raw:    vdso: 649 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-raw: syscall: 441 nsec/call
clock-getres-monotonic-raw:    libc: 571 nsec/call
clock-getres-monotonic-raw:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-tai: syscall: 485 nsec/call
clock-gettime-tai:    libc: 18 nsec/call
clock-gettime-tai:    vdso: 18 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-tai: syscall: 451 nsec/call
clock-getres-tai:    libc: 667 nsec/call
clock-getres-tai:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-boottime: syscall: 489 nsec/call
clock-gettime-boottime:    libc: 493 nsec/call
clock-gettime-boottime:    vdso: 727 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-boottime: syscall: 439 nsec/call
clock-getres-boottime:    libc: 634 nsec/call
clock-getres-boottime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime: syscall: 484 nsec/call
clock-gettime-realtime:    libc: 19 nsec/call
clock-gettime-realtime:    vdso: 17 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime: syscall: 443 nsec/call
clock-getres-realtime:    libc: 618 nsec/call
clock-getres-realtime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime-coarse: syscall: 444 nsec/call
clock-gettime-realtime-coarse:    libc: 4 nsec/call
clock-gettime-realtime-coarse:    vdso: 5 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime-coarse: syscall: 450 nsec/call
clock-getres-realtime-coarse:    libc: 606 nsec/call
clock-getres-realtime-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
getcpu: syscall: 445 nsec/call
getcpu:    libc: 11 nsec/call
getcpu:    vdso: 13 nsec/call
gettimeofday: syscall: 471 nsec/call
gettimeofday:    libc: 20 nsec/call
gettimeofday:    vdso: 26 nsec/call
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
cpu MHz   : 2596.955
cache size  : 35840 KB
physical id : 1
siblings  : 8
core id   : 14
cpu cores : 8
apicid    : 30
initial apicid  : 30
fpu   : yes
fpu_exception : yes
cpuid level : 13
wp    : yes
flags   : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush acpi mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch cpuid_fault invpcid_single pti intel_ppin ssbd ibrs ibpb stibp fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear flush_l1d
bugs    : cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf mds
bogomips  : 5273.03
clflush size  : 64
cache_alignment : 64
address sizes : 46 bits physical, 48 bits virtual
power management:

```
