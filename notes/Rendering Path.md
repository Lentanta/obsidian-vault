```mermaid
flowchart TD

RenderTree(Render Tree)

style RenderSteps text-align:left
RenderSteps["`
	1.Style
	2.Layout
	3.Paint
	4.Composite
`"]

Server --> HTML
HTML   --> CSS --> CSSOM
HTML   --> DOM
HTML   --> JS  --> DOM
HTML   --> Assets

CSSOM  --> RenderTree
DOM    --> RenderTree

RenderTree  --> RenderSteps
RenderSteps --> Display

```
## Core Web Vitals
Metrics that measure how fast a page load (CRP) and how fast it response to input

LCP (loading): Largest Content Full Paint
INP (interactively): 

