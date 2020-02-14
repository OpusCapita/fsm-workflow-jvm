## FSM Workflow (for Java)

[![CircleCI Status](https://circleci.com/gh/OpusCapita/fsm4j/tree/master.svg?style=shield&circle-token=:circle-token)](https://circleci.com/gh/OpusCapita/fsm4j)
![badge-license](https://img.shields.io/github/license/OpusCapita/fsm4j.svg)

### Demo

- [Complete demo app](https://github.com/OpusCapita/fsm4j/tree/master/demo)

### Introduction
[Finite State Machine](https://en.wikipedia.org/wiki/Finite-state_machine) workflow is implemented in Groovy

- state is stored in the business object related to workflow(machine), not in an extra
workflow generic object. Multiple workflows could be defined for one business object,
it means that for each workflow own state field should be used
- one state per workflow execution (no parallelism)
- actions are executed in the transition, not in the node/state
- no event sending inside the workflow itself (in action)
- no variables in state workflow: all variables/data need to be stored in
the business objects
- events: visible/available in UI as action buttons for the user
- workflow definition stored as JSON
- guard support (transition/event availability is defined via
condition/expression/function = guard)
- hierarchical states are not supported

#### Notes

The following things will be implemented later as extensions/helpers (separate sibling library) or in specific application:
- automatic transitions
- task list is based on domain object
- graphical editor
- logging
- analysis

**P.S.** basic ideas on how FSM API looks like are taken from [fsm-as-promised](https://github.com/vstirbu/fsm-as-promised)

### FSM (Core)

FSM core could be found here [here](core/README.md)

### Workflow Transition History

Workflow Transition History is implemented as separate library. You can find more information [here](history/README.md).

### FAQ for developers
**How I can run demo application in development mode?**
`make start`

**How I can build demo application?**
`make build`

### References

[Existing FSM libs review](existingFsmLibsReview.md)

### Contributors

| [<img src="https://avatars.githubusercontent.com/u/24603787?v=3" width="100px;"/>](https://github.com/asergeev-sc) | [**Alexey Sergeev**](https://github.com/asergeev-sc)     |
| :---: | :---: |
| [<img src="https://avatars.githubusercontent.com/u/24652543?v=3" width="100px;"/>](https://github.com/kvolkovich-sc) | [**Kirill Volkovich**](https://github.com/kvolkovich-sc) |
| [<img src="https://avatars0.githubusercontent.com/u/31243790?s=460&v=4" width="100px;"/>](https://github.com/estambakio-sc) | [**Egor Stambakio**](https://github.com/estambakio-sc) |
| [<img src="https://avatars1.githubusercontent.com/u/24733803?v=4" width="100px;"/>](https://github.com/ddivin-sc) | [**Dmitry Divin**](https://github.com/ddivin-sc) |


Contributing are welcome. We need YOU! :metal:
