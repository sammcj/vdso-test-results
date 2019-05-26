# Host

- CentOS 7 (ISO build 1810) install on physical server
- Host Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz
- Host HPE BL460 Gen9, 256GB DDR4 ECC, Latest Firmware as of 14/05/2019
- All CentOS updates installed as of 21/05/2019
- CPU 14 cores + hyperthreading enabled
- Kernel 5.1.3-1 (standard current stable el-repo kernel-ml)
- No VMs / other applications running (fresh install, CentOS updates installed, Kernel updated, rebooted)
- /sys/devices/system/clocksource/clocksource0/current_clocksource = tsc

# vdsotest-all

```
clock-gettime-monotonic: syscall: 290 nsec/call
clock-gettime-monotonic:    libc: 16 nsec/call
clock-gettime-monotonic:    vdso: 15 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic: syscall: 272 nsec/call
clock-getres-monotonic:    libc: 271 nsec/call
clock-getres-monotonic:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-coarse: syscall: 270 nsec/call
clock-gettime-monotonic-coarse:    libc: 4 nsec/call
clock-gettime-monotonic-coarse:    vdso: 3 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-coarse: syscall: 275 nsec/call
clock-getres-monotonic-coarse:    libc: 273 nsec/call
clock-getres-monotonic-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-monotonic-raw: syscall: 291 nsec/call
clock-gettime-monotonic-raw:    libc: 295 nsec/call
clock-gettime-monotonic-raw:    vdso: 295 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-monotonic-raw: syscall: 273 nsec/call
clock-getres-monotonic-raw:    libc: 272 nsec/call
clock-getres-monotonic-raw:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-tai: syscall: 287 nsec/call
clock-gettime-tai:    libc: 296 nsec/call
clock-gettime-tai:    vdso: 295 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-tai: syscall: 274 nsec/call
clock-getres-tai:    libc: 271 nsec/call
clock-getres-tai:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-boottime: syscall: 292 nsec/call
clock-gettime-boottime:    libc: 298 nsec/call
clock-gettime-boottime:    vdso: 296 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-boottime: syscall: 273 nsec/call
clock-getres-boottime:    libc: 272 nsec/call
clock-getres-boottime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime: syscall: 291 nsec/call
clock-gettime-realtime:    libc: 16 nsec/call
clock-gettime-realtime:    vdso: 15 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime: syscall: 272 nsec/call
clock-getres-realtime:    libc: 271 nsec/call
clock-getres-realtime:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
clock-gettime-realtime-coarse: syscall: 269 nsec/call
clock-gettime-realtime-coarse:    libc: 5 nsec/call
clock-gettime-realtime-coarse:    vdso: 4 nsec/call
Note: vDSO version of clock_getres not found
clock-getres-realtime-coarse: syscall: 273 nsec/call
clock-getres-realtime-coarse:    libc: 272 nsec/call
clock-getres-realtime-coarse:    vdso: not tested
Note: vDSO version of clock_getres not found
Note: vDSO version of clock_getres not found
getcpu: syscall: 230 nsec/call
getcpu:    libc: 11 nsec/call
getcpu:    vdso: 14 nsec/call
gettimeofday: syscall: 281 nsec/call
gettimeofday:    libc: 15 nsec/call
gettimeofday:    vdso: 15 nsec/call
```

# `/proc/cpuinfo`

```
processor : 55
vendor_id : GenuineIntel
cpu family  : 6
model   : 79
model name  : Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz
stepping  : 1
microcode : 0xb00002e
cpu MHz   : 1200.000
cache size  : 35840 KB
physical id : 1
siblings  : 28
core id   : 14
cpu cores : 14
apicid    : 61
initial apicid  : 61
fpu   : yes
fpu_exception : yes
cpuid level : 20
wp    : yes
flags   : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc aperfmperf eagerfpu pni pclmulqdq dtes64 monitor ds_cpl vmx smx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid dca sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch epb cat_l3 cdp_l3 intel_ppin intel_pt ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm cqm rdt_a rdseed adx smap xsaveopt cqm_llc cqm_occup_llc cqm_mbm_total cqm_mbm_local dtherm ida arat pln pts spec_ctrl intel_stibp flush_l1d
bogomips  : 5204.32
clflush size  : 64
cache_alignment : 64
address sizes : 46 bits physical, 48 bits virtual
power management:

```
