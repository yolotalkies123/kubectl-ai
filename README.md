kubectl-ai is an open-source Kubernetes command-line tool created by Google Cloud that helps users to manage Kubernetes cluster more easily. Instead of typing complex kubectl commands, users can simply describe what they want to do in plain English. The tool uses generative AI to understand the request and then translates it into the right kubectl command. It acts like a translator between human and Kubernetes and makes working with Kubernetes more user-friendly. It’s like having a conversation with the cluster.


**Benefits of kubectl-ai:**

1.Increased productivity
2.Quick troubleshooting
3.Auto YAML generator
4.Saves time

**kubectl-ai supports multiple AI models like:**

1.OPENAI 
2.Locally LLM set up by Ollama 
3.Goodle Gemini
4.Grok

**Prerequisites:**
1.K8s cluster
2.kubectl cli installed and configure the access to the cluster
3.An API key for the model access

**Commands to run:**
1.Install kubectl-ai 

(for Linux)
curl -sSL https://raw.githubusercontent.com/GoogleCloudPlatform/kubectl-ai/main/install.sh | bash
or
(for windows)
download from https://github.com/GoogleCloudPlatform/kubectl-ai/releases/tag/v0.0.12
tar -zxvf kubectl-ai_Darwin_arm64.tar.gz
chmod a+x kubectl-ai
sudo mv kubectl-ai /usr/local/bin/

2.Set up the API key as env variable and use it as:
export GEMINI_API_KEY=your_api_key_here
Note :Get Gemini API key from Google AI Studio.



3.Run kubectl-ai as :
kubectl-ai --model gemini-2.5-pro-exp-03-25

4.Write a prompt for the purpose like:

egs:
1.create a deployment named nginx with 3 replicas using the nginx:latest image
2.list all pods in the default namespace
3.expose the deployment nginx with LoadBalancer service

**Special keywords:**
model: To list the current selected model.
models: To list all available models.
version: To display the kubectl-ai version.
reset: To clear the conversational context.
clear: To clear the terminal screen.
exit or quit: To terminate the interactive shell.




