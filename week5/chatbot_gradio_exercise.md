### Chatbot Gradio Exercise
In this exercise, we will build a chatbot from the ground up, step-by-step

#### Prerequisites
* Groq API key. Use this name: GROQ_API_KEY
* Gemini API key. Us this name: GEMINI_API_KEY
* Huggingface API key. User this name: HF_ACCESS_TOKEN

Add these keys to your Google Colab Secrets manager:

1. Open your Google Colab notebook and click on the 🔑 **Secrets** tab in the left panel.
   
   <img src="https://storage.googleapis.com/generativeai-downloads/images/secrets.jpg" alt="The Secrets tab is found on the left panel." width=50%>

2. Create a new secret with the name `GOOGLE_API_KEY`.
3. Copy/paste your API key into the `Value` input box of `GOOGLE_API_KEY`.
4. Toggle the button on the left to allow notebook access to the secret.

Detailed instructions are [here](https://colab.research.google.com/github/google-gemini/cookbook/blob/main/quickstarts/Authentication.ipynb)
  

#### Instructions
* Make a copy of this [Colab notebook](https://colab.research.google.com/drive/1bjOOI5sNbP10hclqdyKWCv8_TcxFS7Q7?usp=sharing)

##### Step 1 - add the label
Copy the code below and paset under step 1 on your colab note book
```
gr.Label("Welcome to UCSC Ext Chatbot", color="orange")
```
Now return the cell to see the changes

##### Step 2 - add the system prompt and llm provider
Copy the code below and paset under step 2 on your colab note book
```
with gr.Row():
   system_prompt = gr.Textbox("You are helpful AI.", label="System Prompt")
   llm_provider = gr.Radio(["Groq", "Gemini"], type="value", label="Provider", value="Groq")
```
Copy the code below and paste below the additional input area
```
   system_prompt,
   llm_provider,
```

Re-launch the chatbot Gradio application by re-run the cell

##### Step 3 - add the temperature and max_tokens
Copy the code below and paset under step 3 on your colab note book
```
   with gr.Row():
      temperature = gr.Slider(0,1, minimum=0, maximum=1.0, step=0.1, value=0.5, label="Temperature")
      max_tokens = gr.Slider(label="Max Tokens", minimum=300, maximum=1000, value=500)
```
Copy the code below and paste below the additional input area after llm_provider
```
   temperature,
   max_tokens,
```

Re-launch the chatbot Gradio application by re-run the cell

##### Step 4 - replace the random_response with the following
```
def random_response(message, history, system_prompt, llm_provider, temperature, max_tokens):
    print(f"system_prompt: {system_prompt}")
    print(f"llm_provider: {llm_provider}")
    print(f"temperature: {temperature}")
    print(f"max_tokens: {max_tokens}")
    return random.choice(["I understand", "You are kidding right?"])
```
Re-run the cell and then re-run the chatbot app cell
