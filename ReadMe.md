# Replit Code
This is a simple web application that generates code based on user input. It uses a language model API built with Flask and the transformers library from Hugging Face.

# Usage
To use the code generator, follow these steps:

<ol>
    <li>Enter your input code in the "Input Code" text area.</li>
    <li>Click the "Generate Code" button..</li>
    <li>Wait a few seconds for the generated code to appear.</li>
</ol>

# Technical Details
The code generator is built using the following technologies:
<ul>
    <li><b>Flask</b>: a Python web framework used to build the API.</li>
    <li><b>transformers</b>: a Python library from Hugging Face that provides state-of-the-art pre-trained models for natural language processing tasks, including language generation.</li>
    <li><b>HTML, CSS, and JavaScript</b>: used to build the web frontend.</li>
</ul>

The API is hosted on http://127.0.0.1:5000/generate_code and accepts POST requests with a JSON payload containing the input code. The response is a JSON object containing the generated code.

# Running Locally
To run the code generator locally, follow these steps:
<ol>
    <li>Clone this repository.</li>
    <li>Install the required dependencies: <code> pip install -r requirements.txt</code></li>
    <li>Start the Flask server: <code>python app.py</code></li>
    <li>Open <code>index.html</code> in your web browser.</li>
</ol>

Note that you may need to modify the API endpoint URL in index.html to match the address of your locally running Flask server.

# Model Details
The language model used in the code generator is the <code><i>replit/replit-code-v1-3b</i></code> model from [Hugging Face](https://huggingface.co/). This model was fine-tuned on a large dataset of code snippets and is capable of generating high-quality code based on user input.

The model is used in conjunction with a tokenizer, which is responsible for converting the input code into a format that the model can understand. In this case, we use the AutoTokenizer class from the transformers library to automatically select the appropriate tokenizer for the replit/replit-code-v1-3b model.

The generated code is produced using the <code>generate()</code> method of the AutoModelForCausalLM class, which performs language generation using the replit/replit-code-v1-3b model. The generate() method takes various parameters, such as max_length, top_p, and temperature, which control the behavior of the language generation process.
