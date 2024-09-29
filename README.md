Consolidated list of quick guides to get started with using ai tools you can use locally in your laptop without paying any subscription fee 

## Quick Guide to run chatgpt like interface in your laptop


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

**Step 5 : Access open-webui using following link**

http://localhost:3000/auth

Following instructions in the web application to signup for an account and start  using the application


**Reference Links**

[https://hub.docker.com/r/ollama/ollama](https://hub.docker.com/r/ollama/ollama)

[https://github.com/open-webui/open-webui](https://github.com/open-webui/open-webui)

