# Scaffolds Reading Group

## Reading List
[link to list](https://docs.google.com/document/d/1HPfYtBJkwuexZnb3_XWWrlCL8dlMHvBBjONkNc8MSNk/edit?usp=sharing)

## dPASP

Geh, R.L., Gonçalves, J., Silveira, I.C., Mauá, D.D. and Cozman,
F.G., 2023. dPASP: a comprehensive differentiable probabilistic answer
set programming environment for neurosymbolic learning and
reasoning. [arXiv preprint
arXiv:2308.02944](https://arxiv.org/abs/2308.02944).

### Installing dPASP

The GitHub repo is at https://github.com/kamel-usp/dpasp .

The tutorial link is broken, so I raised an issue here
https://github.com/kamel-usp/dpasp/issues/11 However the page is
available via the Internet Archive at:
https://web.archive.org/web/20240620194257/http:/kamel.ime.usp.br/pages/learn_dpasp

It seems that the software only works on Linux (not Mac) on x86
processors. Here are the steps I
[@RobBlackwell](https://github.com/RobBlackwell) ) took to run it on
an Azure Linux VM:

``` sh

sudo apt install python3-venv build-essential

sudo add-apt-repository ppa:potassco/stable
sudo apt update
sudo apt install clingo libclingo-dev libncurses-dev

pip install --upgrade setuptools pip

pip install pasp-plp

```

### dPASP via Docker on Apple Silicon

In the docker subdirectory, there is a `Dockerfile` that provides a
working dPASP environment via Docker, even on Apple Silicon
machines. I assume you have a working Docker (See [Get
Docker](https://docs.docker.com/get-started/get-docker/)), and `Make`
(probably via homebrew).

To build the Docker image (this may take some minutes!):

``` sh
make build
```

To run the Docker image:

``` sh
make run
```

The latter drops you into a shell prompt. You can test `pasp` by typing:

``` sh
pasp --help
```

``` sh
cd /app
pasp smokers.plp
```

I ([@RobBlackwell](https://github.com/RobBlackwell)) have tested this
on Apple Silicon. It might work on Windows too?
