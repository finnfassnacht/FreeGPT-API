# FreeGPT-API
API for the EleutherAI/gpt-neo-125M LLM

This is a simple demo of an API that uses GPT-Neo for text generation. The API is built using Node.js and the Express framework, while the text generation is performed using the Hugging Face implementation of the GPT-Neo 125M model in Python.

This demo is designed to be used on a local area network (LAN) and is meant as a simple showcase of LLMs as a web API.

## installation
To use this demo, you will need to have Node.js, Pyhton3 and Pytorch.

1. Clone this repository and install transformers:
```
git clone https://github.com/finnfassnacht/FreeGPT-API.git
cd FreeGPT-API
pip3 install transformers
```
2. Install Express js
```
npm install express
```
3. VVerify that you can generate text using the GPT-Neo 125M model by running the following command. If GPT-Neo is not already installed, it will be installed automatically:
```
python3 LLM.py 20 "hello"
```
This should generate a response with a maximum length of 20 given the prompt "hello".

## Usage
1. Start the server
```
npm run startserver
```
This will start the server and display the API routes.

Use a web browser to navigate to http://localhost:3000 to access the web interface.

To generate text, type a prompt into the input field and click the "Send" button. The text generated by GPT-Neo will be displayed below the input field.

If you want GPT-Neo to continue the response, click the "Continue" button. The text generated by GPT-Neo will be appended to the existing text.

The generated text will also be displayed in the console of the server.

The API route is
```
http://localhost:3000/api/gpt-neo/maxlength/prompt
```
For example, to generate a response with a maximum length of 20 given the prompt "hello my name is", the API route would be:
```
http://localhost:3000/api/gpt-neo/20/hello my name is
```
The root route serves a simple HTML page for using the web interface.
