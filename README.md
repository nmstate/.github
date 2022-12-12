# nmstate-ts-proposal

Proposal to add [nmstate-ts](https://github.com/upalatucci/nmstate-ts) as a repo in the `nmstate` org namespace

`NMState-ts` is a typescript types library that would help developers write nmstate compatible code. 
It generates types based on `kubenertes-nmstate` crds under `models` folder and under `custom-models` there are handcrafter non-crds types like interface 
(Maybe later we'll find a way to generate them as well). 

I'm working on another repo where these types will be used to create the [nmstate ui console plugin](https://github.com/upalatucci/nmstate-console-plugin).

- [x] CI enabled and passed.
- [x] Has integration test cases proving valid use cases. (no need for them. this library contain only types)
- [x] Licensed under LGPL-2.0+ or Apache-2.0+(preferred).
