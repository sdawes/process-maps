# process-maps
## Simple Process Example

```mermaid
flowchart TD
A([Change identified])
B[Log in backlog]
C[Assess change]
D{Estimate needed?}
E[Get estimate]
F[Proceed to prioritisation]

A --> B
B --> C
C --> D
D -- Yes --> E
D -- No --> F
E --> F
