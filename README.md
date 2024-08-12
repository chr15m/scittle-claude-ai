A prompts for Claude AI to generate ClojureScript + Reagent apps.

Now that Borkdude's [Scittle](https://github.com/babashka/scittle/) ClojureScript interpreter for the browser is available on cdnjs, we can use Claude AI to generate simple web apps written in ClojureScript. Please apply all the usual AI generation caveats, warnings, and disclaimers as you please.

The basis of the prompt is the file [`scittle-basic.html`](./scittle-basic.html). It implements an example Scittle app that the AI can build on.

# Prompt

> I would like you to create a simple web app using Scittle, a ClojureScript interpreter for the browser. An example Scittle HTML file implementation is below.
> Scittle largely follows ClojureScript conventions. The Reagent library is available for rendering the interface with React.
> You may also use the Promesa library for handling promises. For example, a fetch request could be performed as follows:
> 
> (p/let [req (js/fetch "https//example.com/api.json")
          json (when (aget req "ok") (.json req))]
          ; do something with the resulting JSON here
          ; or handle nil when the request fails
          )
> 
> Please write an application that ... [YOUR APPLICATION DESCRIPTION HERE]
> 
> [PASTED CONTENTS OF scittle-basic.html HERE]

