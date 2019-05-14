# Host

- Physical
- Intel i7-4790K
- Kernel 5.1.1-1.el7
- 16GB DDR3 1600 Kingston
- Gigabyte Z97MX-Gaming Motherboard, BIOS F6
- OS CentOS 7, All updates as of 14/05/2019

# vdsotest-all

```
clock-gettime-monotonic: syscall: 183 nsec/call
clock-gettime-monotonic:    libc: 13 nsec/call
clock-gettime-monotonic:    vdso: 12 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic: syscall: 163 nsec/call
clock-getres-monotonic:    libc: 163 nsec/call
clock-getres-monotonic:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-coarse: syscall: 166 nsec/call
clock-gettime-monotonic-coarse:    libc: 3 nsec/call
clock-gettime-monotonic-coarse:    vdso: 3 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-coarse: syscall: 166 nsec/call
clock-getres-monotonic-coarse:    libc: 165 nsec/call
clock-getres-monotonic-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-raw: syscall: 183 nsec/call
clock-gettime-monotonic-raw:    libc: 187 nsec/call
clock-gettime-monotonic-raw:    vdso: 183 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-raw: syscall: 162 nsec/call
clock-getres-monotonic-raw:    libc: 163 nsec/call
clock-getres-monotonic-raw:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-tai: syscall: 184 nsec/call
clock-gettime-tai:    libc: 13 nsec/call
clock-gettime-tai:    vdso: 12 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-tai: syscall: 164 nsec/call
clock-getres-tai:    libc: 163 nsec/call
clock-getres-tai:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-boottime: syscall: 186 nsec/call
clock-gettime-boottime:    libc: 190 nsec/call
clock-gettime-boottime:    vdso: 187 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-boottime: syscall: 163 nsec/call
clock-getres-boottime:    libc: 163 nsec/call
clock-getres-boottime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime: syscall: 180 nsec/call
clock-gettime-realtime:    libc: 13 nsec/call
clock-gettime-realtime:    vdso: 12 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime: syscall: 163 nsec/call
clock-getres-realtime:    libc: 162 nsec/call
clock-getres-realtime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime-coarse: syscall: 166 nsec/call
clock-gettime-realtime-coarse:    libc: 3 nsec/call
clock-gettime-realtime-coarse:    vdso: 3 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime-coarse: syscall: 164 nsec/call
clock-getres-realtime-coarse:    libc: 164 nsec/call
clock-getres-realtime-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
getcpu: syscall: 149 nsec/call
getcpu:    libc: 9 nsec/call
getcpu:    vdso: 8 nsec/call
gettimeofday: syscall: 170 nsec/call
gettimeofday:    libc: 14 nsec/call
gettimeofday:    vdso: 14 nsec/call
```

# `/proc/cpuinfo`

```
processor	: 7
vendor_id	: GenuineIntel
cpu family	: 6
model		: 60
model name	: Intel(R) Core(TM) i7-4790K CPU @ 4.00GHz
stepping	: 3
microcode	: 0x1c
cpu MHz		: 4371.871
cache size	: 8192 KB
physical id	: 0
siblings	: 8
core id		: 3
cpu cores	: 4
apicid		: 7
initial apicid	: 7
fpu		: yes
fpu_exception	: yes
cpuid level	: 13
wp		: yes
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand lahf_lm abm cpuid_fault invpcid_single pti tpr_shadow vnmi flexpriority ept vpid ept_ad fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid xsaveopt dtherm ida arat pln pts
bugs		: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf
bogomips	: 8000.57
clflush size	: 64
cache_alignment	: 64
address sizes	: 39 bits physical, 48 bits virtual
power management:
```