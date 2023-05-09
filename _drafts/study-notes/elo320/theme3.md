# Theme 3

## 3.1

### 3.1.1 Advanced Development

1. reduce risk by analysis, simulation, development, prototyping.
1. risk managemnt requires a well-defined system concept
1. Concept definition -specs concept-> Adcvanced Development -validated developmental model-> engineering design
1. The Systems Engineering Method!

### 3.1.2 Requirements Analysis

Translate system spec to critical subsystems/components spec and identify high risk components for advanced development.

1. look at system functional specifications first
    - is proposed breakdown of subsystems/components still valid
    - should requirements be derived where not stated

1. identify components requiring advanced development
    - if no analogous components exiost are there ones wioth similar funciton and architecture/materials? if not the advanced development
    - risk analysis what is scope of adnvacced development
    - development planning
    - consider budget
1. what type of development is appropriate
    - new function: design required
    - new architecture: design required
    - new production method: use old design and test new hardware
    - note: sometimes simulation is enough

### 3.1.3 Functional Analysis and Design

Analysis and simulation to resolve exactly what is required of components.

1. refine from concepot defnition
1. look for:
    - extended funcitonal performance
        - compare function of element to that of new one. what is new/different? is the extension trivial?
    - high complexity functions
        - inherintly complex functionalioty compared to other functions
    - unknown environment interaction
        - complex interfacs, things that can't be simulated
1. Redo functional design with th eaboveanalysis in place

### 3.1.4 Prototype Development

Identify inpolementation issues. design, develop, build critical components.

1. where cant simulate/analyse; design build and test
1. identify problem areas in selecting what to prototype
    - unusually stringent performance
    - new material or manufacturing
    - extreme or defined environments
    - unusual or complex interfaces
1. choose level of development carefully
1. apply concurrent engineering. bring logistics, produciton & maintenance experts into advanced development
1. use rapid prototyping
1. test only what you need ot validate

### 3.1.1 Development Testing

Test plan for critical element testing. Conducting tests. Feedback deficiencies.

1. have a sound test  plan, procedures and analysis lna in place
    - seek out desing deficiencies not presupoosed success
    - good methodology
        - prioritize tests
        - plan how to analyse tests
1. create asuitable test environment
    - realistic inputs
    - compare model and sustem element responses
    - equipment needs calibration/verification too
1. conduct tests 
    - know how to deal with failures
    - conduct tests wwiht full life cycle under consideration(where approriate)
    - make provision for modification and retest
1. analysis of test results
    - compare top models
    - if fail: check model, test setup, and test procedurte first
1. plan for correcting deficiencies or relaxing requirements

## 3.2

### 3.2.1 Engineering Design

1. Implementing the system buildiung blocks. all about DESIGN!
    - Advanced Dev -validated developmental model (+design specs)-> engineering design -engineered prototype(+test plan)-> integration and evaluation
1. All components must be materialized at the end of this phase
    - NB! All interactions/interfacesdefined here in detail
    - Systems engineering method

### 3.2.2 Requirements Analysis

Verify requirements for consistency and completeness. Identify requirements for interanl and external interactions.

1. start with the system specs and reevaluate for completeness, relevance, consistency etc.
1. focus on medium risk requirements not developed during advanced development.
1. consider user and environmental interface requirements
1. assembly and installation requirements now important (no design alterations on site)

### 3.2.3 Functional Analysis and Design

Analyse component interactions. Analyse detailed user interactions. Design and prototyping interfaces.

1. focus on components
    - define functional interactions between components
    - draw boundaries
1. modular configuration
    - minimum interfaces/interactions
    - allows for independant specification, development, design, manufacturing and testing
    - functional post assembly
    - faulty components can eb swapped with "form, fit and function" equivalents
    - upgrades
1. sectioning functional elements/units
    - distinct significant function
    - single engineering discipline
    - function is commonly found in multitude of systems
1. user interface functionality
    - displays
    - user reaction 
    - user command
    - command actuator

- NB! use functional diagrams down to component level!

### 3.2.4 Component Design

Preliminary and Detailed hardware designs (with reviews and interfaces). Prototype engineered components.

1. Preliminary Design
    - demonstrate chosen system design conforms 
    - functional design done here
    - design adn interface specifications
    - mockups, models, breadboards
    - interface design
    - top level software
    - integratrion and test plans
    - RMA logistics
    - follow up by PDR (focus on large issues, establis system configuration baseline)
1. Detail Design
    - production specs
    - detailed engineering drawings 
    - prototyped hardware
    - detailed test plans, QA
    - critical design review (more extensive, product baseline)

### Validation

Test components, correct deficiencies and document.

### 3.2.5 More Component Design Considerations

- CAD is integral
- electronics: benefit from connector/port/interface/comms standards
- automated layouts are used

#### how does SE fit into this stage?

- provide and oversee implementation of automation tools
- reliability analysis
- more...
    1. external interfaces
    1. mounting
    1. temp and pressure
    1. contamination
    1. special high risk components
    1. integrate into design
        - modularity
        - dependancy
        - multiple functional paths
    1. desiugn for maintainability
        - repair andservicing
        - fault tracing
        - test points

### 3.2.1 More Detail Design Considerations

design for production
1. reasonable tolerances
1. common manufacturing processes
1. use OTS componernst as much as possible
    - lets other tak erisk and development costt
    - not wise for proprietary IP specific stuff
1. design for automated manufacturing
1. stadardized circuitry
1. minimal "hand tuning"
1. software progrmmable where possible

## 3.3

### 3.3.1 Integration and Evaluation

- The "Lego" phase 
- change in activities and participents from the engineering design phase.
- things dont work together as they should
- plan ahead

engineering desing -> integration and evaluation -> produciton and development

1. test engineers take lead in conducting and analysis of tests
1. design engineers involved in test equipment requierements
1. SE involved in test planning
1. All are involved in test architecture

HIGH pressure!

### 3.3.2 Test Planning and Preparation

- formal test plan will inclued
    1. system introduciton (test engineers arent involved in development)
    1. programme summary (who what wher)
    1. developmental testing and evaluation (objectives, methods, events)
    1. operational testing and evaluation
    1. testing and evaluation ersource summary (test articles, inputs, sites, instruments)

- All the above hase to happen before / during engineering development as you ened toime to prepare.
    1. First review system requirements (did they change? have there been any technological improvements, cahnges in programme scheduling/funding?)
    1. Specific issues (What oversight migh occure during testing? (manager? QA? Customer?). Resource planning)
    1. do you need to test bough components before integration?
    1. Are the facilities available? 

### 3.3.3 System Integration

1. integrate bottom up (components inbto subsystems then subsystems into systems)
1. incremental testing needs equipment to "simulate" the missing parts
1. make sure everything is qualified (hardware, software, people, equipment)

### 3.3.4 Subsystem Integeration

start with the subsystems that only use external inputs and simulate these inputs with equipment. Qualify the output then use as test equipment


### 3.3.5 Developmental Subsystem Testing

### 3.3.6 Operational Teset and Evaluation
