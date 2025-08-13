# GPUZIP: A Checkpointing Optimization Library for Adjoint-Mode Applications

This repository contains the MSc dissertation by Thiago Maltempi titled "GPUZIP: A checkpointing optimization library for adjoint-mode applications," completed at the Institute of Computing, UNICAMP, Brazil.

## Abstract

Adjoint-mode applications, such as seismic Reverse Time Migration (RTM), require significant computational resources, particularly when running on GPUs. The checkpoint-recompute trade-off is a critical aspect of these applications, where optimizing the storage and retrieval of intermediate states during computation can significantly improve performance.

GPUZIP addresses this challenge by combining two key techniques:

1. **Prefetching**: Proactively schedules asynchronous data transfers from host memory to GPU memory, reducing wait times.
2. **Compression**: Applies lossy compression techniques (cuZFP, NVIDIA Bitcomp) to reduce the data transfer volume.

Together, these approaches substantially accelerate checkpointing operations in GPU-based adjoint computations, with demonstrated speedups of up to 8.9× in real-world seismic imaging applications.

## Key Features

- Compatible with multiple checkpointing algorithms (Revolve, zCut, Uniform)
- NVIDIA CUDA-based implementation for GPU acceleration
- Asynchronous prefetching mechanism to hide data transfer latency
- Integration with lossy compression libraries
- Application-specific optimizations for seismic RTM workflows

## Contents

This repository includes:

- Full dissertation text in LaTeX format (`ic-tese-v3.tex`)
- Final PDF version (`output/Thiago_Maltempi__Dissertação_Mestrado__FINALFINALFINAL.pdf`)
- Defense Presentation PDF and PPT version (Portuguese only) (`output/PRESENTATION__ThiagoMaltempi__Defesa__Mestrado.pdf`, `output/PRESENTATION__ThiagoMaltempi__Defesa__Mestrado.pptx`)
- Bibliography (`ic-tese-v3.bib`)
- Figures and diagrams illustrating the architecture and results

## Key Findings

- The prefetching mechanism alone achieves up to 1.7× speedup in checkpoint retrieval
- Compression techniques alone achieve up to 5.4× speedup
- The combined GPUZIP approach achieves up to 8.9× speedup in overall application performance
- Minimal impact on result quality when using carefully tuned lossy compression parameters

## Publications

This research has been presented in several venues:

- Maltempi, T., Rigo, S., Pereira, M., Yviquel, H., Leite, G., Lee, O., Costa, J., & Araujo, G. (2025). Checkpointing fine-tuning for accelerating seismic applications in GPUs. The International Journal of High Performance Computing Applications. [DOI: 10.1177/10943420251340794](https://doi.org/10.1177/10943420251340794)

- Maltempi, T., Rigo, S., Pereira, M., Yviquel, H., Costa, J., & Araujo, G. (2024). [Euro-Par Conference Publication]

- Maltempi, T., Rigo, S., Pereira, M., Yviquel, H., Costa, J., Souza, A., & Araujo, G. (2023). Introducing Prefetching and Data Compression to Accelerate Checkpointing for Inverse Seismic Problems. [Poster presented at Super Computing 2023 (SC'23)](https://sc23.supercomputing.org/proceedings/tech_poster/poster_files/rpost129s3-file2.pdf)

## Citation

```bibtex
@article{ijhpca,
  author = {Thiago Maltempi and Sandro Rigo and Marcio Pereira and Hervé Yviquel and Gustavo Leite and Orlando Lee and Jessé Costa and Guido Araujo},
  title = {Checkpointing fine-tuning for accelerating seismic applications in GPUs},
  journal = {The International Journal of High Performance Computing Applications},
  year = {2025},
  doi = {10.1177/10943420251340794},
  URL = {https://doi.org/10.1177/10943420251340794}
}
```
