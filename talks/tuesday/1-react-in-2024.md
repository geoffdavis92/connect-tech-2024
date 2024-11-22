# React in 2024
*Cory House - @housecor*

* React 19 the New Stuff
  * https://19.react.dev/reference/react
* Fetching in React over 10 years
  * 2014 - fetch in `componentDidMount`
  * 2019 - fetch in `useEffect`
  * 2020 - Custom fetch hook `useFetch`
  * 2021 - React query
  * 2022 - React query with `useErrorBoundary`
  * 2023 - React query with `useSuspenseQuery`
  * 2024 - React Server Components
* App demo
  * Decompose components
  * `<title/>` sets head title (like Helmet)
  * Zod - runtime typechecker
  * No state set
    * "Future of React where you'll rarely explicitly use `useState`/`useEffect`"
* Optimistic UI
  * App should feel fast, even if operation is slow
  * Server-based functions
    * `"use server";`
    * Fns accessible over HTTP(s)
  * If error, revert to previous state
  * `useActionState` hook
  * Uncontrolled input
  * `action` prop on `<form>`
    * Uses callback with `formData` argument
* React 19's new stuff
  * 9 new features, 2 new directives, 5 new apis, 3 new hooks
  * Removing long-deprecated features
* New Features
  * React Server cmpnts - render at build, or each req
  * Actions - use async transitions and auto submit data
  * Custom element support
  * Document metadata support - ex. `<title>`, link, eta tags with auto hoist
  * Stylesheets with precedence settings
  * Async scripts in any cmpnt - auto deduped
  * Preload resources - prefetch DNS, preconnect, preload, preinit
  * Unexpected tags in head/body are skipped 
  * Better error reporting - deduped errors
* New Directives
  * `"use client"` - mark code that only runs on client
    * Hooks can only be used on client cmpnts
    * All children are client components
  * `"user server"` - server-side functions to be called from client
    * libraries that generate code on RSCs are not sent to client
* 5 new APIS
  * `use` Read resources (like promises and context) in render
    * Not a hook
    * Can be called conditionally or in loops
    * Way to use this API as light `async`-style behavior
  * `ref` prop
  * `ref` callback cleanup
  * `Context`
  * `useDefferedValue`
* Hooks
  * `useActionState`
  * `useFormStatus` - read form status
    * Useful during form submitting
    * Pending state, complete, etc
  * `useOptimistic`
* New/Coming soon
  * useTransition/startTransition - update state w/o blocking UI
  * server-only - throw error if imported by client cmpnt
  * May not be for React 19.0.0
    * React compiler - Beta; can use in 17/18 now
    * cache - cache data fetch/computation
    * taint - prevent object from being passed to client cmpnt

* Links
  * github.com/coryhouse/next-react-19