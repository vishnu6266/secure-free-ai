## Access private chatgpt application from your mobile browser hosted in your mac

Access private chatgpt application in your mobile device for free. Setup the 

**Step 1 : Install Docker**

Download and install Docker from the link https://www.docker.com/get-started/

**Step 2 : Run ollama locally**

<code> docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama </code>

**Step 3: Download model**

Check the model library and make sure you have enough RAM in the machine to run the model that you select

[ollama model library](https://github.com/ollama/ollama?tab=readme-ov-file#model-library)


<code>docker exec -it ollama ollama run llama3</code>

**Step 4 : Run open-webui locally**

<code> docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main </code>

**Step 5 : Find IP address of your mac**

Run following command in your mac to get the IP address 

<code>ipconfig getifaddr en0 en1</code>

**Step 6 : Access the application from your mobile browser**

Use the IP from above step to access the application.

Following is an example URL 

http://192.168.1.4:3000/

Following instructions in the web application to signup for an account and start  using the application


**Additional Commands**

To list all models

<code>docker exec -it ollama ollama list</code>

To remove a model

<code>docker exec -it ollama ollama rm llama3:latest</code>


**Reference Links**

[https://hub.docker.com/r/ollama/ollama](https://hub.docker.com/r/ollama/ollama)




