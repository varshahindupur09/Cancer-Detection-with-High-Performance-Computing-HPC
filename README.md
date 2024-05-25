# Overview:
Leveraging PyTorch's distributed computing capabilities, this project aims to accelerate the training of a deep learning model for lung and colon cancer image classification, harnessing the power of parallelism and GPU acceleration to achieve faster convergence and improved model performance

Our choice for image classification is ResNet, a cutting-edge neural network designed for this purpose. However, its depth, while beneficial for accuracy, often leads to longer training durations. ​

In an era where swift model training is crucial, the growing need for high-performance parallel computation has driven us to meet the challenge head-on by optimizing and executing our models in parallel.​

To significantly reduce the training time of image classification models through efficient high parallel computation, enabling faster experimentation and deployment in real-world scenarios.​

P.S. All the codes are executed on Discovery's CPUs and GPUs.

# Methods used to increase the performance of the models:

1. Serial Execution
2. DDP (Distributed Data Parallel) on CPU
3. DDP on GPU
4. Model Parallelism
5. AMP (Automatic Mixed Precision)

# Results & Analysis derived from the executions are as follows:

Images were pre-processing using following techniques:

<img width="942" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/83e88240-6fd1-4c58-b328-6454097bcbad">

Data Loading Parallelization is performed using Dask and Multiprocessing.Pool() functions. Other aspects considered were async Pool, async apply and more.

<img width="927" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/79b2f7ab-c586-44c0-ad6f-a2afafe708f6">

Data Modeling Parallelization results are accumulated via Serial executions on CPU, DDP (Distributed Data Processing on CPU) and DDP on GPU.

<img width="931" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/be7ef1a0-fd6a-4cbd-b60e-66ec1c5eb473">

<img width="942" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/58ac25c9-5fdd-499e-b49b-2e4cf3b2c71d">

<img width="940" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/6254fc1f-2225-46ec-9643-0d69a4adb91c">

<img width="940" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/a59de35a-6e89-47b5-b6e3-9e416690a02b">

<img width="931" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/de0ead0d-0786-40ec-9ed5-7e17a3ddbc1b">

SpeedUp and Efficiency:

<img width="439" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/e167bf87-2e77-4d34-a9b7-dd42988d647e">

<img width="425" alt="image" src="https://github.com/varshahindupur09/HighPerformanceParallelComputingProject/assets/114629181/84476e69-63ad-474e-b485-bb0612a204b0">


# Conclusion: 

And, as per the result part we could train our model in 30 seconds using the parallel processing techniques and still maintain the accuracy to 93% overall.

The procedures used were 24 times efficient when compared to Serial Executions on CPU. Speedup recieved was more than 50%. Overall, if all the model executes in 30 seconds with the use of modern compute resources, then we have achieved our goal of making the product available to consumers and businesses. 
