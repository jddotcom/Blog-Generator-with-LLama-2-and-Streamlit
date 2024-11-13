# Blog Generator with LLama 2 and Streamlit

This project is a **blog generation application** built using **Streamlit** and **LLama 2** (through `CTransformers`). It allows users to generate AI-written blog content for different job profiles based on a specific topic, desired word count, and writing style.

---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Setup and Installation](#setup-and-installation)
- [How to Use](#how-to-use)
- [Components](#components)
- [Future Improvements](#future-improvements)
- [License](#license)

---

## Overview
This application uses the **LLama 2 language model** to generate blog content. By leveraging the power of language models, it aims to create blog posts based on custom input parameters like job role (e.g., "Data Scientist" or "Researcher") and topic. The app is built with **Streamlit** to provide a clean and interactive user interface for inputting parameters and viewing the generated content.

## Features
- **Customizable Blog Topic**: Specify any blog topic as the main theme.
- **Adjustable Word Count**: Set the approximate word count for the generated content.
- **Job Profile-Oriented Writing Styles**: Choose a writing style for specific audiences (e.g., Data Scientists, Researchers, or general readers).
- **Interactive UI**: User-friendly interface powered by Streamlit, providing a seamless blog generation experience.

## Setup and Installation

### Prerequisites
- Python 3.7 or higher
- Streamlit
- `langchain`
- `CTransformers` (for running LLama models)

### Step-by-Step Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/blog-generator-llama.git
   cd blog-generator-llama
   ```

2. **Install Required Libraries**
   Use the `requirements.txt` file to install all necessary dependencies.
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the LLama 2 Model**
   Download the **LLama 2** model file `llama-2-7b-chat.ggmlv3.q8_0.bin` and save it in a `models` folder within the project directory.

4. **Run the Streamlit App**
   Start the Streamlit app with the following command:
   ```bash
   streamlit run app.py
   ```

   This will open a local server, where the app can be accessed at `http://localhost:8501`.

---

## How to Use

1. **Enter Blog Topic**: Input the main topic for the blog.
2. **Specify Word Count**: Enter the desired word count (approximate).
3. **Choose a Writing Style**:
   - Select the job profile for which the blog is being written (e.g., "Data Scientist", "Researchers", or "Common People").
4. **Generate**:
   - Click the **Generate** button to initiate the blog generation process.
5. **View Output**:
   - The generated blog will appear on the interface.

---

## Components

1. **LLama Model Setup** (`CTransformers`):
   - The model is initialized using the `CTransformers` library, loading the LLama 2 model from the local file. Parameters like `max_new_tokens` and `temperature` are configured to control the response output.

2. **Prompt Template**:
   - A prompt template in `langchain` is used to structure the input parameters into a cohesive query for the LLama 2 model, asking it to generate content as per topic, word count, and job profile style.

3. **Streamlit UI**:
   - Streamlit provides an interactive front-end where users can input data for topic, word count, and profile style, and view the model’s output directly.

---

## Future Improvements
- **Add More Customization**: Include options for tone (formal, casual, etc.), more specific topics, or target audience types.
- **Enhanced NLP Processing**: Add NLP pre-processing to better handle grammar and style refinement.
- **Real-Time Preview**: Provide a live preview of generated content as parameters are changed.
- **Expanded Model Support**: Integrate support for other generative models beyond LLama 2 for additional stylistic options.

---

## License
This project is open-source and available under the MIT License. 

Feel free to contribute to the project or use it as a base for your own generative AI applications.
