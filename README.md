# paperless-gpt-prompts

These are my prompt drafts for paperless-gpt. 

I'm using a self-hosted `ollama` instance with a single RTX3090, currently with `qwen2.5:32b-instruct`(albeit 7b and 14b version works quite good too, just a little bit less reliable), that's where I'm coming from ... right now I'm not using any external API, if I will I will seperate that into different prompt because my ollama prompts are quite large.

DO NOT USE OLLAMA PROMPTS WITH APIS LIMITED IN TOKEN INPUT SIZE - AS THEY COULD BE PRETTY EXPENSIVE!

I have set my default Token size for Ollama to `8092` via the ENV-Var `OLLAMA_CONTEXT_LENGTH` and paperless-gpt's `TOKEN_LIMIT` to `3000` right now ...

Settings a manual default max token size is is quite important because the context-length cannot be defered with the go-versions of langchain and its token-dependency together with Ollama as such it will not be able to calculate any token size itself. So if you don't setup these you will likely get very subpar results or stuck work.

