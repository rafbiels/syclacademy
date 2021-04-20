# SYCL Academy

![SYCL Academy](sycl_academy.png "SYCL Academy")

This repository provides materials that can be used for teaching SYCL 1.2.1. The
materials are provided using the "Creative Commons Attribution Share Alike 4.0
International" license.

## What is SYCL?

If you're not familiar with SYCL or would like some further resources for
learning about SYCL below are a list of useful resources:

*  Read a description of SYCL on the [Khronos website SYCL page](https://www.khronos.org/sycl/).
*  Go to the Khronos website to find [a list of SYCL resources](https://www.khronos.org/sycl/resources).
*  Check out the [SYCL 1.2.1 reference guide](https://www.khronos.org/files/sycl/sycl-12-reference-card.pdf).
*  Browse SYCL news, blog posts, videos, projects and more on the [sycl.tech community website](https://sycl.tech/)
*  Get a list of the [available SYCL implementations](https://sycl.tech/#get-sycl)

### How to use the Materials

To use these materials simply clone this repository, ensuring you are on the
`iwocl21` branch and including submodules.

```
git clone --branch iwocl21 --recursive https://github.com/codeplaysoftware/syclacademy.git
```

The lectures are written in reveal.js, and can be found in `Lesson_Materials`,
in the sub-directory for each topic. To view them simply open the `index.html`
file in your browser. Your browser will have a "Full Screen" mode that can be
used to run the presentation, use the right and left cursors to move forward and
backward in the presentation.

The exercises can be found in `Code_Exercises` in the sub-directory for each
topic. Each exercise has a markdown document instructing what to do in the
exercise, a source file to start with and a solution file to provide an
example implementation to compare against.

## Contributing to SYCL Academy

Contributions to the materials are very gratefully received and this can be done
by submitting a Pull Request with any changes. Please limit the scope of each
Pull Request so that they can be reviewed and merged in a timely manner.

### List of Contributors

Codeplay Software Ltd., Heidelberg University.

## Supporting Organizations
Abertay University, Universidad de Concepcion, TU Dresden, University of
Edinburgh, Federal University of Sao Carlos, University of Glasgow, Heriot Watt
University, Universitat Innsbruck, Universidad de Málaga, University of Salerno
and University of the West of Scotland.

## Lesson Curriculum

The SYCL Academy curriculum is divided up into a number of short lessons
consisting of slides for presenting the material and a more detailed write-up,
each accompanied by a tutorial for getting hands on experience with the subject
matter.

Each of the lessons are designed to be self contained modules in order to
support both academic and training style teaching environments. A playlist of
the video content is [also available][video-playlist]. Though note that these
slides and exercises may have changed since these videos were created so they
may not match completely.

| Lesson | Title | Slides | Exercise | Source | Solution | ComputeCpp | DPC++ | hipSYCL |
|--------|-------|--------|----------|--------|----------|------------|-------|---------|
| 01 | What is SYCL | [slides][lesson-1-slides] | [exercise][lesson-1-exercise] | [source][lesson-1-source] | [solution][lesson-1-solution] | Yes | TBC | Yes |
| 02 | Enqueueing a Kernel | [slides][lesson-2-slides] | [exercise][lesson-2-exercise] | [source][lesson-2-source] | [solution][lesson-2-solution] | Yes | TBC | Yes |
| 03 | Managing Data | [slides][lesson-3-slides] | [exercise][lesson-3-exercise] | [source][lesson-3-source] | [solution][lesson-3-solution] | Yes | TBC | Yes |
| 04 | Handling Errors | [slides][lesson-4-slides] | [exercise][lesson-4-exercise] | [source][lesson-4-source] | [solution][lesson-4-solution] | Yes | TBC | Yes |
| 05 | Device Discovery | [slides][lesson-5-slides] | [exercise][lesson-5-exercise] | [source][lesson-5-source] | [solution][lesson-5-solution] | Yes | TBC | Yes |
| 06 | Data Parallelism | [slides][lesson-6-slides] | [exercise][lesson-6-exercise] | [source][lesson-6-source] | [solution][lesson-6-solution] | Yes | TBC | Yes |
| 07 | Introduction to USM | [slides][lesson-7-slides] | [exercise][lesson-7-exercise] | [source][lesson-7-source] | [solution][lesson-7-solution] | Yes | TBC | Yes |
| 08 | Using USM | [slides][lesson-8-slides] | [exercise][lesson-8-exercise] | [source][lesson-8-source] | [solution][lesson-8-solution] | Yes | TBC | Yes |
| 09 | Asynchronous Execution | [slides][lesson-9-slides] | [exercise][lesson-9-exercise] | [source][lesson-9-source] | [solution][lesson-9-solution] | Yes | TBC | Yes |
| 10 | Data and Dependencies | [slides][lesson-10-slides] | [exercise][lesson-10-exercise] | [source][lesson-10-source] | [solution][lesson-10-solution] | Yes | TBC | Yes |


## Building the Exercises

The exercises can be built for ComputeCpp CE, DPC++ and hipSYCL.

### Supported Platforms

Below is the supported platforms and devices for each SYCL implementations, see
this before deciding which SYCL implementation to use.
Make sure to also install the specified version to ensure that you can build
all of the exercises.

| Implementation | Supported Platforms | Supported Devices | Required Version |
|----------------|---------------------|-------------------|------------------|
| ComputeCpp | Windows 10 Visual Studio 2019 (64bit)* <br> Ubtuntu 18.04 (64bit) | Intel CPU (OpenCL) <br> Intel GPU (OpenCL) | CE 2.4.0 |
| DPC++ | Intel DevCloud <br> Windows 10 Visual Studio 2019 (64bit) <br> Ubtuntu 18.04 (64bit) | Intel CPU (OpenCL) <br> Intel GPU (OpenCL) <br> Intel FPGA (OpenCL) <br> Nvidia GPU (CUDA) | 2021.1-beta05	|
| hipSYCL | Any Linux | CPU (OpenMP) <br> AMD GPU (ROCm)** <br> Nvidia GPU (CUDA) | Latest master |

\* See [here][troubleshooting-for-computecpp] for troubleshooting when using
ComputeCpp with Visual Studio post toolset version 14.26.

\*\* See [here][rocm-gpus] for the official list of GPUs supported by AMD for
ROCm. We do not recommend using GPUs earlier than gfx9 (Vega 10 and Vega 20
chips).

### Install SYCL implementations

First you'll need to install your chosen SYCL implementation and any
dependencies they require.

#### Installing ComputeCpp

To set up ComputeCpp download the [ComputeCpp CE package][computecpp-download]
and follow the [getting started instructions][computecpp-getting-started].

#### Installing DPC++

To set up DPC++ follow the
[getting started instructions][dpcpp-getting-started].

If you are using the Intel DevCloud then the latest version of DPC++ will
already be installed and available in the path.

#### Installing hipSYCL

You will need a hipSYCL build from April 26th 2020 or newer. The easiest way to
install a recent distribution of hipSYCL is to use the
[daily package repositories][hipsycl-repositories-detail]. Binary packages are
provided for Ubuntu 18.04, CentOS 7 and Arch Linux. See
[here][hipsycl-repositories] for an explanation of the packages that you need.

If you do not need the ROCm backend, a recent distribution can also be installed
using the [spack][spack] package manager:
```
spack install hipsycl@master +cuda
```
If you do not need the CUDA backend, you can remove `+cuda`.

Of course, you can also build hipSYCL [from source manually][hipsycl-building].

### Pre-requisites

Before building the exercises you'll need:

* One of the platforms in the support matrix above, depending on which SYCL
implementation you are wishing to build for.
* A C++17 or above tool-chain.
* An appropriate build system for the platform you are targeting (CMake, Ninja,
Make, Visual Studio).

### Configuring using CMake (ComputeCpp CE and hipSYCL only)

Clone this repository, there are some additional dependencies configured as git
sub-modules so make sure to clone those as well. Then simply invoke CMake as
follows:

```
mkdir build

cd build

cmake ../ -G<cmake_generator> -A<cmake_arch> -D<sycl_implementation>=ON
```

For `<cmake_generator>` / `<cmake_arch>` we recommend:

* Visual Studio 16 2019 / x64 (Windows)
* Ninja / NA (Windows or Linux)
* Make / NA (Linux)

For `sycl_implementation` this can be one of:

* `SYCL_ACADEMY_USE_COMPUTECPP`
* `SYCL_ACADEMY_USE_HIPSYCL`

You can also specify the additional optional options:

-DSYCL_ACADEMY_INSTALL_ROOT=<path_to_sycl_impl_install_root>

For `<path_to_sycl_impl_install_root>` we recommend you specify the path to the
root directory of your SYCL implementation installation, though this may not
always be required.

-DSYCL_ACADEMY_ENABLE_SOLUTIONS=ON

This will enable building the solutions for each exercise as well as the source
files. This is disabled by default.

#### Additional cmake arguments for hipSYCL

When building with hipSYCL, cmake will additionally require you to specify the
target platform using `-DHIPSYCL_PLATFORM=cpu|rocm|cuda` and, when compiling for
GPU, the target architecture using `-DHIPSYCL_GPU_ARCH=arch`.
* For NVIDIA GPUs, `arch` is of the form `sm_XX`. For example, `sm_60` for
Pascal GPUs (GeForce GTX 1000 series). 
* When compiling for AMD GPUs, `arch` is of the form `gfxXXX`. For example,
`gfx900` for Vega 10 chips (Vega 56 and Vega 64) or `gfx906` (Radeon VII).

### Compiling directly (DPC++ only)

If you are using DPC++ there is no CMake integration, but it is very simple to
use the DPC++ compiler directly.

First you have to ensure that your environment is configured to use DPC++ (note
if you are using the Intel DevCloud then you don't need to do this step).

On Linux simply call the `setvars.sh` which when is available in
`/opt/intel/inteloneapi` when installed as root or sudo and
`~/intel/inteloneapi/` otherwise.

`source /opt/intel/inteloneapi/setvars.sh`

or

`source ~/intel/inteloneapi/setvars.sh`

On Windows the script is located in  `<dpc++_install_root>\setvars.bat`

Where `<dpc++_install_root>` is wherever the `inteloneapi` directory is
installed.

Once that's done you can invoke the DPC++ compiler as follows:

`dpcpp -I<syclacademy_root>/External/Catch2/single_include -o a.out source.cpp`

Where `<syclacademy_root>` is the path to the root directory of where you cloned
this repository.

### Troubleshooting for ComputeCpp

If you are using ComputeCpp with a more recent version of Visual Sutdio 2019
which has a toolset version greater than 14.26 you may encounter compilation
errors in the C++ STL it's likely due to an unsupported version of the Visual
Studio toolset, if you encounter this the solution is to configure the project
to use an earlier troolset version, you can use the following steps to do this.

* As a pre-requisite, open the Visual Studio 2019 Installer, select "Modify" and
then open the "Individual components" tab and check the following components:
  * `MSVC v142 - VS 2019 C++ x64/x86 build tools (v14.26)`
  * `C++/CLI support for v142 build tools (14.26)`
* First we recommend opening the root directory of the SYCL Academy repository
in Visual Studio 2019 and configuring CMake this way rather than running CMake
on the command line as this makes configurating the toolset version easier.
* Ensure that you are building in Release mode.
* Next, add the following option to the CMake configuration:
  * `-DCOMPUTECPP_DEVICE_COMPILER_FLAGS=-D_ALLOW_COMPILER_AND_STL_VERSION_MISMATCH"`
* Open `CMakeSettings.json` in the root directory and add the following:
```
  "environments": [
    {
      "VCToolsVersion" :  "14.26"
    }
  ],
```

## Online Interactive Tutorial

Hosted by tech.io, this [SYCL Introduction](https://tech.io/playgrounds/48226/introduction-to-sycl/introduction-to-sycl-2) tutorial introduces the concepts of SYCL. The website also provides the ability to compile and execute SYCL code from your web browser.

## Setting up Computers for SYCL

#### Machine Setup Instructions

ComputeCpp, a SYCL v1.2.1 conformant implementation by Codeplay Software provides setup instructions on [developer.codeplay.com](https://developer.codeplay.com). There is more detailed information about what hardware is supported by ComputeCpp on the [Platform Support](https://developer.codeplay.com/products/computecpp/ce/guides/platform-support) page.

Other SYCL implementations can be found on the SYCL community website [sycl.tech](https://sycl.tech).

#### Setting up a Docker Container for Lab Machines

In order to more easily deploy a SYCL implementation onto a bank of machines in a university lab for example, a Docker container can be used to deploy on these machines. This ensures all the dependencies that are needed are installed on each machine.

An example of how to set up a Docker container:

For Intel CPU or GPU
* Download the OpenCL Drivers for Intel from the [Intel website](https://software.intel.com/en-us/articles/opencl-drivers)
* Download the latest ComputeCpp release package from [developer.codeplay.com](https://developer.codeplay.com)

Now create a DockerFile that uses these packages, an example of how this might be done is below. Please note this file is not tested or maintained regularly but shows the elements that need to be installed.

```
FROM ubuntu:18.04

RUN apt-get update
RUN apt-get install -y git
RUN apt-get install -y ninja-build
RUN apt-get install -y g++
RUN apt-get install -y python3
RUN apt-get install -y python3-pip
RUN apt-get install -y software-properties-common

RUN add-apt-repository -y ppa:ubuntu-toolchain-r/test
RUN apt-get update

RUN python3 -m pip install cmake

# install Intel OpenCL drivers from downloaded package
RUN tar -xvf l_opencl_p_18.1.0.015.tgz
RUN cd l_opencl_p_18.1.0.015
RUN chmod +x install.sh
RUN ./install.sh

# Download the Khronos OpenCL headers
RUN git clone https://github.com/KhronosGroup/OpenCL-Headers.git
RUN mv OpenCL-Headers/CL/ /opt/khronos/opencl/include

# Set up the ICD Loader
RUN mkdir -p /etc/OpenCL/vendors/ \
    && echo "$OCL_LIB/libintelocl.so" > /etc/OpenCL/vendors/intel.icd

# Create a directory for ComputeCpp
RUN mkdir /usr/local/computecpp
RUN cd /usr/local/computecpp

# Copy the ComputeCpp release package and extract it to /usr/local/computecpp
RUN cp Ubuntu-16.04-64bit.tar.gz . 
RUN tar -xvf Ubuntu-16.04-64bit.tar.gz

# Add the ComputeCpp location to the path on the machine
ENV PATH=OCL_INC:OCL_LIB:/usr/local/computecpp/bin:/usr/local/computecpp/include:/usr/local/computecpp/lib:${PATH}

ENV CC=gcc-8
ENV CXX=g++-8
```

SYCL and the SYCL logo are trademarks of the Khronos Group Inc.

[computecpp-download]: https://developer.codeplay.com
[computecpp-getting-started]: https://developer.codeplay.com/products/computecpp/ce/guides/getting-started?
[dpcpp-getting-started]: https://software.intel.com/en-us/articles/how-to-install-oneapi-products-and-run-data-parallel-cpp-code-samples

[hipsycl-repositories]: https://github.com/illuhad/hipSYCL#repositories
[hipsycl-repositories-detail]: https://github.com/illuhad/hipSYCL/blob/master/install/scripts/README.md#installing-from-repositories
[hipsycl-download]: https://github.com/illuhad/hipSYCL/blob/master/install/scripts/README.md#installing-from-repositories
[hipsycl-getting-started]: https://github.com/illuhad/hipSYCL#building-and-installing-hipsycl
[hipsycl-building]: https://github.com/illuhad/hipSYCL#manual-installation
[rocm-gpus]: https://github.com/RadeonOpenCompute/ROCm#supported-gpus
[spack]: https://github.com/spack/spack

[video-playlist]: https://youtube.com/playlist?list=PLCssnq0MpRdM-IUAYtNSPYck6u3oz7OZQ

[lesson-1-slides]: ./Lesson_Materials/Lecture_1_What_is_SYCL/
[lesson-1-exercise]: ./Code_Exercises/Exercise_01_Compiling_with_SYCL/doc.md
[lesson-1-source]: ./Code_Exercises/Exercise_01_Compiling_with_SYCL/source.cpp
[lesson-1-solution]: ./Code_Exercises/Exercise_01_Compiling_with_SYCL/solution.cpp

[lesson-2-slides]: ./Lesson_Materials/Lecture_2_Enqueuing_a_Kernel/
[lesson-2-exercise]: ./Code_Exercises/Exercise_02_Hello_World/doc.md
[lesson-2-source]: ./Code_Exercises/Exercise_02_Hello_World/source.cpp
[lesson-2-solution]: ./Code_Exercises/Exercise_02_Hello_World/solution.cpp

[lesson-3-slides]: ./Lesson_Materials/Lecture_3_Managing_Data/
[lesson-3-exercise]: ./Code_Exercises/Exercise_03_Scalar_Add/doc.md
[lesson-3-source]: ./Code_Exercises/Exercise_03_Scalar_Add/source.cpp
[lesson-3-solution]: ./Code_Exercises/Exercise_03_Scalar_Add/solution.cpp

[lesson-4-slides]: ./Lesson_Materials/Lecture_4_Handling_Errors/
[lesson-4-exercise]: ./Code_Exercises/Exercise_04_Handling_Errors/doc.md
[lesson-4-source]: ./Code_Exercises/Exercise_04_Handling_Errors/source.cpp
[lesson-4-solution]: ./Code_Exercises/Exercise_04_Handling_Errors/solution.cpp

[lesson-5-slides]: ./Lesson_Materials/Lecture_5_Device_Discovery/
[lesson-5-exercise]: ./Code_Exercises/Exercise_05_Device_Selection/doc.md
[lesson-5-source]: ./Code_Exercises/Exercise_05_Device_Selection/source.cpp
[lesson-5-solution]: ./Code_Exercises/Exercise_05_Device_Selection/solution.cpp

[lesson-6-slides]: ./Lesson_Materials/Lecture_6_Data_Parallelism/
[lesson-6-exercise]: ./Code_Exercises/Exercise_06_Vector_Add/doc.md
[lesson-6-source]: ./Code_Exercises/Exercise_06_Vector_Add/source.cpp
[lesson-6-solution]: ./Code_Exercises/Exercise_06_Vector_Add/solution.cpp

[lesson-7-slides]: ./Lesson_Materials/Lecture_7_Introduction_to_USM/
[lesson-7-exercise]: ./Code_Exercises/Exercise_07_USM_Selector/doc.md
[lesson-7-source]: ./Code_Exercises/Exercise_07_USM_Selector/source.cpp
[lesson-7-solution]: ./Code_Exercises/Exercise_07_USM_Selector/solution.cpp

[lesson-8-slides]: ./Lesson_Materials/Lecture_8_Using_USM/
[lesson-8-exercise]: ./Code_Exercises/Exercise_08_USM_Vector_Add/doc.md
[lesson-8-source]: ./Code_Exercises/Exercise_08_USM_Vector_Add/source.cpp
[lesson-8-solution]: ./Code_Exercises/Exercise_08_USM_Vector_Add/solution.cpp

[lesson-9-slides]: ./Lesson_Materials/Lecture_9_Asynchronous_Execution/
[lesson-9-exercise]: ./Code_Exercises/Exercise_09_Synchronization/doc.md
[lesson-9-source]: ./Code_Exercises/Exercise_09_Synchronization/source.cpp
[lesson-9-solution]: ./Code_Exercises/Exercise_09_Synchronization/solution.cpp

[lesson-10-slides]: ./Lesson_Materials/Lecture_10_Data_and_Dependencies/
[lesson-10-exercise]: ./Code_Exercises/Exercise_10_Managing_Dependencies/doc.md
[lesson-10-source]: ./Code_Exercises/Exercise_10_Managing_Dependencies/source.cpp
[lesson-10-solution]: ./Code_Exercises/Exercise_10_Managing_Dependencies/solution.cpp

