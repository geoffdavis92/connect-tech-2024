# Fully Type-Safe Projects with Zod
*Sean McQuaid*

* About Sean
  * @seanmcquaidcode.bsky.social
  * @seanmcquaidcode
  * Github - seanmcquaid
  * Lead Software Engineer at Chick-fil-A

* I <3 TypeScript
  * Fake build-time safety
  * No runtime safety
* Some "wild" stuff can be done with valid TS
  * `any`
  * Type casting: `x = "Hello world" as unknown as number"`
    * `x.toFixed(2) // throws error`
  * `// @ts-ignore`
* Actual type-safety
  * Zod
  * https://github.com/colinhacks/zod 
* Zod Fundamentals
  * `import { z } from "zod";`
  * `z.<data type>`
  * Can be used to infer TS types
    * `z.infer<typeof string>`
  * Utility types from TS
    * union, optional, etc
  * Can describe enums in Zod
  * Type coercing
    * ex: `z.coerce.string()`
  * Able to use `z.(...).revine()` for custom validation
    * ex: enforcing exact length on string
* Practical examples demo
  * Environment variable enforcement
    * Also enables autocomplete!
  * Search params
    * Validate parameters
    * Length, actual strings, etc
  * API responses
    * Ky (js library) to handle API response
    * validate API response schema
    * Good to have sane defaults in case of API schema invalidation
  * Validating request body
    * Enforcing expected shape
    * Validation using generic typing
  * Form validations  
    * Custom validations like `.email()`
    * Refine methods for custom validations
  * Date picker
    * (in React) bad `useEffect` to check inputs
    * Using zod's `.superRefine()` method
* Closing thoughts
  * Great for validating inputs
  * Also usable for backend code
  * Helps enable greater predictability
* Q&A
  * Refine vs. SuperRefine
    * 99% you'll use refine
  * Mechanisms for custom regex?
    * Depends on regex
    * Builtins offer a lot of power
    * .refine() to extend
  * IgnoreUnknownProperties?
    * Zod will not validate unknown/un-defined properties
    * Option to turn on strictness
  * Composable schemas?
    * ex: password schema, use that in form data schema in password field
    * Answer: yes!
    * Try not to overdo it
  * Generate Zod schema from Typescript?
    * Website to do this (TS type or JSON -> Zod)
    * "Use AI"