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
   
#### Securely store the Hugging Face access token on Google Colab
* Go to [Google Colab](https://colab.research.google.com/)
* Click on the "Key" icon on the left most side of the page to open up the "Secrets" area
  * Each secret has a name and a value (key-value pair)
* Click on the "Add new secret" link
  * Enter HF_ACCESS_TOKEN as the name of the secret
  * Paste the Hugging Face access token value into the Value field
  * Enbable "Notebook access" by clicking on the empty area next to the "x" mark (left most field of the secret)
* Now close the the Secrets page by clicking on the "X" at the top right area of the "Secrets" area.

#### Accessing the secret inside a Colab
* To access a secret inside colab via Python
```python
from google.colab import userdata
userdata.get('secretName')
```
* A popup will show up to ask you to grant access to a secret when those lines of code are executed in colab

##### Have fun
