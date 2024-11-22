# LLMs for Web Developers
*Roy Derks*

* About
  * @gethackteam
  * IBM (Granite AI model)
  * Book author, conf speaker
  * royderks/ai-web-workshop (github)
* AI Today
  * ChatGPT
  * Can run in-app (VS Code, ChatGPT on airplane mode, etc)
  * Changed how devs write code
* Code Assistants
  * Mock data
    * Multi-lingual!
  * Write tests
  * Optimize code
  * generate new code
  * debug
* "You don't have to be a data scientist to build AI apps"
  * Latent Space podcast
  * Making use of foundation models (LLMs)
* Ways to extend models
  * LLM provider
  * API on local machine (running model)
  * LangChain (way to abstract extensions on top of other models), OpenAI, watsonX
* Prompt Engineering
  * Process of (re)structuring text to be better understood by AI
  * Question -> prompt (question + instructions) -> LLM -> answer
  * LangChain/"MyGPT" demo example
    * Temperature: how deterministic a model will be
  * Zero-shot prompt ex: "Take the role of a personal travel assitant; {question}"
  * Few-shot prompt 
    * Providing examples to LLM when asking question
  * Others
    * chain of thought prompting
    * self-consistency
    * tree of thoughts
    * ReAct prompting (what agents use)
    * Look at model guard(sp?)
      * Helps provide syntax to prompts
  * promptingguide.ai
* Dynamically provide LLM with add'l context
  * RAG = retrieval augmented generation
    * question -> embeddings -> search in vector db -> prompt -> LLM -> answer
  * Vector database
    * chunking into smaller datasets -> store in vector db -> retrieve using semantic search
    * Unstructured (startup)
    * Brahma(?) vector db
  * Embeddings
    * TensorFlowEmbedding -> use with LangChain
  * Context
    * Helpful for using custom LLM implementations using custom data
    * Prevents reliance on training data or hallucinations
  * Libraries
    * LangChain has built in libs
* RAG not the only way to make LLMs context aware
  * Long context windows
  * Train or fine-tune model (but logn and expensive)
* AI Agents
  * Agents to do all sorts of things
  * Companies providing agents to customers
  * Ex stripe providing agents to help users create APIs/integrations
  * Question -> ? -> Answer
    * Q -> Think/plan | (Re)Act | LLM <-> tools (vector db, data, APIs) --> answer
  * Tool calling
    * Import from web
    * Create own tools
    * Ex tool to query Wikipedia
* Future: building autonomous agents
* Materials
  * ibm.com/watsonx/developer
  * coursera.org/professional-certificates/applied-artificial-intel. ibm-watson-?
* Q&A