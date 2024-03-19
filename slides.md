---
theme: seriph
background: ./images/background.jpg
class: text-center
highlighter: shiki
lineNumbers: false
persist: false
defaults:
  foo: true
transition: slide-left
title: Introduction to Artificial Intelligence and Computer Vision
mdc: true
---

# Artificial Intelligence and Computer Vision

Workshop

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <!-- <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button> -->
  <a href="https://github.com/antoniomtz/ai-cv-workshop" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: slide-left
---

# Outline

<ol>
  <li>Introduction of AI and CV</li>
  <li>AI and CV Basics</li>
  <li>Intel SW and HW</li>
  <li>Hands-on with openVINO</li>
  <li>Questions</li>
</ol>    


---
layout: cover
transition: slide-left
background: ./images/background.jpg
---
# Introduction of AI and CV

---
transition: slide-left
level: 2
---

# Use case: Intelligence queue management
<br/>
<center>
  <video width="600" height="300" controls>
    <source src="/assets/intelligent-queue.mp4" type="video/mp4">
  </video>
</center>

---
layout: image-right
image: ./images/ai-graphics.jpg
transition: slide-left
---

# Definitions

<v-click>
<ul>
  <li>AI involves teaching computers to process data in a way that <b>mimics the human brain</b></li>
</ul>
</v-click>

<v-click>
<ul>
  <li><b>Computer Vision</b> is a field of AI that focuses on enabling computers to <b>interpret visual data</b></li>
</ul>
</v-click>

<v-click>
  <ul>
    <li>AI and CV are important in our lives for several reasons:<ul>
      <li>Automation</li>
      <li>Healthcare</li>
      <li>Safety</li>
      <li>Customer experience</li>
    </ul>
    </li>
  </ul>
</v-click>

---
transition: slide-left
---
# Computer Vision Use Cases

<div grid="~ cols-2 gap-4">
  <div>
    <ul>
      <li>Robotics</li>
      <li>Facial Recognition</li>
      <li>Object Detection</li>
      <li>Medical Imaging</li>
    </ul>
  </div>

  <div>
    <img src="/assets/cv-use-cases.jpg" />
  </div>

</div>

---
transition: slide-left
---
# Robotics Use Cases

* Self-driving Cars
  * Commercial vehicles
  * Delivery robots
* Surveillance robots
* Drones

<div grid="~ cols-2 gap-2" m="t-2">

  <img border="rounded" src="/assets/Autonomous-driving-Barcelona.jpg" alt="">

  <iframe width="450" height="250" src="https://www.youtube.com/embed/kN0MLclnWa0?si=w1yJBFJ_IS81y-eo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

</div>


---
transition: slide-left
---
# Object Detection Use Cases

<div grid="~ cols-2 gap-4">
  <div>
    <ul>
      <li>Retail:
        <ul>
          <li>Automated Self Checkout</li>
          <li>Inventory Magagement</li>
          <li>Customer Experience</li>
        </ul>
      </li>
      <li>Self-driving Vehicles:
        <ul>
          <li>Pedestrian detection</li>
          <li>Trees,cars,etc detection</li>
          <li>Lane detection</li>
        </ul>
      </li>
    </ul>
  </div>

  <div>
   <iframe width="350" height="200" src="https://www.youtube.com/embed/lEWFmKI5RYY?si=bsUWXxiUOfh4KId3" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
   <br/>
   <iframe width="350" height="200" src="https://www.youtube.com/embed/3B8369neIHI?si=dpDsaq8x1yyDsv41" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  </div>

</div>

---
transition: slide-left
---
# Facial Recognition Use Cases

* Facial Authentication
  * Buildings
  * Phones
* Criminal detection
  * Airports
  * Stores

<div grid="~ cols-2 gap-2" m="t-2">

  <img border="rounded" src="/assets/airport.jpg" alt="">

  <iframe width="450" height="250" src="https://www.youtube.com/embed/SnH5qe8_rps?si=ym6M0GQGbs73GCzK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

</div>

---
layout: cover
transition: slide-left
background: ./images/background.jpg
---
# AI and CV Basics

---
transition: slide-left
---
# How does AI/CV work?
<br/>
<br/>
<br/>
<br/>
<br/>
<center>
```mermaid {theme: 'default',scale: 1, alt: 'A simple sequence diagram'}
flowchart LR
    data["Data Collection"]
    model["Model Creation"]
    inference["Inferencing Application"]
    data --> Annotation --> Training --> model --> inference   
```
</center>
---
transition: slide-left
---
# Type of CV Models
<div grid="~ cols-2 gap-4">
  <div>
    <ul>
    <li>Classification</li>
    <li>Detection</li>
    <li>Semantic Segmentation</li>
    <li>Instance segmentation</li>
    </ul>
  </div>

  <div>
    <img src="/assets/models.jpg" />
  </div>

</div>
---
layout: image-right
image: ./images/dogs.jpg
transition: slide-left
---
# Data Collection

* Collect-Create hundresds or thousands of images for the desire output.

# Annotation

* Manually indentify desired object on each image. (object detection)
* Manually name each image (classification)

# Training

* Tensorflow
* Pytorch 

# Model & Inferencing

* Use your model with your application

---
layout: cover
transition: slide-left
background: ./images/background.jpg
---

# Intel Software and Hardware on AI

---
transition: slide-left
---

# Intel GETi

<div grid="~ cols-2 gap-4">
  <div>
    <ul>
      <li>Train models for classification, object detection, segmentation or anomaly detection</li>
      <li>Annotation tools</li>
      <li>Optimized models for Intel architecture (CPU,GPUS)</li>      
    </ul>
  </div>

  <div>
    <img src="/assets/intel-geti.jpg"  />
    <center>
      <img src="/assets/intel-geti-1024.jpeg" width="200" />    
      geti.intel.com
    </center>
  </div>

</div>

---
transition: slide-left
---

# Intel openVINO

* Opensource toolkit that accelerates AI inference.
* Used for AI development and integration of deep learning in domains like computer vision, LLM and genAI.

<center>
  <img src="/assets/openvino.jpg" width="800"  />
</center>


---
transition: slide-left
---

# Intel openVINO Model Server

* A scalable inference server for models opmitized with OpenVINO.

<center>
  <img src="/assets/ovms_diagram.jpg" width="800"  />
</center>

---
transition: slide-left
---

# Intel DLStreamer

* Streaming media analytics framework, based on Gstreamer.
* Enables developers to create deep learning pipelines across Intel architecture.

<div grid="~ cols-2 gap-2" m="t-2">
  <img src="/assets/dlstreamer.jpg" width="350" />
  <img src="/assets/dlstreamer.gif"  />
</div> 

---
transition: side-left
---

# Intel Hardware in AI

<div grid="~ cols-2 gap-4">

<div markdown="1">
<ul>
<v-click>
  <li>CPU<ul>
    <li>Atom</li>
    <li>Core 5,7,9</li>
    <li>Xeon</li>
  </ul>
  </li>
</v-click>
<v-click>
  <li>GPU<ul>
    <li>iGPU</li>
    <li>Flex GPU</li>
    <li>Arc GPU</li>
  </ul>
  </li>
</v-click>
<v-click>
  <li>VPU</li>
  <li>NPU</li>
</v-click>
</ul>
</div>

<div>
  <center>
    <img src="/assets/intel-hw.jpg" width="400" />  
    <img src="/assets/intel-cpu.jpg" width="300" />
  </center>
</div>
</div>

---
transition: side-left
layout: cover
---

# Hands-on with openVINO

---
transition: side-left
---

# Intel DLStreamer

<div grid="~ cols-2 gap-4">

  <div>
    <img src="/assets/dlstreamer-syntax.jpg" />
  </div>

  <div>
    <img src="/assets/dlstreamer-demo.gif" />
  </div>

</div>

---
transition: side-left
layout: full
---
<video controls>
  <source src="/assets/dlstreamer-demo-small.mp4" type="video/mp4">
</video>

---
transition: side-left
---
# DLStreamer on Windows using docker

Prerequisites:

Install <a href="https://docs.docker.com/desktop/install/windows-install/" target="_blank">Docker on Windows</a>

<v-click>

## Step 1 Download Moba Xterm

<a href="https://mobaxterm.mobatek.net/download-home-edition.html" target="_blank">MobaXterm</a>
</v-click>
<v-click>

## Step 2 Run DLstreamer docker container

```docker
docker run -it --rm --network=host --entrypoint /bin/bash --name dlstreamer_test --privileged --user root openvino/ubuntu18_data_dev
```
<br/>
</v-click>
<v-click>

## Step 3 Download Models

```bash 
cd /opt/intel/openvino/data_processing/dl_streamer/samples
./download_models.sh
```
</v-click>

---
transition: side-left
---
## Step 4 Run Face Detection/Age-Gender/Emotions pipeline

<br/>

```bash
gst-launch-1.0 urisourcebin buffer-size=4096 uri=https://github.com/intel-iot-devkit/sample-videos/raw/master/head-pose-face-detection-female-and-male.mp4 !
 decodebin ! videoconvert ! video/x-raw,format=BGRx ! gvadetect model=/root/intel/dl_streamer/models/intel/face-detection-adas-0001/FP32/face-detection-adas-0001.xml 
 device=CPU ! queue ! gvaclassify model=/root/intel/dl_streamer/models/intel/age-gender-recognition-retail-0013/FP32/age-gender-recognition-retail-0013.xml model-proc=/opt/intel/openvino/data_processing/dl_streamer/samples/gst_launch/face_detection_and_classification/model_proc/age-gender-recognition-retail-0013.json 
 device=CPU ! queue ! gvaclassify model=/root/intel/dl_streamer/models/intel/emotions-recognition-retail-0003/FP32/emotions-recognition-retail-0003.xml model-proc=/opt/intel/openvino/data_processing/dl_streamer/samples/gst_launch/face_detection_and_classification/model_proc/emotions-recognition-retail-0003.json 
 device=CPU ! queue ! gvaclassify model=/root/intel/dl_streamer/models/intel/landmarks-regression-retail-0009/FP32/landmarks-regression-retail-0009.xml model-proc=/opt/intel/openvino/data_processing/dl_streamer/samples/gst_launch/face_detection_and_classification/model_proc/landmarks-regression-retail-0009.json 
 device=CPU ! queue ! gvawatermark ! videoconvert ! fpsdisplaysink video-sink=ximagesink sync=false
```
<center>
  <img src="/assets/facedetection.jpg" width="450" />
</center>

---
transition: side-left
layout: full
---
<video controls>
  <source src="/assets/dlstreamer-win.mp4" type="video/mp4">
</video>

---
transition: side-left
---

# OpenVINO Runtime

## Install openVINO python runtime

```bash
pip install -q "openvino>=2023.1.0"
```
<v-click>

## Initialize openVINO runtime 

```python
import openvino as ov
core = ov.Core()
```
</v-click>

<v-click>

## Loading a model

```python
classification_model_xml = "model/classification.xml"
model = core.read_model(model=classification_model_xml)
compiled_model = core.compile_model(model=model, device_name="CPU") # Compile model to a specific device
```
</v-click>

<v-click>

## Analyze the input

```python
model.inputs # [<Output: names[input, input:0] shape[1,3,224,224] type: f32>]
```

* model expects one input and input data with the batch size of 1 (N), 3 channels ( C) , and images with a height (H) and width (W) equal to 224.
</v-click>
---
transition: side-left
layout: two-cols
---

## Analyze the output

```python
model.outputs # [<Output: names[MobilenetV3/Predictions/Softmax] shape[1,1001] type: f32>]
```

* shape of [1, 1001] where 1001 is the number of classes

<v-click>

## Load an Image

```python
image = cv2.cvtColor(cv2.imread(filename=str("image.jpg")), code=cv2.COLOR_BGR2RGB) # RBG Format  
input_image = cv2.resize(src=image, dsize=(224, 224)) # Resize image
input_image = np.expand_dims(input_image, 0) # Reshape image
input_image.shape # (1, 3, 224, 224)
```
</v-click>

<v-click>

## Do Inference
```python
output_layer = compiled_model.output(0)
result_infer = compiled_model([input_image])[output_layer]
result_index = np.argmax(result_infer)
imagenet_classes[result_index] # n02099267 flat-coated retriever
```
</v-click>

::right::

<img src="/assets/dog.png" />

---
transition: side-left
---

# openVINO Jupyter notebooks

<a href="https://github.com/openvinotoolkit/openvino_notebooks" target="_blank">https://github.com/openvinotoolkit/openvino_notebooks</a>

<div grid="~ cols-3 gap-2" m="t-1">
  <img src="https://user-images.githubusercontent.com/47499836/163544861-fa2ad64b-77df-4c16-b065-79183e8ed964.png" width="250"/>
  <img src="https://user-images.githubusercontent.com/4547501/141471665-82b28c86-cf64-4bfe-98b3-c314658f2d96.gif" width="250"/>
  <img src="https://docs.openvino.ai/2024/_images/208-optical-character-recognition-with-output_26_0.png" width="250" />
</div>

<div grid="~ cols-3 gap-2" m="t-1">
  <img src="https://docs.openvino.ai/2024/_images/230-yolov8-instance-segmentation-with-output_11_1.png" width="250" />
  <img src="https://user-images.githubusercontent.com/91237924/210479548-b70dbbaa-5948-4e49-b48e-6cb6613226da.gif" width="300" />
  <img src="https://user-images.githubusercontent.com/10940214/151552326-642d6e49-f5a0-4fc1-bf14-ae3f457e1fec.gif" width="300" />
</div>

---
transition: side-left
layout: two-cols
---

# AI popular trends (genAI)

* Text to Video/Image generation
* Large Language Models (LLM)
* Natural Language procesing (NLP)
* Sound generators

::right::

<table>
<thead>
<tr>
<th style="text-align:center">Darth Vader is surfing on waves</th>
</tr>
</thead>
<tbody>
<tr>
<center>
  <td style="text-align:center"><img src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/diffusers/darthvader_cerpense.gif" width="200" alt=""></td>
</center>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th style="text-align:center">a beautiful pink unicorn</th>
</tr>
</thead>
<tbody>
<tr>
<center>
  <td style="text-align:center"><img src="https://user-images.githubusercontent.com/29454499/277367065-13a8f622-8ea7-4d12-b3f8-241d4499305e.png" width="200" alt=""></td>
</center>
</tr>
</tbody>
</table>

---
transition: side-left
---

# How to start developing AI/CV applications

* Install an IDE (<a href="https://code.visualstudio.com/" target="_blank">vscode</a>)
* Install python or c++, openVINO and Docker
* Demos from openVINO model zoo <a href="https://github.com/openvinotoolkit/open_model_zoo/tree/master/demos" target="_blank">repo</a> 
* Retail use cases using openVINO model server gRPC or cAPI and docker containers (<a href="https://github.com/intel-retail/retail-use-cases" target="_blank">link</a>)
<center>
  <img src="/assets/vscode.jpg" width="420"/>
</center>


---
layout: cover
background: ./images/background.jpg
---
# Questions
