# Host

- Virtual
- Host Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz
- Host HPE BL460 Gen9, 256GB DDR4 ECC, Latest Firmware as of 14/05/2019
- All host XCP-ng updates installed as of 14/05/2019
- VM PVHVM running on XCP-ng 7.6
- VM 16 vCPU
- VM Kernel 5.1.1-1.el7
- VM 8GB Memory provisioned, SWAP only VRAM (unused)
- VM OS CentOS 7, All updates as of 14/05/2019
- /sys/devices/system/clocksource/clocksource0/current_clocksource = tsc

# vdsotest-all

```
clock-gettime-monotonic: syscall: 458 nsec/call
clock-gettime-monotonic:    libc: 40 nsec/call
clock-gettime-monotonic:    vdso: 26 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic: syscall: 289 nsec/call
clock-getres-monotonic:    libc: 481 nsec/call
clock-getres-monotonic:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-coarse: syscall: 290 nsec/call
clock-gettime-monotonic-coarse:    libc: 6 nsec/call
clock-gettime-monotonic-coarse:    vdso: 5 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-coarse: syscall: 261 nsec/call
clock-getres-monotonic-coarse:    libc: 398 nsec/call
clock-getres-monotonic-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-raw: syscall: 375 nsec/call
clock-gettime-monotonic-raw:    libc: 324 nsec/call
clock-gettime-monotonic-raw:    vdso: 475 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-raw: syscall: 534 nsec/call
clock-getres-monotonic-raw:    libc: 434 nsec/call
clock-getres-monotonic-raw:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-tai: syscall: 403 nsec/call
clock-gettime-tai:    libc: 30 nsec/call
clock-gettime-tai:    vdso: 34 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-tai: syscall: 265 nsec/call
clock-getres-tai:    libc: 381 nsec/call
clock-getres-tai:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-boottime: syscall: 330 nsec/call
clock-gettime-boottime:    libc: 498 nsec/call
clock-gettime-boottime:    vdso: 595 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-boottime: syscall: 361 nsec/call
clock-getres-boottime:    libc: 451 nsec/call
clock-getres-boottime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime: syscall: 438 nsec/call
clock-gettime-realtime:    libc: 32 nsec/call
clock-gettime-realtime:    vdso: 37 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime: syscall: 284 nsec/call
clock-getres-realtime:    libc: 300 nsec/call
clock-getres-realtime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime-coarse: syscall: 257 nsec/call
clock-gettime-realtime-coarse:    libc: 7 nsec/call
clock-gettime-realtime-coarse:    vdso: 6 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime-coarse: syscall: 325 nsec/call
clock-getres-realtime-coarse:    libc: 450 nsec/call
clock-getres-realtime-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
getcpu: syscall: 320 nsec/call
getcpu:    libc: 18 nsec/call
getcpu:    vdso: 16 nsec/call
gettimeofday: syscall: 505 nsec/call
gettimeofday:    libc: 35 nsec/call
gettimeofday:    vdso: 35 nsec/call
```

# `/proc/cpuinfo`

```
processor	: 0
vendor_id	: GenuineIntel
cpu family	: 6
model		: 79
model name	: Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz
stepping	: 1
microcode	: 0xb00002e
cpu MHz		: 2601.508
cache size	: 35840 KB
physical id	: 0
siblings	: 8
core id		: 0
cpu cores	: 8
apicid		: 0
initial apicid	: 0
fpu		: yes
fpu_exception	: yes
cpuid level	: 13
wp		: yes
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush acpi mmx fxsr sse sse2 ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm cpuid_fault invpcid_single pti intel_ppin ssbd ibrs ibpb stibp fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid xsaveopt flush_l1d
bugs		: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf
bogomips	: 5203.09
clflush size	: 64
cache_alignment	: 64
address sizes	: 46 bits physical, 48 bits virtual
power management:

```
