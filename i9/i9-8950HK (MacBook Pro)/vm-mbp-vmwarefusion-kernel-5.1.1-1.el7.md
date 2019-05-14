# Host

- Virtual
- Host MacBook Pro 15,1
- Host Intel(R) i9-8950HK
- Host MacOS 10.14.5 (18F132)
- VM Running on VMWare Fusion 11.0.2
- VM 6 vCPU
- VM Kernel 5.1.1-1.el7
- VM 8GB Memory provisioned, SWAP only VRAM (unused)
- VM OS CentOS 7, All updates as of 14/05/2019
- **Note: Host Laptop Powered But Charging at 50% - CPU not at full speed**

# vdsotest-all

```
clock-gettime-monotonic: syscall: 223 nsec/call
clock-gettime-monotonic:    libc: 13 nsec/call
clock-gettime-monotonic:    vdso: 12 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic: syscall: 201 nsec/call
clock-getres-monotonic:    libc: 199 nsec/call
clock-getres-monotonic:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-coarse: syscall: 204 nsec/call
clock-gettime-monotonic-coarse:    libc: 3 nsec/call
clock-gettime-monotonic-coarse:    vdso: 2 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-coarse: syscall: 200 nsec/call
clock-getres-monotonic-coarse:    libc: 199 nsec/call
clock-getres-monotonic-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-raw: syscall: 224 nsec/call
clock-gettime-monotonic-raw:    libc: 229 nsec/call
clock-gettime-monotonic-raw:    vdso: 226 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-raw: syscall: 200 nsec/call
clock-getres-monotonic-raw:    libc: 199 nsec/call
clock-getres-monotonic-raw:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-tai: syscall: 228 nsec/call
clock-gettime-tai:    libc: 13 nsec/call
clock-gettime-tai:    vdso: 12 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-tai: syscall: 204 nsec/call
clock-getres-tai:    libc: 199 nsec/call
clock-getres-tai:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-boottime: syscall: 228 nsec/call
clock-gettime-boottime:    libc: 231 nsec/call
clock-gettime-boottime:    vdso: 228 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-boottime: syscall: 201 nsec/call
clock-getres-boottime:    libc: 198 nsec/call
clock-getres-boottime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime: syscall: 248 nsec/call
clock-gettime-realtime:    libc: 14 nsec/call
clock-gettime-realtime:    vdso: 13 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime: syscall: 202 nsec/call
clock-getres-realtime:    libc: 207 nsec/call
clock-getres-realtime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime-coarse: syscall: 199 nsec/call
clock-gettime-realtime-coarse:    libc: 3 nsec/call
clock-gettime-realtime-coarse:    vdso: 2 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime-coarse: syscall: 200 nsec/call
clock-getres-realtime-coarse:    libc: 198 nsec/call
clock-getres-realtime-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
getcpu: syscall: 185 nsec/call
getcpu:    libc: 8 nsec/call
getcpu:    vdso: 7 nsec/call
gettimeofday: syscall: 218 nsec/call
gettimeofday:    libc: 13 nsec/call
gettimeofday:    vdso: 13 nsec/call
```

# `/proc/cpuinfo`

```
processor	: 5
vendor_id	: GenuineIntel
cpu family	: 6
model		: 158
model name	: Intel(R) Core(TM) i9-8950HK CPU @ 2.90GHz
stepping	: 10
microcode	: 0xb4
cpu MHz		: 2903.845
cache size	: 12288 KB
physical id	: 1
siblings	: 3
core id		: 2
cpu cores	: 3
apicid		: 6
initial apicid	: 6
fpu		: yes
fpu_exception	: yes
cpuid level	: 22
wp		: yes
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon nopl xtopology tsc_reliable nonstop_tsc cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch cpuid_fault invpcid_single pti ssbd ibrs ibpb stibp fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 invpcid rtm mpx rdseed adx smap clflushopt xsaveopt xsavec xsaves arat flush_l1d arch_capabilities
bugs		: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf
bogomips	: 5807.69
clflush size	: 64
cache_alignment	: 64
address sizes	: 43 bits physical, 48 bits virtual
power management:
```