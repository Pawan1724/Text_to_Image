# Stable Bud - AI Image Generator

## Overview
Stable Bud is a simple AI-powered image generator using Stable Diffusion. It provides a user-friendly interface built with Tkinter and CustomTkinter, allowing users to generate images from text prompts.

## Features
- User-friendly GUI with a modern dark theme.
- Uses Stable Diffusion to generate images from text input.
- Displays generated images within the application.
- Saves generated images automatically.

## Requirements
Ensure you have the following installed:
- Python 3.7+
- `torch`
- `diffusers`
- `tkinter`
- `customtkinter`
- `Pillow`

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Pawan1724/Text_to_Image
   cd StableBud
   ```
2. Install dependencies:
   ```bash
   pip install torch diffusers customtkinter pillow
   ```
3. Replace `auth_token` in the script with your Hugging Face API key.

## Usage
Run the application with:
```bash
python image_gen.py
```
1. Enter a text prompt in the input field.
2. Click the "Generate" button.
3. The generated image will appear in the application window and be saved as `generatedimage.png`.

## Model Details
- Model: `CompVis/stable-diffusion-v1-4`
- Backend: `torch`
- Default Device: `CPU`


## License
This project is licensed under the MIT License.

## Author
Pawan Kumar Salikanti

