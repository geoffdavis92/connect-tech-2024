# Microfrontends

* Why?
  * Challenges with monolithic frontends
  * When to adopt?
    * scalability issues
    * multiple independent teams
    * greater flexibility in tech coices
  * Inspired by microservices architecture
* Benefits  
  * Scalability
  * Faster time to Market
  * Team autonomy
  * Granular updates
* Transitioning from Monolith to Microfrontends
  * Why?
    * Only for a good reason
    * Consider if setup is truly a problem
  * Shifting constraints
    * Complex logic is simpler, but create other challenges like communication and deployment
  * Be deliberate
    * Have a clear plan/visiion on new architecture
    * Have incremental plan on how to get there
* Key principles
  * Focus on biz domains (domain driven design)
    * specific separations of concern 
  * Keep details private
    * Have clear rules between MicroFs to hide how they work
    * Lets teams work independently
    * Make changes without affecting others
  * Automate everything w/ CI/CD pipelines
* Starting Points
  * App shell
    * Core fxnality
    * Enables seamless integration
  * Routing/MicroF loading
  * Global config retrieval (global settings/config)
  * Error handling
  * User state mgmt
    * authentication
    * authorization
    * session mgmt
  * Library integration
    * Essential libs for logging, monitoring, analytics, etc
* Splitting Strategies
  * Horizontal split
    * Good for big teams
    * Each part of website works on its own
    * Lets teams work faster, on their own
    * Make sure different parts can talk to each other
  * Vertical split
    * Good for SPAs
    * Different part of biz
    * 1 team works on whole thing
    * Good for ownership, but attention needed on data flow & UX
* Diagramming for MicroFs
  * Isolated biz logic - decouples app logic from implementation details
  * Defined I/O boundaries - clear interfaces
  * Enhanced adaptability - seamless integration
  * Hexagonal architecture
    * vertical sections
      * admin/app shell
      * external/API
      * internal/events
    * horizontal sections
      * left = input/driving
      * right = output/driven
* Links
  * slides
  * microfrontend.dev

Q&A
* Does app shell have to be JS-based stack?
  * Not necessarily
  * Astro/Next.js just 2 options
* Way to combine vertical and horizontal splits?
  * Ex: StJude.org with different product teams + design system (managed horizontally)