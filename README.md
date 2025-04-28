# Scaffolds Reading Group

## dPASP

Geh, R.L., Gonçalves, J., Silveira, I.C., Mauá, D.D. and Cozman,
F.G., 2023. dPASP: a comprehensive differentiable probabilistic answer
set programming environment for neurosymbolic learning and
reasoning. [arXiv preprint
arXiv:2308.02944](https://arxiv.org/abs/2308.02944).

## Installing dPASP

The GitHub repo is at https://github.com/kamel-usp/dpasp .

The tutorial link is broken, so I raised an issue here
https://github.com/kamel-usp/dpasp/issues/11 However the page is
available via the Internet Archive at:
https://web.archive.org/web/20240620194257/http:/kamel.ime.usp.br/pages/learn_dpasp

It seems that the software only works on Linux (not Mac). Here are the
steps I (@RobBlackwell) took to run it on an Azure Linux VM:

``` sh

sudo apt install python3-venv build-essential

sudo add-apt-repository ppa:potassco/stable
sudo apt update
sudo apt install clingo libclingo-dev libncurses-dev

pip install --upgrade setuptools pip

pip install pasp-plp

```
