# Real-time object detection for disaster response using Transfer Learning Toolkit

A notebook that demonstrates how to use the NVIDIA Intelligent Video Analytics suite to detect objects in real-time. 
We use **Transfer Learning Toolkit** to train a fast and accurate detector and **DeepStream** to run that detector on an NVIDIA Jetson edge device.

![IVA diagram](https://developer.nvidia.com/sites/default/files/akamai/deeplearning/tlt/tlt_end_to_end_v2.png)

## Getting Started Guide

Sign up for a free NVIDIA GPU Cloud (NGC) account at [ngc.nvidia.com](https://ngc.nvidia.com), then pull the Transfer Learning Toolkit (TLT) container.

```
DATA_DIR=/path/to/your/data
WORKING_DIR=/path/to/workingdir # include the "specs" and "deepstream" directories

docker pull nvcr.io/nvidia/tlt-streamanalytics:v1.0_py2
docker run --runtime=nvidia -it -v $DATA_DIR:/data \ 
        -v $WORKING_DIR:/src -p 8888:8888 \ 
        nvcr.io/nvidia/tlt-streamanalytics:v1.0_py2 /bin/bash
```

Launch jupyter notebook

```
cd /src
jupyter notebook --ip=0.0.0.0 --allow-root
```

Now navigate in your browser (we use Chrome) to `<your host IP>:8888`. If working on a local machine you can go to `localhost:8888`.

## References

This notebook accompanies the Real-time object detection for disaster response using Transfer Learning Toolkit webinar, available at [info.nvidia.com/real-time-object-detection-for-disaster-response-reg-page.html](https://info.nvidia.com/real-time-object-detection-for-disaster-response-reg-page.html).

For more information on Transfer Learning Toolkit: [developer.nvidia.com/transfer-learning-toolkit](https://developer.nvidia.com/transfer-learning-toolkit)