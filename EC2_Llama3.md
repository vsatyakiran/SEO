# Problems faced when hosting llama3 8b on aws instance

**What are the hardware configurations required of LLama3 8B**

1.High latency when running the lamma3 8b model on local system
  - `Solution:` LLaMA 3 8B requires around 16GB of disk space and 20GB of VRAM (GPU memory) in FP16. You could of course deploy LLaMA 3 on a CPU but                 the latency would be too high for a real-life production use case. As for LLaMA 3 70B, it requires around 140GB of disk space and                    160GB of VRAM in FP16. `On AWS EC2, you should select a G5 instance in order to provision an A10 GPU. A g5.xlarge will be enough.`

2. AWS Error for vCPU
  - `Error:`You have requested more vCPU capacity than your current vCPU limit of 0 allows for the instance bucket that the specified instance type belongs to. Please visit http://aws.amazon.com/contact-us/ec2-request to request an adjustment to this limit.

**How to check your VRAM:** You can check your computer's VRAM by opening the Settings app, selecting System > Display > Advanced display > Display adapter properties for Display 1, and then looking at the number next to Dedicated Video Memory. 

# what are quantization techniques ?
