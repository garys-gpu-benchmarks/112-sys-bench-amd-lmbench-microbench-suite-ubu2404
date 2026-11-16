# Results: 112 lmbench Microbench Suite

**Main goal:** Measure a fixed lmbench OS microbenchmark subset  
**Tools:** Run lmbench lat_syscall (null, read), lat_ctx, lat_mem_rd 16 128, bw_mem 512m rd, and bw_pipe

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_142 · recorded 2026-11-16). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-16T11:09:11Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:10 · benchmark 00:44 · whole run 01:04
- **Source:** run 112_20261116_110911
- **Command:** `bash run_benchmark.sh --smoke --warmup-duration-us 1000 --repetitions 1`

| # | Metric | Result |
|---|---|---|
| 1 | Null syscall latency, us (lat_syscall_null_us) | 0.1077 |
| 2 | Context-switch latency, us (context_switch_latency_us) | 3.96 |
| 3 | 16 MB stride-128 sequential-read latency, cache- and prefetch-assisted, ns (lat_mem_rd_16mb_stride128_ns) | 7.042 |
| 4 | Single-thread memory read bandwidth, MB/s (bw_mem_mb_s) | 14702.75 |
| 5 | Inter-process pipe bandwidth, MB/s (bw_pipe_mb_s) | 3578.66 |
<!-- /profile:smoke -->
