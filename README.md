# AMD AIE-ML GEMM Accelerator

This repository contains my AMD Versal AIE-ML accelerator exploration conducted as part of the HAI-25 Edge AI project.

The work focuses on mapping vector-search style matrix multiplication workloads onto AMD AI Engine hardware using MLIR-AIE and XRT.

## Highlights

- Tiled GEMM implementation on AMD Versal AIE-ML
- XRT host runtime orchestration
- DMA/FIFO streaming pipeline design
- Memory-layout reconstruction and verification
- Performance benchmarking and throughput analysis

## Technologies

- C++
- MLIR-AIE
- XRT
- AMD Versal AIE-ML
- DMA / FIFO Streaming

## Performance

Workload Configuration:
- GEMM (128 × 128 × 10240)
- Tile Size: 32 × 64 × 64
- AIE Grid: 4 × 4

Results:
- Peak Throughput: 675.1 GFLOPS
- Peak Efficiency: 66% of theoretical AIE2 peak
- Best Latency: 497 µs
- Typical Throughput: 500–600 GFLOPS
- Typical Latency: 550–700 µs

Highlights:
- Up to ~100× speedup over CPU baseline
- Stable DMA-streamed execution on AMD Versal AIE-ML

## Attribution

This repository contains only the AMD AIE-ML portion of the broader HAI-25 Edge AI project and does not include the Qualcomm QIDK or CPU baseline implementations developed by other team members.
