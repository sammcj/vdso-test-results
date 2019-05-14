# Host

- Virtual
- Host Intel(R) Xeon(R) CPU E5-2660 0 @ 2.20GHz
- Host HPE BL460 Gen8, 192GB DDR3 ECC, Latest Firmware as of 14/05/2019
- All host XCP-ng updates installed as of 14/05/2019
- VM PVHVM running on XCP-ng 7.6
- VM 16 vCPU
- VM Kernel 5.1.1-1.el7
- VM 8GB Memory provisioned, SWAP only VRAM (unused)
- VM OS CentOS 7, All updates as of 14/05/2019

# vdsotest-all

```
clock-gettime-monotonic: syscall: 633 nsec/call
clock-gettime-monotonic:    libc: 35 nsec/call
clock-gettime-monotonic:    vdso: 35 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic: syscall: 610 nsec/call
clock-getres-monotonic:    libc: 590 nsec/call
clock-getres-monotonic:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-coarse: syscall: 541 nsec/call
clock-gettime-monotonic-coarse:    libc: 13 nsec/call
clock-gettime-monotonic-coarse:    vdso: 9 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-coarse: syscall: 537 nsec/call
clock-getres-monotonic-coarse:    libc: 551 nsec/call
clock-getres-monotonic-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-raw: syscall: 695 nsec/call
clock-gettime-monotonic-raw:    libc: 768 nsec/call
clock-gettime-monotonic-raw:    vdso: 851 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-raw: syscall: 518 nsec/call
clock-getres-monotonic-raw:    libc: 561 nsec/call
clock-getres-monotonic-raw:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-tai: syscall: 612 nsec/call
clock-gettime-tai:    libc: 35 nsec/call
clock-gettime-tai:    vdso: 33 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-tai: syscall: 548 nsec/call
clock-getres-tai:    libc: 547 nsec/call
clock-getres-tai:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-boottime: syscall: 736 nsec/call
clock-gettime-boottime:    libc: 723 nsec/call
clock-gettime-boottime:    vdso: 750 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-boottime: syscall: 566 nsec/call
clock-getres-boottime:    libc: 589 nsec/call
clock-getres-boottime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime: syscall: 883 nsec/call
clock-gettime-realtime:    libc: 38 nsec/call
clock-gettime-realtime:    vdso: 42 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime: syscall: 523 nsec/call
clock-getres-realtime:    libc: 608 nsec/call
clock-getres-realtime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime-coarse: syscall: 557 nsec/call
clock-gettime-realtime-coarse:    libc: 13 nsec/call
clock-gettime-realtime-coarse:    vdso: 10 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime-coarse: syscall: 638 nsec/call
clock-getres-realtime-coarse:    libc: 551 nsec/call
clock-getres-realtime-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
getcpu: syscall: 485 nsec/call
getcpu:    libc: 27 nsec/call
getcpu:    vdso: 22 nsec/call
gettimeofday: syscall: 650 nsec/call
gettimeofday:    libc: 30 nsec/call
gettimeofday:    vdso: 35 nsec/call
```

# `/proc/cpuinfo`

```
processor	: 15
vendor_id	: GenuineIntel
cpu family	: 6
model		: 45
model name	: Intel(R) Xeon(R) CPU E5-2660 0 @ 2.20GHz
stepping	: 7
microcode	: 0x714
cpu MHz		: 2200.018
cache size	: 20480 KB
physical id	: 1
siblings	: 8
core id		: 14
cpu cores	: 8
apicid		: 30
initial apicid	: 30
fpu		: yes
fpu_exception	: yes
cpuid level	: 13
wp		: yes
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush acpi mmx fxsr sse sse2 ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl cpuid pni pclmulqdq ssse3 cx16 pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx hypervisor lahf_lm cpuid_fault pti ssbd ibrs ibpb stibp xsaveopt flush_l1d
bugs		: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf
bogomips	: 4478.15
clflush size	: 64
cache_alignment	: 64
address sizes	: 46 bits physical, 48 bits virtual
power management:

```