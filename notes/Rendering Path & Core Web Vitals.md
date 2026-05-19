## Rendering Path Diagram
---
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

CSSOM  --> RenderTree
DOM    --> RenderTree

RenderTree  --> RenderSteps
RenderSteps --> Display
```
## Core Web Vitals
---
Metrics that measure **loading performance**, **interactivity**, and **visual stability**.

LCP (loading): Largest Contentful Paint
INP (interactively): Interaction to Next Paint
CLS (visual stability): Cumulative Layout Shift

**Diagnostic metrics**
FCP: First Contentful Paint
TBT: Total Blocking Time
