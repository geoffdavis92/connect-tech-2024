# BYOM Ai Model with TensorFlow.js

*Gant Laborde — 11/18/2024*

* Learning TensorFlow.js
* Popular AI
  * 4k TensorFlow ML models in prod at Google
  * "Code is reflective of the people who coded it"
  * "What if we had a system where you didn't teach program what to do, but the machine figured out characteristics of X action/Y behavior/Z content/etc?"
  * Machines _have_ to give you an answer
* Text gen
  * Chat GTP
  * Gemini (Google)
  * Llama 3 (Meta)
  * Claude 3 (Anthropic)
  * Perplexity
  * MM1 (apple)
  * Titan (Amazon)
  * Grok (Musk)
  * Copilot (Microsoft)
  * CodeWhisperer (Amazon's ev AI)
  * Tabnine (Copilot competitor)
  * Jasper (mktg)
  * Mistral AI
* Generative Images
  * Midjourney
  * Dall-E (OpenAI)
  * Adobe Firefly
  * Stable Diffusion (best)
  * Getty iStock
  * Synthesia
  * Sora
  * Runway
  * Pika
* Other popular AI
  * ElevenLabs
  * Suno
  * Voice.ai
  * AIMastering.com
  * Lalal.ai (remove instrument from music)
* What is ML
  1. We don't program
  1. We create tests
  1. Machines learn
  * "Generative AI is the more popular use case"?
    * For right now, yes
* Buckets
  * Narrow AI (most of what we know right now)
    * Object detection
      * NSFW.js
    * Tracking (ex sports, security video)
    * Person detection
    * Face detection
      * Sentiment analysis (enjoy the show demo)
      * CageFace
    * Face mesh
    * Pose detection (ex counting exercises for physical therapy)
    * Scan documents
    * Language (id'ing languages, entity extraction)
  * General AI (ex: Terminator, aka what everyone's afraid of)
* The Future
  * Combo of AI models workign in concert to give excellent CX
  * "Where are the models?"
    * ModelZoo (google search)
    * HuggingFace 
* Why Neural?
  * Compared to brain neurons
  * Synapses
    * dense
    * vary thickness/cxns
    * Certain amount of electricity req'd
  * Network examples
    * XOR (exclusive OR)
    * 5 node networks
      * w=weight
      * b=bias
      * a=activation (sigma fxn)
      * Why does 1 <XOR> 0 not equal out to 1? (or 0?)
        * Fuzzy
        * Always rounding
      * Linear algebra
    * GPU speed
      * CPU vs GPU
      * speed vs efficiency(?)
      * Matrix math– majority can be cached!
      * GPU can be utilized to batch intense calculations
* How to choose weight/bias/activation?
  * Model's parameters
  * Nodes = network structure
  * Answer: training
  * figuring out which numbers to input to get answers
  * Iris example
    * Initial runs = truly random answer
    * Use feedback, back propagation (machine training itself), re-test
    * "ML training = showing machine flashcards"
  * My understanding:
    * Have a use case
    * Have some examples of correct answers
    * Use platform/library to guess write answers/correct itself until output matches (to certain %) known answers
* Math from scratch? No
  * For math by hand? do course: TBD
  * TensorFlow (Lite, JS - versatile, scalable)
  * PyTorch ("way cooler for people")
  * playground.tensorflow.org
    * clean data is important
    * data with bias/no bias will be reflected in models
    * epoch = iteration of model training (forwards and backwards)
    * numbers goes in, number comes out
      * text, numbers, videos = concepts that layer on top 
* Let's build a model
  * TeachableMachine
  * https://teachablemachine.withgoogle.com/
  * Eye tracking: screen quadrant/glasses or no glasses
  * Hoodie: hood up or down
  * Why are these models unusable in production?
    * Bias
* Solving FizzBuzz with AI/ML
  * FizzBuzz-Consume repo
  * Cursor ai code editor
    * Can index website (ex: indexed TensorFlow.js docs site)
  * Tensors
    * Wrapper around input fed to model
    * Built using
      * Scalar
      * Vector
      * Matrix
    * Need to understand what to use when building models for X solution
    * "Shape" of tensor
  * Models require input the same shape as how it was trained on

(Break)

* Visual data
  * MNSIT data set 
  * https://adamharley.com/nn_vis/
  * Pull out image components (edges, curvature, etc)
    * ML chooses best filters to use when generating models
    * Convolution = filter created/used by ML
    * MaxPooling = most activated pixels, picked out
    * Soft max = numbers will add up to 1
    * Confusion matrix
      * Y = labels = correct answers
      * X = predictions = initial (untrained) model output
      * "Evaluation" stage of RPS demo
    * Loss fn = how "wrong" the model is
      * During training, will go closer to 0
      * Means the model is learning, architecture works
      * validation loss = stuff model has never seen before
      * VALIDATION data **cannot be in training data set**
    * Errors
      * Type 1: assigning true but not actually true
      * Type 2: assigning not true but actually true
    * "How can you fix model to get more accurate if results aren't trending towards expectations?"
      * Confusion matrix can help show this
  * Rock Paper Scissors demo
    * https://rps-tfjs-training.netlify.app
* LLMs for Programmers
  * 3 Stages of LLM Customization
    * Prompts
    * Embeddings
    * Fine-tuning
  * At the start
    * Slabchat example
      * "Chat" with Infinite Red intranet wiki
      * How does it work with ChatGPT?
        * Opt 1: Insert in context window, ask questions
        * Opt 2: Insert proper context into ChatGPT and ask
      * How to get context? Embeddings
    * Neural Network
      * values in/out in numbers
  * Tokens
    * How does sentence become numbers?
      * ex: Unicode
      * Aka tokenization strategy
    * Character tokens vs word tokens
      * letter as tokens (26) vs every book is a unique token
      * What numbers should we use?
  * Vectors
    * Things to numbers
    * Vector similarity
      * Dot product of vectors
      * Cosine similarity of vectors (between 0 and 1)
    * Multi-dimensional vector
      * Latest space
        * chunks between vectors
        * can place input data in space
        * AUTOencoders
        * encode & decode
    * Vectors for Text/Words?
      * TensorFlow Projector for viz of vectors
      * Tokenization is a number with context
    * Gensim to train word vectors
    * ChatGPT encodings
  * Embeddings
    * Figure out features
    * Make it
      * Searchable
      * quantifiable
      * matchable
    * Text embeddings
      * Tokenized, get array of embeddings
      * Wrods is vector in latent space
      * So are words next to it
      * Attention models care about context
      * Classify text
      * Search
      * Use recommendations
* KNN
  * KNN demo
    * knn = known nearest neighbor
    * optimized for images, but can be used with other types of datasets
    * MobileNet = model extensively trained and optimized to be usable on mobile devices
      * predict method
      * infer method
    * can be utilized to measure similarities between items in dataset
  * Person/facial recognition
    * facial landmarks will be valid markers even if face distorted
    * gaussian distance between target image and known answer image
  * Could be used with voices?
* Transfer learning
  * What if I don't want to add datasets to active model?
  * Reuse base part of model to do something new?
  * aisortinghat.com example
  * Few train models from scratch
    * Use transfer learning
* Shares
  * @gantlaborde
  * infinite-red.slides.com/d/Honjtoc/live
  * Google explainer course for recommendation engine
  * Writing own models
    * Fast AI course
    * PyImageSearch.com
* tensorflow.org/hub 