```mermaid
flowchart LR

style D text-align:left

T(Render Tree)
RenderStep["`
	1.Style
	2.Layout
	3.Paint
	4.Composite
`"]

Server --> HTML
HTML   --> CSS --> CSSOM
HTML   --> JS  --> DOM
HTML   --> Fonts

CSSOM  --> T
DOM    --> T 

T --> RenderStep

```