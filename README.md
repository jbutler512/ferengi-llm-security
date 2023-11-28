open ai api key required
  https://platform.openai.com/docs/overview
  In .env add:
  OPENAI_API_KEY='<API KEY>'
  If you get authentication errors, or main doesn't run, hardcode the key into common/chat_app.py:
    openai.api_key = '<API KEY>'



Setting up the environment:
  Launch anaconda navigator
  Launch VSCode through the navigator
  In VSCode terminal create a conda environment with python version 3.11.5 and pip:
  conda create -n <env_name> python=3.11.5 pip


Activate environment:
  conda activate <env_name>
  pip install -r requirements.txt python-dotenv
  pip install -r requirements.txt
  pip install python-dotenv
  Create .env file


To run the code:
  python main.py

