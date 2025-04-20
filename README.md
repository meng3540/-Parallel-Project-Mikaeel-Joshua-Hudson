# -Parallel-Project-Mikaeel-Joshua-Hudson

Discussion on problem statement:

There is a challenge in achieving real-time object detection on embedded devices while optimizing its performance and hardware efficiency. With how AI is being integrated into alot of fields now, there is a need or high demand for creating AI that is fast, has the highest efficiency and do not have latency or privacy issues. GPU-accelerated embedded devices can be leveraged by offloading the computational burden of the AI inferencing to a more highly parallelized hardware in which the NVIDIA Jetson Nano 6.1 was used in this case. This served to provide significant improvements in throughput and latency. The steps followed to demonstrate this idea would be through the exploration of the NVIDIA Jetson Nano 6.1 which was used to implement a basic object detection model. The SD card would be prepared and inserted into Jetson device, Jetson would be booted, connected and configured with PuTTY. It would then be connected to a Wi-Fi network. Camera would be setup, Visual studio would be installed along with the necessary extensions and dependencies. Model would be selected, program would be created and modified to use camera. Finally, it would be optimized, monitored and put through testing until ready to be deployed. Skills in CUDA programming, optimization of AI and embedded systems would be further developed and focus would be given more on AI application for edge devices.


Initial configuration and setup of the edge device and the software:
   - Flashing the SD card:
      JetPack 6.1 image was downloaded and flashed onto a micro-SD card using Balena Etcher. 
      This was done after formatting the card with SD formatter.
     
   - Booting and serial connection setup for NVIDIA JEtson 6.1:
      The Jetson Nano was connected to a host PC using a USB-C cable and intiial setup was done 
      through PuTTY using a serial connection at a Baud rate of 115200. 
     
   - Network configuration:
      The NVIDIA Jetson 6.1 device was connected using the nmcli command. IP address was found 
      using the ifconfig command would provide a path for interent conenction of the Jetson 
      device. SSH access was used with PuTTY using IP address as serial cable is no longer  
      needed.

   - Camera Configuration:
      Camera was set up using the nvgstcapture command to capture images and manually video the 
      environment.


List of possible hardware,software frameworks and libraries that can be used:
- Hardware: Monitor, keyboard, camera, NVIDIA Jetson 6.1 device, mouse
- Software framework: JetPack SDK, TensorRT, ONNX Runtime, Ultralytics YOLOv11N, VS Code, jtop and 
  PuTTY.
- Libraries: opencv-python, numpy, torch, onnx, onnxruntime-gpu

  
Choice of pre-trained models and rationale for your selection
- YOLOv11N

The reasoning for choosing this pre-trained model is due to how optimized this model is for real time object detection as it offers a good ballance between speed and accuracy when compared to others. It provides proper detection acrosss many common obects wihtout the need for custom training. Its very flexible as there are different model sizes of YOLOv5 which can be chosen based on performance or resource limitations. Lastly, it is very easy to implement as it supports GPU acceleration and integration with the TensorRT.
















