mshadow: Matrix Shadow
======

MShadow is a lightweight CPU/GPU Matrix/Tensor Template Library in C++/CUDA. The goal of mshadow is to support ***efficient***,
***device invariant*** and ***simple*** tensor library for machine learning project that aims for both simplicity and performance.

MShadow also provides interface that allows writing Multi-GPU and distributed deep learning programs in an easy and unified way.

* [Contributors](https://github.com/tqchen/mshadow/graphs/contributors)
* [Tutorial](guide)
* [Documentation](doc)
* [Parameter Server Interface for GPU Tensor](guide/mshadow-ps)

Features
=====
* Efficient: all the expression you write will be lazily evaluated and compiled into optimized code
  - No temporal memory allocation will happen for expression you write
  - mshadow will generate specific kernel for every expression you write in compile time.
* Device invariant: you can write one code and it will run on both CPU and GPU
* Simple: mshadow allows you to write machine learning code using expressions.
* Whitebox: put a float* into the Tensor struct and take the benefit of the package, no memory allocation is happened unless explicitly called
* Lightweight library: light amount of code to support frequently used functions in machine learning
* Extendable: user can write simple functions that plugs into mshadow and run on GPU/CPU, no experience in CUDA is required.
* MultiGPU and Distributed ML: mshadow-ps interface allows user to write efficient MultiGPU and distributed programs in an unified way.

Related Projects
=====
* [CXXNET: large-scale deep learning backed by mshadow](https://github.com/antinucleon/cxxnet)
* [Parameter Server](https://github.com/mli/parameter_server)
  - Parameter server project provides distributed back-end for mshadow-ps
  - mshadow-ps extends original parameter server to support async updates for GPU Tensor
