**Automate process locally in your mac usin n8n**

Step 1 : Install Docker

Download and install Docker from the link https://www.docker.com/get-started/

Step 2 : Run ollama locally

 docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama 

Step 3: Download model

Check the model library and make sure you have enough RAM in the machine to run the model that you select

[ollama model library](https://github.com/ollama/ollama?tab=readme-ov-file#model-library)

<code>docker exec -it ollama ollama run llama3</code>

