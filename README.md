# CUDA Aerial Image Processing

## Project Description

This project analyzes aerial images using CUDA-based GPU acceleration. It performs multiple image processing tasks—such as converting images to grayscale, applying Gaussian blur, detecting edges with the Sobel operator, and enhancing image quality—by leveraging custom CUDA kernels for efficient parallel computation on NVIDIA GPUs.

## Steps to Run
To run this, you must have access to an NVIDIA GPU and CUDA toolkit. Clone this repository and build:

```bash
git clone https://github.com/AkshatBhatt4/CUDAatScaleForTheEnterpriseCourseProject
cd CUDAatScaleForTheEnterpriseCourseProject
mkdir build && cd build
cmake ..
cmake --build . --config Release
```

## Run the Pipeline

```bash
.\bin\Release\cuda_image_processor.exe -i ..\aerials -o ..\output -m all
```

## Process Specific Mode

```bash
./bin/cuda_image_processor -i ../aerials -o ../output -m edge
./bin/cuda_image_processor -i ../aerials -o ../output -m blur
./bin/cuda_image_processor -i ../aerials -o ../output -m grayscale
```

## Code Organization
- `aerials/` This folder holds the USC-SIPI aerial image dataset (38 TIFF images).
- `execution/` Contains sample execution log for proof of execution.
- `Output/` Contains the Output files.
- `src/` The source code for this project.
- `CMakeLists.txt` CMake build configuration for this project.
- `README.md` The description of the project.
- `run.sh` Convenience script for running the pipeline (Linux/macOS).