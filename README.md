Setup backend
Change directory into backend

cd chatbot/backend
Setup virtual environment
Create a Virtual Environment

python3 -m venv venv
Activate Virtual Environment (MAC)

source venv/bin/activate
Activate Virtual Environment (Windows)

source venv/Scripts/activate
Upgrade PIP

pip3 install --upgrade pip
Install Python packages
Install required Python packages

pip3 install openai python-decouple fastapi "uvicorn[standard]" python-multipart
Or use this alternative method (although this alternative method might not work if using Windows)

pip3 install -r requirements.txt
Create Environment Variables
Create your .env file

touch .env
Update your .env file with the following. You can see your .env by typing sudo nano .env or just by clicking on the file if you are in VS Code.

OPEN_AI_ORG=enter-you-key-here
OPEN_AI_KEY=enter-you-key-here
ELEVEN_LABS_API_KEY=enter-you-key-here
Start your backend server
Start your backend server

uvicorn main:app
Alternatively, you can ensure your server resets every time you make a change by typing:

uvicorn main:app -- reload
You can check your server is working by going to:

http://localhost:8000/health
Setup frontend
Change directory into frontend

cd ..
cd chatbot/frontend
Install packages

yarn --exact
Build application

yarn build
Start server in dev mode

yarn dev
You can check your dev server is working by going to:

http://localhost:5173/health
or alternatively in live mode:

yarn start
You can check your live server is working by going to:

http://localhost:4173/health
