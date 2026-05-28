```mermaid
flowchart TD

A([Change identified by any team])

B[WCP: Log change in FWT backlog]
C[(FWT backlog in SharePoint Excel)]
A --> B
B --> C

D[WCP: Review and assess change]
C --> D

N1["Assessment considers
Resources
Time
Cost
Impact
Size and complexity
Quick win
Regulatory or mandatory
Available budget"]
D --- N1

E{More detail needed?}
D --> E

F[WCP: Draft high level requirements]
G[(High level requirements in SharePoint Word)]
E -->|Yes| F
F --> G

H{Estimate required?}
E -->|No| H
G --> H

I[Internal teams or HYKE: Provide estimate]
J[(Estimate: time, cost, resources)]
H -->|Yes| I
I --> J

K[WCP: Update assessment using estimate]
H -->|No| K
J --> K

L[WCP: Prioritise change and assign status]
K --> L

M{Mandatory regulatory change?}
L --> M

P{Funding available within existing allocation?}
M -->|No| P
M -->|Yes| R
P -->|Yes| R

O[WCP: Set status
Backlog
Revisit
Monitor
Reject]
P -->|No| O

R{Significant change or change of priority?}
R -->|Yes| S
R -->|No| T

S[WCP: Prepare paper for Proposition Design Forum and Steering]
S --> T

T{Approved to proceed?}
T -->|No| O
T -->|Yes| U

U[Start delivery activities]
U --> V
U --> W
U --> X

V[Marketing and UX: Content and design updates]
W[Legal and compliance: Review and sign off]
X[HYKE and or internal teams: Build and configure]

Y[WCP: Coordinate testing and sign off]
V --> Y
W --> Y
X --> Y

AA[Deploy change]
AB[Monitor outcomes and feed learning into backlog]
Y --> AA
AA --> AB
AB --> C
