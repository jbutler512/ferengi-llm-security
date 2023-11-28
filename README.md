## open ai api key required
  - https://platform.openai.com/docs/overview
  - In .env add:
  - OPENAI_API_KEY='<API KEY>'
  - If you get authentication errors, or main doesn't run, hardcode the key into common/chat_app.py:
    -openai.api_key = '<API KEY>'



## Setting up the environment:
  - Launch anaconda navigator
  - Launch VSCode through the navigator
  - In VSCode terminal create a conda environment with python version 3.11.5 and pip:
  - conda create -n <env_name> python=3.11.5 pip


## Activate environment:
  - conda activate <env_name>
  - pip install -r requirements.txt python-dotenv
  - pip install -r requirements.txt
  - pip install python-dotenv
  - Create .env file


## To run the code:
  - python main.py

# Our goal:

- In the original codebase, main tests scenarios that 'pass' when the model initialized as a digital assistant is polluted by a prompt injection.
- We wanted to introduce a way that the scenarios would 'fail' without hampering the functionality of the assistant.
- The most effective method that we discovered was to introduce a 'vigilant prompt' during the assistant's initialization.
- The vigilant prompt further specifies the behavior that the assistant is meant to exhibit.
- The demo shows how an LLM-integrated application can be protected with a simple implementation of a vigilant prompt.
- Depending on the application's purpose, the vigilant prompt can be tailored for specific use cases.

Experiment: Remote control
#Added prompt to user

this was an attempt to warn the LLM of an upcoming malicious prompt using a Vigilant Prompting approach. 
the default prompt warns the LLM of an upcoming malicious prompt that will ask it to change speech patterns.

Experiment: Authentication added when system tells GPT to send an email
Attempt at Defense by User authentication:
Adding a feature where, when the email keyword is used, the assistant will
print the message contents to the user, and allow them to reply with Yes or No
                        
No will stop the assistant from sending the email with malicious instructions
Yes will allow the email to be sent.
Block: this caused the program to exit as intended with the no keyword
however, the yes keyword also caused the scenerio to fail due to unforseen complexities.


