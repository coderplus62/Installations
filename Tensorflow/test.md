# Device Installation

Step-by-Step Tutorial for PC Installation for Deep Learning Applications:
Note: This tutorial assumes you are using a Windows operating system.

## 1. Driver Setup:
   - Download and install [NVIDIA Driver](https://www.bing.com/ck/a?!&&p=525f9c0cd8286e05JmltdHM9MTY4NDcxMzYwMCZpZ3VpZD0zNDA1MDQwOS1lYjhmLTZhMDItMzM1Ny0xNmVlZWFkOTZiZDQmaW5zaWQ9NTE4NA&ptn=3&hsh=3&fclid=34050409-eb8f-6a02-3357-16eeead96bd4&psq=nvidia+drivers&u=a1aHR0cHM6Ly93d3cubnZpZGlhLmNvbS9Eb3dubG9hZC9pbmRleC5hc3B4P2xhbmc9ZW4tdXM&ntb=1)
   - Download and install [CUDA Toolkit v11.8](https://developer.nvidia.com/cuda-toolkit-archive) 
   - Download [cuDNN v8.6](https://developer.nvidia.com/rdp/cudnn-archive) 
        - Copy the files from the `bin` directory to `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.8\bin`
        - Copy the files from the `include` directory to `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.8\include`
        - Copy the files from the `lib` directory to `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.8\lib\x64`.
   - Download and install [Visual Studio 2015, 2017, 2019, and 2022](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)

## 2. Apps Setup (Anaconda):
   - Download and install [Git](https://www.bing.com/ck/a?!&&p=d60f585f2e245f59JmltdHM9MTY4NDcxMzYwMCZpZ3VpZD0zNDA1MDQwOS1lYjhmLTZhMDItMzM1Ny0xNmVlZWFkOTZiZDQmaW5zaWQ9NTE5MQ&ptn=3&hsh=3&fclid=34050409-eb8f-6a02-3357-16eeead96bd4&psq=download+git&u=a1aHR0cHM6Ly9naXQtc2NtLmNvbS9kb3dubG9hZHM&ntb=1)
   - Download and install [Anaconda](https://www.bing.com/ck/a?!&&p=e8839c9daa00ef27JmltdHM9MTY4NDcxMzYwMCZpZ3VpZD0zNDA1MDQwOS1lYjhmLTZhMDItMzM1Ny0xNmVlZWFkOTZiZDQmaW5zaWQ9NTE5MA&ptn=3&hsh=3&fclid=34050409-eb8f-6a02-3357-16eeead96bd4&psq=anaconda+download&u=a1aHR0cHM6Ly93d3cuYW5hY29uZGEuY29tL2Rvd25sb2FkLw&ntb=1)

## 3. Create Environment and Install TensorFlow GPU (Native Windows):
   - Open the Anaconda Prompt (found in the Start Menu under Anaconda) or any command prompt.
   - Create a new conda environment by running the following command:
      ```
      conda create --name tf_gpu python=3.9
      ```
   - Activate the newly created environment using the following command:
      ```
      conda activate tf_gpu
      ```
   - GPU setup:
      ```
      conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
      ``` 
   - Install TensorFlow GPU using pip by running the following command:
      ```
      pip install -r requirements.txt
      ```

## 4. Testing:
   - Verify the installation by running this code:
      ```
      python -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
      ```

If you have errors related to the installation please contact me through this [email](mailto:igedesusastragunawan@gmail.com) with *SUBJECT* **ERROR INSTALLATION**