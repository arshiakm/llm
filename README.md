
# Project Description

This project is designed to fine-tune the GPT-Neo model, a powerful autoregressive language model that emulates the GPT-3 architecture, using a custom dataset potentially containing sensitive or adversarial content. The ultimate goal is to explore the model's capabilities and vulnerabilities in generating text based on both regular and adversarially manipulated inputs. This project includes a step to create adversarial images intended to test the robustness of the model against inputs designed to bypass its safety mechanisms.

### Functionality

The application allows users to:
- Generate text using a fine-tuned GPT-Neo model through a user-friendly web interface.
- Optionally integrate adversarial images with text prompts to see how they influence the generated text.

**What works:**
- Fine-tuning GPT-Neo on a specified dataset.
- Generating text based on user-provided prompts and displaying it in an interactive web app.
- Creating adversarial images to manipulate model outputs.

**What does not work/Not implemented:**
- A fully implemented adversarial image manipulation function integrated seamlessly with the text generation process (requires further development).
- Real-time training or fine-tuning within the web interface is not supported; the model must be pre-trained or fine-tuned prior to deployment.

## How to Clone and Deploy

### Prerequisites
- Python 3.8 or later
- Access to a GPU (preferably with CUDA support to utilize PyTorch optimizations)
- An installed version of PyTorch that supports your GPU
- Gradio installed (for web interface)

### Using the Application

- **Text Input:** Enter a text prompt to generate text.
- **Image Upload:** Upload an image to test adversarial attacks (note: full functionality for adversarial attacks is conceptual and requires additional implementation).
- **Sliders:** Adjust the `Max Length` for generated text and `Temperature` to control the randomness of the output.
- **Generate Text:** Click the button to view the model's output based on the input.

## Functionality Overview

### Fine-Tuning the Model

The model is fine-tuned on a dataset specified by the user, which should contain text that might be considered sensitive or adversarial. This fine-tuning step adapts the model to better understand and generate text under conditions that it might not have encountered during its initial training phase.

### Text Generation

Users can input text prompts and image, and the model generates responses based on these prompts. The responses are influenced by the nature of the model’s training and fine-tuning and images, showcasing how well the model can generate contextually relevant and coherent text.

![image](https://github.com/arshiakm/llm/assets/108753082/4db51bf8-9d50-45b6-8bf3-a212d5e54861)


### Adversarial Image Testing

The code provides a  framework for creating adversarial images that are supposed to manipulate the model’s output by subtly altering the visual input.

## Lessons Learned

This project highlights the importance of rigorous testing, especially when dealing with language models trained on or fine-tuned with potentially sensitive content. The challenges in fully implementing adversarial attacks also underline the need for careful consideration of both the technical and ethical implications of using such models in real-world applications.
