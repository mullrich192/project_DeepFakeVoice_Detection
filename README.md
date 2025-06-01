# DeepFakeVoice Detection

Project in the context of the course "Signal and Natural Language Processing with Deep Learning" at the UPV in Valencia.

## Project Objective
The project presents an approach to detect Deepfake voices iin audio recordings. 

## Dataset
The dataset used in this project is called "in-the-wild", which was created by the Fraunhofer AIESEC Institut (https://deepfake-total.com/in_the_wild)

### CNN structure
```mermaid
graph TB
  input[Input Layer: 128, 126, 1] --> conv1[Conv Layer: 32, 3x3 Filters]
  conv1 --> relu1[ReLU Activation]
  relu1 --> pool1[Max Pooling: 2x2, stride=2]
  pool1 --> flatten[Flatten Layer]
  flatten --> fc1[Fully Connected Layer: 128 Neurons]
  fc1 --> relu3[ReLU Activation]
  relu3 --> drop[Dropout Layer: 0.5]
  drop --> output[Fully Connected Output Layer: 2 Classes]
  output --> softmax[Softmax Activation]

```
