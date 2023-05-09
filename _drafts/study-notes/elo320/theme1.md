# Theme 1

## system complexity

System -> Subsystem -> Component -> Subcomponent -> Part

eg. Airplane -> Radar -> RF Transiever -> Amplifier -> Transistor

## System Building Blocks

- Functional
- Physical
- Common

### System Boundaries

External Inputs and Outputs exist (eg. User, Environment, Shipping ...), they carry:

- Data
- Signals
- Materials
- Energy
- Activities

## System Development Process

1. Concept Development
    - Needs Analysis (Whata are the needs)
    - Concept Exploration (What are the options)
    - Concept Definition (What must it do)
2. Engineering Development
    - Advanced Development (Risk Managementl, Subsystem Development)
    - Engineering Design (Designt Reviews, Component Designs, Testing, 1st prototype)
    - Integration & Evaluation (Trials, Refine and Iterate)
3. Post Development
    - Production (Factory Floor)
    - Operations and Support (Training, Upgrades, Logistics, Support Field Engineers)
    - Disposal (When its done how do you get rid of it?)

The above all fallsunder documentation. After that there is also system modelling.

- Models
- CAD , schematics
- Test setups
- Architectural diagrams/mockups
- High level system simulation

## The SE Method

Need -> **requirements analysis** -> Requirements -> **Functional Definition** -> System Model -> **Design Validation** -> Solution

between every phase you go back and check/iterate of the choices made and whether the current developemnt is inline with what was decided.

The four steps:

1. Requiremnents Analysis
1. Functional Definitition
1. Physical Definition
1. Design Validation



## Systems Engineering Management (lines between PM and SE)

2 interfaces between people: responsibilities and authority

sys eng management is importantn so that enveryone knows what is expected of them

1. SE
    - Systems Architecture
    - Technical Coordination
    - Integration
2. PM
    - Project Plam (costs and schedules)
    - resource Allocation
    - Financials & Conflicts
3. Either Or
    - Task Definitions
    - risk Management (simply defined on  (1)*Probability* and (2)*Criticality*)
    - Customer Interaction

### SOW (Statement of Work)

### WBS (Work BreakDown Structure)

Heirarchical

```
                                       System
_________________________________________|_______________________________________________________________
|                           |                   |                           |                            |
SE                          PM                  Eng Dev                     Integration                  Installation
|                           |                   |                           Eval                         support
|-> Needs Analysis          |-> Documentation   |-> Development             |-> integration testing      |-> Installation
|-> Concept Exploration     |-> HR              |   |-> subsystems          |-> systems testing          |-> Transport
|-> concept Development     |-> Contracting     |       |-> component1      |-> operational testing      |-> Operations Testing
                                                |       |-> component2      |-> Acceptance testing       
                                                |                           
                                                |-> Acceptance Testing      

```

generally:

1. Product
    - subsystems
        - components
    - functional design
    - engineering design
    - fabrication
    - technical documentation
1. Support
    - supply support
    - test equipment
    - transport
    - documentation
    - facilities
1. Testing
    - integration testing
    - systems testing
    - acceptance testing
    - operational testing


### Gantt chart

- Time based
- Critical path: is the route that takes the longest amount of time.
- Slack: empty space between tasks where people are waiting for other people

### The sys eng process

1. Operational requirements
1. functional analysis
1. system analysys
1. system testing
1. evaluation trategy

### Risk Management

$$risk = probability \times severity$$

#### mitigation

- more review
- more oversight/senior designer
- special analysis and testing
- rapid prototyping
- requirements relief
- fallback alternatives