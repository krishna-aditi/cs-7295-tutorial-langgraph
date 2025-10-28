# CS 7295 Data Viz and GenAI - Tutorial on LangGraph and Agentic AI tools 
Before the class, please complete the following setup steps to ensure you can run all the code examples during class.

## 1. Environment Setup
Create a dedicatedConda environment for this tutorial:
```
# Create a new environment named 'cs7295-tutorial' with Python 3.11
conda create -n cs7295-tutorial python=3.11

# Activate the environment
conda activate cs7295-tutorial
```

Install required packages:
- Create a **requirements.txt** file with the following content
```
streamlit
pandas
langgraph
langchain-core
langchain-openai
matplotlib
seaborn
python-dotenv
```

Run the following command in the terminal:
```
# Install package with pip command
pip install -r requirements.txt
```

## API Key
First, create your OpenAI API key [here](https://platform.openai.com/api-keys), and save the key in a secure location. 

Create a project directory for the tutorial (where you are going to create your Python files for the tutorial). In the directory, create a **.env** file. 

Open the **.env** file in any text editor and add the following. Then save the file: 
```
OPENAI_API_KEY=sk-proj-your-actual-api-key-here
```

**NOTE:**
- No spaces around the = sign
- No quotes around the API key
- Replace sk-proj-your-actual-api-key-here with your actual OpenAI API key that you created

## Loading the API key to your code
Here is the code with which you can verify that your API key is loaded:
```
from dotenv import load_dotenv
import os
# This loads the .env file
load_dotenv()  

# Get the API key (For verification)
api_key = os.getenv("OPENAI_API_KEY")
print(f"API Key loaded: { api_key }")
```
