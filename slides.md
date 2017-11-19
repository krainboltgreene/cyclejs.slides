class: middle, center

# cycle.js

PEOPLE

⎯⎯⎯👰⎯⎯⎯👰⎯⎯⎯👰⎯⎯⎯🤵⎯⎯⎯🤵⎯⎯⎯🤵⟶

by(2)

⎯⎯⎯👰👰⎯⎯⎯👰🤵⎯⎯⎯🤵🤵⟶

mapValues(💕)

⎯⎯⎯👭⎯⎯⎯👬⎯⎯⎯👬⟶

---

class: middle, center

complex ⟺ simple

---

background-image: url('./assets/complex.png')

---

class: middle, center

> **suf·fer·ing**

> */ˈsəf(ə)riNG/*

---

class: middle, center

# 👶

> value(s) over time(s)

---

class: middle

``` javascript
xstream
  .of("😶")
  .map((value) => alert(beep))
```

---

class: middle

``` javascript
xstream
  .of("🗣")
  .map((value) => alert(beep))
  .addListener({})
```

---

class: middle

``` javascript
xstream
  .perodic(1000)
  .of("🗣")
  .map((value) => alert(beep))
  .addListener({})
```

---

class: center, middle

background-image: url('./assets/cyclejs_logo.svg')

---

background-image: url('./assets/simple-human-computer.svg')

---

background-image: url('./assets/actuators-senses-input-output.svg')

---

background-image: url('./assets/hci-inputs-outputs.svg')

---

class: middle

``` javascript
import {run} from "@cycle/run"

import application from "./application"

import drivers from "./drivers"

run(application, drivers)
```

---

class: middle

``` javascript
import {run} from "@cycle/run"
```

---

class: middle

``` javascript
import application from "./application"
```

---

class: middle

``` javascript
import drivers from "./drivers"
```

---

class: middle

``` javascript
run(cycle, drivers)
```

---

class: middle

``` javascript
import {makeDOMDriver} from "@cycle/dom"

export default {
  DOM: makeDOMDriver("body")
}
```

---

class: middle

``` javascript
import mapValues from "@unction/mapvalues"
import cycleState from "cycle-state"
import {infuse} from "snabbdom-view"
import {shell} from "@internal/ui"
import * as intents from "@internal/intents"
import signals from "@internal/signals"
import initialState from "./initialState"

export default function cycle (sources) {
  const state = cycleState(
    intents
  )(
    initialState()
  )(
    signals(sources)
  )

  return {DOM: mapValues(infuse(shell))(state)}
}
```

---
