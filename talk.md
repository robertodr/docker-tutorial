name: inverse
layout: true
class: center, middle, inverse
---

background-image: url(img/yoshimi.jpg)
class: background

## Docker battles the (pink) virtual machines

<!-- 
<p style="text-align:center;"><img src="img/Yoshimi-Slide.jpg" style="width: 40%"></p>
<p style="clear: both;">
-->

.author[Roberto Di Remigio]

.date[21 January 2019, Haraldvollen]

.footnote[[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) licensed.
Browse slides at [http://tinyurl.com/docker-tutorial](http://tinyurl.com/docker-tutorial)]

???

- Add Docker whale

---

layout: false
.left-column[
  ## What is it?
]
.right-column[
- An _image_ build tool
- A _container_ management tool

<p style="text-align:center;"><img src="img/nyan-whale.gif" style="width: 100%"></p>
<p style="clear: both;">
]

---

layout: false
.left-column[
  ## What is it?
]
.right-column[
- An _image_ build tool
- A _container_ management tool

<p style="text-align:center;"><img src="img/docker-overview.png" style="width: 100%"></p>
<p style="clear: both;">
]

---

layout: false
.left-column[
  ## What is it?
]
.right-column[
- An _image_ build tool
- A _container_ management tool

<p style="text-align:center;"><img src="img/layering.png" style="width: 100%"></p>
<p style="clear: both;">
]

---

layout: false
.left-column[
  ## What is it?
  ## Why should I care?
]
.right-column[
- Reproducibility
- Shipping your applications
- Running services in isolation
- Reproducibility

<p style="text-align:center;"><img src="img/hypnotoad.gif" style="width: 70%"></p>
<p style="clear: both;">
]

???

- Add figure explaining how Docker stacks on the OS
- Add hypnotoad gif saying "Reproducibility"

---

layout: false

## What does the OS do?

.left-column[
<p style="text-align:left;"><img src="img/ranxerox.jpeg" style="width: 150%"></p>
<p style="clear: both;">
]
.right-column[
<p style="text-align:right;"><img src="img/os.jpeg" style="width: 80%"></p>
<p style="clear: both;">
]

???

- Add RanXerox picture

---
layout: false

## Why not Virtual Machines?

![Sample image](img/vm.jpeg)

---
layout: false

##  HaaS: "Hello, world"-as-a-Service

- `Dockerfile`
```
FROM ubuntu:18.04
CMD ["bash", "-c", "echo 'Hello, world!"]
```

- `docker build -tag simple-hello .`
- `docker images`
- `docker run simple-hello`

???

- Not very useful! It only says "Hello, world!"
- Explain options
- Then move to terminal

---

## User says: "Can't compile/Tests fail/Can't run"

<p style="text-align:center;"><img src="img/mrchem-issue.png" style="width: 100%"></p>
<p style="clear: both;">

```bash
docker run --rm -it -v "$PWD":/home/mightybuilder/work mrchemsoft/mrchem_ubuntu-18.04:latest 
```

---

## User says: "Can't compile/Tests fail/Can't run"

- Option A. Troubleshoot in a container

```bash
docker
```

- Option B.

```bash
docker run --rm -it -v "$PWD":/home/mightybuilder/work mrchemsoft/mrchem_ubuntu-18.04:latest 
```

---

## JaaS: Jupyter-as-a-Service 

```bash
docker run --rm -p 10000:8888 -e JUPYTER_ENABLE_LAB=yes -v "$PWD":/home/jovyan/work jupyter-teaching/psi4-notebook:latest
```

??? 

- Explain options
- Then move to terminal

---
layout: false

## Commercial #1

<p style="text-align:center;"><img src="img/cmake-cookbook-doge.jpg" style="width: 70%"></p>
<p style="clear: both;">

---
name: last-page
template: inverse

<p style="text-align:center;"><img src="img/whale.gif" style="width: 50%"></p>
<p style="clear: both;">

## Go! Docker!

Slideshow created using [remark] and served using [cicero]

Slides available on [GitHub](https://github.com/robertodr/docker-tutorial)

Browse slides at [http://tinyurl.com/docker-tutorial](http://tinyurl.com/docker-tutorial)

[remark]: https://github.com/gnab/remark
[cicero]: https://github.com/bast/cicero

???

Add a GIF with the whale
