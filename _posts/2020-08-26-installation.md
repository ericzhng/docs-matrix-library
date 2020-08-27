---
layout: post
title:  "Install matrix-library"
date:   2020-08-26 11:00:00
author: Dr. Hui Zhang
---

This post addresses the installation of matrix-library package in Ubuntu. Other Linux distrbutions are not tested here, but should be able to adapted correspondingly.

## Intro

The matrix-library contains two packages, LAPACK and ScaLAPACK. BLAS library is included in the LAPACK package. Sometimes compiling and linking them might cause some troubles for novices. Thereby some efforts are taken here to simplify the installation of LAPACK and ScaLAPACK packages to any specified directory.

The matrix-library source codes are directly from the original packages of LAPACK and ScaLAPACK. The original LAPACK package can be downloaded [here](http://www.netlib.org/lapack/) and the original ScaLAPACK is availible [here](http://www.netlib.org/scalapack/). The LAPACK versions is 3.8.0 and ScaLAPACK version if 2.0.0. The newest versions will be updated accordingly.  

You can download the matrix-library packages from the GitHub repositories below.
* https://github.com/ericzhng/matrix-library-lapack
* https://github.com/ericzhng/matrix-library-scalapack

After you have these two repositories, you can now go inside them and compile the codes and install the libraries to your system.


## Install LAPACK

The `matrix-library-lapack` directory contains all source codes to LAPACK library, including its C version wrappers. Regardless, you can call the Fortran library or C library at your own convenience. BLAS and its C version, CBLAS, are included here. The original packages are missing some functions, compared to original BLAS package. The missing functions are added here. 

The steps to install LAPACK in your system is as follows:
* `sudo apt-get update` to download package information from sources.
* `sudo apt-get -y upgrade` to upgrade system changes.
* `sudo apt-get -y install build-essential gfortran` to install missing compilers.
* `make all` to compile all static and dynamic libraries. `make lib` for static only, `make shared_lib` depends on static libraries, and can only be issued after `make lib`. After the compiling finishes successfully, you should be able to see .a and .so libraries generated in the main directory.
* `make man` to compile manual pages.
* `make install PREFIX=$(HOME)/matrix-library/lapack` to install LAPACK libraries.


## Install ScaLAPACK

The `matrix-library-scalapack` directory contains all source codes to ScaLAPACK library, including BLACS, PBLAS and so on. These are a mix of C and Fortran programs. The compilation of them requires MPI tools. 

The steps to install ScaLAPACK in your system is as follows:
* `sudo apt-get update` to download package information from sources.
* `sudo apt-get -y upgrade` to upgrade system changes.
* `sudo apt-get -y install openmpi` to install mpif90 and mpicc. Other MPI packages can be used as well.
* `make all` to compile all static and dynamic libraries. `make lib` for static only, `make shareso` depends on static libraries, and can only be issued after `make lib`. After the compiling finishes successfully, you should be able to see .a and .so libraries generated in the main directory.
* `make install PREFIX=$(HOME)/matrix-library/scalapack` to install ScaLAPACK libraries.


## Test LAPACK

After successfully generating the libraries for LAPACK, you should be able to see the following files:
 - libtmglib.a (.so)
 - libblas.a (.so)
 - libcblas.a (.so)
 - liblapack.a (.so)
 - liblapacke.a (.so)

You can type `make cblas_example` or `make lapacke_example` to see whether these libraries would work.

To test whether BLAS and LAPACK libraries can be linked from the installed location, you need to follow the below steps.

* Define LAPACK_LIB/LAPACK_INC environment variables in either .bashrc file or export them to use them temporarily. LAPACK_LIB=$(HOME)/matrix-library/lapack/lib64.
* Add LAPACK_LIB to LD_LIBRARY_PATH if you need to use the shared libraries, by issuing `export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$LAPACK_LIB`.
* For any program that needs to link to these libraries, you can either use the static libraries or shared libraries.
*  to use the static library, do something like `gcc -o test test.cpp $(LAPACK_LIB)/lapack.a $(LAPACK_LIB)/blas.a`.
*  to use the dynamic library, do something like `gcc -o test test.cpp -L$(LAPACK_LIB) -llapack -lblas`. Sometimes you might need to add options like `-lgfortran`.
* The order for the linking matters here. Always use `-llapacke -llapack -lcblas -lblas` order.


## Test ScaLAPACK

After successfully generating the libraries for ScaLAPACK, you should be able to see the following files:
 - libscalapack.a (.so)

You can type `make exe` to see whether these libraries would work. However, you would need to have installed LAPACK libraries already in the OS system for these tests to work correctly.

To test whether ScaLAPACK libraries can be linked from the installed location, you need to follow the below steps.

* Define SCALAPACK_LIB environment variables in either .bashrc file or export them to use them temporarily. SCALAPACK_LIB=$(HOME)/matrix-library/scalapack/lib64. Sometimes if you are using BLACS, you need to add the header files as well. It is defined by: SCALAPACK_INC=$(HOME)/matrix-library/scalapack/include.
* Add SCALAPACK_LIB to LD_LIBRARY_PATH if you need to use the shared libraries, by issuing `export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$SCALAPACK_LIB`.
* For any program that needs to link to these libraries, you can either use the static libraries or shared libraries.
*  to use the static library, do something like `mpicc -o test test.cpp $(SCALAPACK_LIB)/scalapack.a $(LAPACK_LIB)/lapack.a $(LAPACK_LIB)/blas.a`.
*  to use the dynamic library, do something like `mpicc -o test test.cpp -L$(SCALAPACK_LIB) -lscalapack -llapack -lblas`. Sometimes you might need to add options like `-lgfortran`.
* The order for the linking matters here. Always use `-lscalapack -llapack -lblas` order.
