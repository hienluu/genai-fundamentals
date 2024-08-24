## Authenticating GenAI Applications with LLM Model Providers from Colab

Access tokens or API keys are preferred way to authenticate an application with LLM model providers. 
When sending prompts to these provides, the tokens or keys are included in the request.  
The LLM model providers use the provided the token or key to determine whether to accept or reject the requests.

This document outline the steps to create an access tokens on [Hugging Face](https://huggingface.co/) and securely store it 
in a google colab.

#### Prerequisites
* Create an account on [Hugging Face](https://huggingface.co/) if you don't already have one
* In order to use (Google Colab for free)[https://colab.research.google.com/], you would need a Google acount,
so create one if you don't already have one

#### Create Access Token on Hugging Face](https://huggingface.co/)
* Log into Hugging Face and click on your [profile](https://huggingface.co/settings/profile)
* Click on the ["Access Tokens"](https://huggingface.co/settings/tokens) area on the left hand menu
* Click on the "Create New Token" button on the upper right hand
* On the "Create new Access Token" page, click on the ("Read")[https://huggingface.co/settings/tokens/new?tokenType=read] option under "Token Type"
  * Enter a name (any name, i.e my_colab) into the text box and then click on the "Create token" button
  * On the "Save your access token" dialog box, click on the "Copy" button to copy the newly created token to your clipboard
  * Paste the copied access token into a text file or somewhere on your computer
    * (because you will not be able to see the access token value again)
   
#### Securely store the Hugginf Face access token on Google Colab
