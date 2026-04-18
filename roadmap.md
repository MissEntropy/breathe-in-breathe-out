# the plan to get there

## where i am

**strengths**
- BSc + MSc CS — strong in theory, complexity, algebra, graph theory
- 6 years algo dev: classic CV, 3D geometry, then ML engineering (data + evaluation)
- worked with X3D, ConvNeXt, know how attention works conceptually
- can read papers
- data and evaluation expertise (underrated in research)

**real gaps**
1. pytorch fluency — layer internals, weight manipulation
2. architecture internals in code — know the theory, haven't built it
3. XAI-specific methods — interested, not deep yet
4. no research artifact yet

---

## the month

### week 1 — pytorch internals
the day tour: inspect, manipulate, do surgery on layers.
key add: **forward and backward hooks** — XAI lives here.

layers to own: `nn.Linear`, `nn.Conv2d`, `nn.Embedding`, `nn.BatchNorm2d`, `nn.LayerNorm`, `nn.MultiheadAttention`

operations to own:
- inspect weight shapes
- assign to `.weight.data` correctly
- custom initialization
- freeze / unfreeze
- copy weights between layers
- replace a layer in a model
- extract activations with hooks
- implement linear fusion + conv fusion
- manual forward with `F.linear`, `F.conv2d`

### week 2 — build a transformer from scratch
not conceptually. in code.
- positional encoding
- multi-head attention
- transformer block
- read "Attention is All You Need" alongside

### week 3 — XAI methods, implement the classics
- **Grad-CAM** — uses backward hooks, connects to week 1
- **Integrated Gradients** — axiomatic attribution
- **Attention visualization**

read the original papers as you implement each one.

### week 4 — build one artifact
apply XAI tools to a model you already know (X3D or ConvNeXt).
find something interesting. write a clean README that explains the findings.
put it on github. this is what you point to.

---

## the job to look for

**research engineer** or **ML engineer at a research-oriented team** — close enough to research to be reading papers and implementing things, not expected to produce novel results from day one.

targets: vision research labs, XAI-focused companies (Fiddler, Arthur), any team where your 3D geometry background is rare and useful.

---

## the habit once employed

- one paper per week
- one implementation per month

in a year: 12 implementations, 50 papers read. that's a researcher.
