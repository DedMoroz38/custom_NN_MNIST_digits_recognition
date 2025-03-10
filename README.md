# Custom MNIST digit classification Neural Network

Today I've decided to build a custom NN for digit classification without any libraries like PyTorch or TensorFlow and get around with **numpy** only !🚀 
Idea behind the project is to learn how neural networks work behind the since: math, forward/backward propagation, etc.

Here I am using MNIST dataset which can be downloaded from: [kaggle](https://www.kaggle.com/competitions/digit-recognizer/data)

## Dataset structure:

**28x28** images all labeled **0-10**

## Neural Network Structure

**1. Input Layer**
- 784 neurons (each representing the 28x28 image)

**2. Hidden Layer**
- 10 neurons 

**1. Output Layer**
- 10 neurons (represents the final prediction: neurton per one of 10 digits)

```mermaid
graph LR;
    subgraph 784 neurons
        A1(( ))
        A2(( )) 
        A3((..784..)) 
        A4(( )) 
        A5(( )) 
    end

    %% Hidden Layer (128 neurons, only a few shown)
    subgraph 10 neurons
        B1(( )) 
        B2(( )) 
        B3((10)) 
        B4(( )) 
        B5(( )) 
    end

    %% Output Layer (10 neurons)
    subgraph 10 neurons
        C1((0)) 
        C2((1)) 
        C3((2)) 
        C4((3)) 
        C5((4)) 
        C6((5)) 
        C7((6)) 
        C8((7)) 
        C9((8)) 
        C10((9)) 
    end

    %% Connections from Input to Hidden Layer
    A1 --> B1
    A1 --> B2
    A2 --> B2
    A2 --> B1
    A3 --> B3
    A4 --> B4
    A4 --> B5
    A5 --> B5
    A5 --> B4

    %% Connections from Hidden to Output Layer
    B1 --> C6
    B2 --> C7
    B3 --> C8
    B4 --> C9
    B5 --> C10
    B1 --> C1
    B2 --> C2
    B3 --> C3
    B4 --> C4
    B5 --> C5

```
## Results
In my case, I achieved **91%** accuracy!

## Further considerations
- More than single epoch
- Use Mini-Batching approach

For this project, I have opted to keep the implementation straightforward without these optimizations. However, I plan to incorporate them in future projects.

Next, I plan to develop a **plane vs bird classification NN**! Once it's completed, I will drop link here: <...>
