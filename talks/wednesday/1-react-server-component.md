# Demystifying React Server
*D*

* ...
* RSC
  * Doesn't ship JavaScript
* Multiple Server Entry points
  * Not limited to single server fetch
  * Suspense
    * Defers requests for children
    * Streams from server once available
    * "Is React still loading in this suspended component?"
      * Depends
      * Thing that is "streaming" is Next.js
* SSR vs SPA vs RSC
  * SSR cmpnts request data from API
  * SPA -> JS-rendered elements, cmpnts, etc; one entry to server
  * RSC -> 5 different entrypoints (components) to servers; each one only interacts with server in context of cmpnt
* "use client"
  * RSC run on server so can't use React 100% of the time
  * `"use client"` directive
  * Any consumed code (ex cmpnts) in a client cmpnt file will load as client
  * Bundling
    * Creates bundles per client cmpnt tree
  * Best practices
    * Only if using React features that req UI
    * Bundler handles redundant issues
* Component Structures
  * Delba Oliveira graphic (@delba_oliveira on twitter)
  * "Can't go back" once declaring a cmpnt on directive or the other
  * Prop rendering is sole way to go S->C (prop)->S
  * via slot pattern
  * Some caveats down the child tree
* "use server"
  * Controls server actions, not components
  * Runs completely on server
  * Server Actions
    * Separate file (`<name>Action.server.(jsx|tsx)`)
    * Using "use server" directive in async function inside component
  * Misconception
    * doesn't turn cmpnt into server cmpnt
    * server-only package
      * Flags components as server-only cmpnt
* Best Practices
  * Use Suspense to defer non-essential content
    * don't use above the fold content unless its secondary data
    * Suspend all data loading below fold
    * Slowest elements should be in suspense
  * Be explicit with component types
    * Server cmpnt example: `<cmpnt name>.server.(jsx|tsx)`
    * Also import server-only
    * .client.(jsx|tsx)
    * Universal `<cmpnt name>.(jsx|tsx)`
  * Fetch everything witha Cache
    * GraphQL's data loader pattern
    * Fetch all data early and as high level as makes sense
    * RSC children can fetch again
    * Avoids excessive prop drilling
  * Colocate data fetcing utils
    * Loading spinners, skeletons, queries, other data loading patterns
    * Colocate in modules
* Recap
  * Multiple server entrypoints
  * More frameworks will be adopting soon, esp with React 19
  * use client to get new client bundles, use server for actions, not components
  * Best practices for your team
  * dustingoodman.dev
  * @dustingoodman.dev (bsky)
  * @dustinsgoodman(twitter)
* Q&A 
  * Should Actions look like my traditional API?
    * Think about like functions
    * Throw/catch errors as necessary
  * Server action non-async?
    * No
    * By practice, they are async
    * Action isn't running on client, but on edge fn
  * Think use client/server ever be automated?
    * Potentially in future
    * Not possible today, how bundlers/tooling work
  * RSC cacheability at component or bundle level?
    * Both
    * But you'll have to fine-tune manually
    * RSC apps are 100% cacheable