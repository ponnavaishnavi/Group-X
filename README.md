# 📚 **Explainify – Text-to-Visual Learning AI**

**🚨 *Problem Statement*** 

Learning complex topics from textbooks, lecture notes, or research papers can be challenging and time-consuming 😩. Most resources rely heavily on text, which:

Can be hard to understand for visual learners 🧠👀

Leads to low retention of important concepts 📉

Requires students to spend extra time summarizing and visualizing key points ⏳

There’s a need for a smart, automated solution that can convert textual lessons into visually engaging, easy-to-understand videos 🎬✨ — making learning faster, fun, and more effective.

**💡 *Initial Solution***

Explainify transforms any text lesson into a visual + audio learning experience. Here’s how it works:

**📝*Text Processing***

Input: any lesson, paragraph, or notes.

Automatically splits text into key scenes or sentences using NLP 🔍.

**🖼 *Visual Generation***

Generates realistic AI images for each scene (DALL·E, Stable Diffusion) 🎨🤖

Adds animations like zoom-in, fade, or slide transitions ✨🎞

**🎤 *Audio Narration***

Converts text to speech using TTS technology 🔊

Synchronizes narration with visuals for smooth comprehension 🎧

**🎬 *Video Composition***

Combines images, audio, and animations into a ready-to-watch video 🖥📹

Adds titles, captions, and subtitles to highlight key concepts 🏷📌

***Outcome:***
A fully automated educational video that turns boring text into a dynamic, engaging learning experience 🚀💡.
Students can understand faster, remember longer, and enjoy learning like never before 🎯📖✨

🌟 **How Explainify Works – Visual Flow**

📄 Text Lesson / Notes

        │
        ▼
        
🧠 NLP / Text Processing
   (Split into scenes / key sentences)
   
        │
        ▼
        
🖼 AI Image Generation
   (DALL·E / Stable Diffusion / Stock Images)
   
        │
        ▼
        
🎤 Text-to-Speech Audio
   (Narration for each scene)
   
        │
        ▼
        
🎞 Video Composition
   (Animations, transitions, titles, captions)

        │
        ▼
        
🚀 Final Explainify Video
   (Engaging, visual + audio learning experience)
   
        │
        ▼
        
📚 Students Understand Faster & Retain Longer

## 👥 Team Roles and Work Allocation

***1️⃣ Text Processing & NLP***

Role: Convert raw text into structured scenes
Tasks:

Take the input lesson/text.

Split the text into scenes or sentences using NLP (nltk / spacy).

Optionally summarize or highlight key points per scene.

Output scene-wise text for image and audio generation.

Tools:

Python, NLTK (sent_tokenize), SpaCy (optional), Pandas (optional for scene storage)

Deliverables:

A list of scene texts ready for images and narration.

Example: ["Photosynthesis converts sunlight into energy", "It occurs in chloroplasts", ...]



***2️⃣ Image Generation***

Role: Generate visual representation for each scene
Tasks:

Take scene texts from Member 1.

Use AI image generation or free stock images.

Options: OpenAI DALL·E, Stable Diffusion, Unsplash API

Save images locally (scene_1.png, scene_2.png, etc.)

Optional: Apply simple overlays or text highlights on images.

Tools:

Python, OpenAI API, Requests, PIL (Pillow)

Image editing software (optional)

Deliverables:

Scene images ready for video composition

***3️⃣ Audio Narration + Scene Video Clips***

Role: Create audio narration and merge with images for each scene
Tasks:

Take scene texts from Member 1.

Generate TTS audio for each scene (gTTS or ElevenLabs).

Combine scene image + narration into a short video clip.

Add scene titles / captions / small animations (zoom, fade, crossfade).

Tools:

Python, gTTS, MoviePy, PIL (for text overlays)

Deliverables:

Individual scene video clips (scene_1.mp4, scene_2.mp4, …)

***4️⃣ Video Compilation & Final Rendering***

1.Role: Combine all scene clips into a final video
Tasks:

Take all scene clips from Member 3.

Apply transitions between scenes (crossfade, fade-in/out).

Add background music or final audio enhancements (optional).

Export final Explainify video (explainify_ai_video.mp4).

Tools:

Python, MoviePy, FFMPEG (optional)

Deliverables:

Final complete video ready for download or presentation

***🧠 How It Works (Step-by-Step)***

## Step-1:🧾 Text Extraction from Multiple File Formats

This Google Colab project allows you to upload a file and automatically extract text from various file formats — including .txt, .pdf, .docx, .csv, .json, .pptx, and even image files (.png, .jpg, .jpeg) using OCR.

•	***Upload the file:***
The script uses google.colab.files.upload() to let you upload any supported file.

•	***Detect file type:***
Based on the file extension, it decides which extraction method or library to use.

•	***Extract text:***
Reads or processes the file:

           .txt: Simple read

           .pdf: Uses PyMuPDF (fitz)

           .docx: Uses python-docx

           .csv: Uses pandas

           .json: Uses json and pprint

           .pptx: Uses python-pptx

           .png / .jpg / .jpeg: Uses pytesseract and Pillow for OCR

•	***Display the extracted text:***
Shows the extracted text inside a formatted HTML block for easy reading.

Displays a message if no text is found.

## 🚀 Features:

📄 Extract text from Word, PDF, and TXT files

📊 Read and display CSV and JSON data

🎞️ Capture text from PowerPoint (.pptx) slides

🖼️ Perform OCR (Optical Character Recognition) on images

⚙️ Automatically detects file type and uses the right extraction method

🧠 Built for Google Colab — no local setup required
## Step-2: 🎬 AI Explainer Video Pipeline (Female Voice) – Colab

Create *automated explainer videos* from documents or images with a *female voice narration* — fully in *Google Colab*!  

---

## ✨ Features
- 📄 Supports multiple file types: .txt, .pdf, .docx, .csv, .json, .pptx, .png, .jpg, .jpeg  
- 📝 Summarizes long text using *Facebook BART Transformer*  
- 🎤 Generates *female-like voice narration* using *gTTS*  
- 🖌 Creates a simple *background image* for the video  
- 🎥 Combines *audio + image* into a downloadable .mp4 video  
- ⬇ Direct download link in Colab  

---

## 🚀 Workflow
1. *Upload File* – Upload your document or image 📁  
2. *Extract Text* – Automatically detects file type and extracts content ✂  
3. *Verify Text* – Displays extracted content for review 👀  
4. *Summarize Text* – Creates a concise summary using AI 🤖  
5. *Convert to Audio* – Generates female voice narration 🎧  
6. *Create Background Image* – Adds a simple colored background with text 🖼  
7. *Generate Video* – Combines image + audio into .mp4 video 🎬  
8. *Download Video* – Provides a direct download link 💾  

---

## 📦 Dependencies
- transformers, torch – Text summarization 🧠  
- gTTS – Text-to-speech conversion 🎤  
- moviepy – Video creation 🎞  
- pillow – Image processing 🎨  
- pymupdf, python-docx, python-pptx, pytesseract – Text extraction from files 🗂  

---

## 📝 Usage
1. Open the notebook in *Google Colab* 🌐  
2. Upload your file when prompted 📤  
3. Wait for the pipeline to extract, summarize, generate audio, and create the video ⏳  
4. Download your final *explainer video* 🎥⬇  

---
## Step-3: Image Generation
🧠 Description of the Work

This code uses Stable Diffusion, a powerful AI image generation model, to create realistic images from text prompts using Python.

🔍 **Step-by-Step Explanation**

Installing Dependencies

- *!pip install -q diffusers transformers accelerate torch pillow*


Installs all the required libraries:

diffusers → to load and run diffusion models

transformers → for text encoding

accelerate → for efficient GPU computation

torch → PyTorch framework for deep learning

pillow → for image processing and saving

Importing Required Modules

- *from diffusers import StableDiffusionPipeline
import torch*


Imports the AI model pipeline (StableDiffusionPipeline)

Imports PyTorch for GPU and tensor operations

Checking GPU Availability

- *print("GPU Available:", torch.cuda.is_available())*


Confirms whether a CUDA-enabled GPU is available for faster image generation.

Loading the Pre-trained Model

- *pipe = StableDiffusionPipeline.from_pretrained(
    "runwayml/stable-diffusion-v1-5",
    torch_dtype=torch.float16,
    safety_checker=None
).to("cuda")*


Loads the Stable Diffusion v1.5 model (by RunwayML).

Uses half precision (float16) for faster inference.

Moves the model to the GPU for acceleration.

Disables safety checker (optional in local usage).

Generating the Image

- *prompt = "dogs"
- image = pipe(prompt, num_inference_steps=30).images[0]*


The model converts the text prompt into an image.

num_inference_steps controls the quality (more steps → higher quality).

Displaying and Saving the Output

- *display(image)
- image.save("my_image.png")*


Shows the generated image in the output window.

Saves it locally as my_image.png.

🎨 **Example Output**

If the prompt is:

"Dogs"

The model will create a scientific visual showing dogs in the picture.

⚙️ **Purpose**

This demonstrates how text-to-image generation works using AI models. It can be used for:

- Educational visualizations

- Creative content generation

- Design prototypes

- Data visualization in AI projects
