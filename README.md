# n8n

The setup in the current project uses a local n8n instance as well as a local GPT4All instance.

## Workflow

![workflow](images/workflow.png)

## Chat

![chat](images/chat.png)

## Setup

* install GPT4All
* GPT4All enable local API server
* install model qwen2.5-coder-1.5b-instruct-q4_0.gguf in GPT4All
* install socat ```sudo apt install socat```
* start socat ```socat TCP-LISTEN:4892,fork,reuseaddr TCP:127.0.0.1:4891```
* create n8n in /home/<user>
* start Docker ```docker-compose up```
* replace webhookUrl in chat.html with value from trigger node
* open chat.html in browser

## Improvments

* Error handling in workflow
* Support for multiple files to extract