<head>
<meta name="google-site-verification" content="j94IkHu19Am6TroNXqgXc1AnHUZ5oJdIR_xoZB8yI88" />
</head>

# Go-Mermaid

![example workflow](https://github.com/BruceNocentini13/go-mermaid/actions/workflows/go.yml/badge.svg)
[![Go Coverage](https://github.com/BruceNocentini13/go-mermaid/wiki/coverage.svg)](https://raw.githack.com/wiki/BruceNocentini13/go-mermaid/coverage.html)

Go-Mermaid is an open-source Go language (Golang) project designed to streamline and automate the creation of Mermaid diagrams.  
Mermaid is a popular diagramming and charting tool that uses a simple and intuitive text-based syntax to generate a wide variety of diagrams, including flowcharts, sequence diagrams, Gantt charts, and more.

Go-Mermaid is tailored for automation and batch diagram generation, making it an ideal choice for projects where numerous diagrams need to be created or updated consistently. Whether you're a developer, a system architect, or a documentation enthusiast, Go-Mermaid empowers you to automate the creation of Mermaid diagrams with efficiency and precision.

## Instalation

`go get -u github.com/BruceNocentini13/go-mermaid`

### Example

All examples are available [here](https://github.com/BruceNocentini13/go-mermaid/blob/main/examples)

```go
package main

import (
    "fmt"

    "github.com/BruceNocentini13/go-mermaid/flowchart"
)

func main() {
    fc := flowchart.NewFlowchart()
    fc.Title = "Simple Flowchart"

    node1 := fc.AddNode("Start")
    node2 := fc.AddNode("End")

    link := fc.AddLink(node1, node2)
    link.Shape = flowchart.LinkShapeDotted

    fmt.Println(fc.String())
}
```

The example above creates the following diagram:

```mermaid
---
title: Simple Flowchart
---

flowchart TB
    0("Start")
    1("End")
    0 -.-> 1
```

### Roadmap

Implement missing Flowchart features:

- [ ] [Interactions](https://mermaid.js.org/syntax/flowchart.html#interaction)
- [ ] [CSS Classes](https://mermaid.js.org/syntax/flowchart.html#css-classes)

Implement support for other Mermaid diagram types:

- [ ] [Sequence Diagram](https://mermaid.js.org/syntax/sequenceDiagram.html)
- [ ] [Class Diagram](https://mermaid.js.org/syntax/classDiagram.html)
- [ ] [State Diagram](https://mermaid.js.org/syntax/stateDiagram.html)
- [ ] [Entity Relationship Diagrams](https://mermaid.js.org/syntax/entityRelationshipDiagram.html)
- [ ] [User Journey Diagram](https://mermaid.js.org/syntax/userJourney.html)
- [ ] [Gantt Diagram](https://mermaid.js.org/syntax/gantt.html)
- [ ] [Pie Chart](https://mermaid.js.org/syntax/pie.html)
- [ ] [Quadrant Chart](https://mermaid.js.org/syntax/quadrantChart.html)
- [ ] [Requirement Diagram](https://mermaid.js.org/syntax/requirementDiagram.html)

Mermaid supports other diagram types that are currently marked as "experimental" and as such, are subject to change. Once these diagrams leave the experimental phase, they can be added to the list above.

### Contribute

Want to help? Found a bug?

1. Do not hesitate to fork the repository and send PRs with your changes
2. No time to code? Open a bug/feature issue
