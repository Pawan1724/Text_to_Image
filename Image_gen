import tkinter as tk
import customtkinter as ctk
from PIL import Image, ImageTk

auth_token="HUGGING_FACE_API"#Your Hugging Face API TOKEN Key

import torch
from diffusers import StableDiffusionPipeline

# Create the app
app = tk.Tk()
app.geometry("532x632")
app.title("Stable Bud")
ctk.set_appearance_mode("dark")

# Create input field
prompt = ctk.CTkEntry(app, height=40, width=512, font=("Arial", 20), text_color="black", fg_color="white")
prompt.place(x=10, y=10)

# Create label for displaying image
lmain = ctk.CTkLabel(app, height=512, width=512)
lmain.place(x=10, y=110)

# Load model
modelid = "CompVis/stable-diffusion-v1-4"
device = "cpu"
pipe = StableDiffusionPipeline.from_pretrained(modelid, torch_dtype=torch.float32, token=auth_token)
pipe.to(device)

def generate():
    prompt_text = prompt.get()
    if not prompt_text:
        return  # Prevents empty input from crashing the program
    
    # Generate image
    image = pipe(prompt_text, guidance_scale=8.5).images[0]
    
    # Save and display image
    image.save("generatedimage.png")
    img = ImageTk.PhotoImage(image)
    lmain.configure(image=img)
    lmain.image = img  

# Create Generate button
trigger = ctk.CTkButton(app, height=40, width=120, font=("Arial", 20), text_color="white", fg_color="blue", text="Generate", command=generate)
trigger.place(x=206, y=60)

app.mainloop()
