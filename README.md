p6steve fork to cover macOS M1 via vftools with
ultimately FROM ubuntu:latest --platform=inux/arm64 VIA p6steve/rakudo

Instructions:
To run jupyter (or adjust Dockerfile)
- git clone https://github.com/p6steve/raku-notebook
- cd raku-notebook
- docker build -t p6steve/rakudo:notebook-2021.05 .
- docker push p6steve/rakudo:notebook-2021.05
- docker run -itP rakudo:notebook-2021.05
- jupyter notebook --port=8888 --no-browser --ip=0.0.0.0 --allow-root
- docker container ls -a (new terminal, note vm-port mapped)
Browse to http://ubuntu:vm-port?token

(Copy 2021.05 and merge for other versions)

Versions covered:
- 2021.05

# Raku notebook

[![Raku](https://img.shields.io/badge/Raku-v6.d-blue.svg)](https://rakudo.org/downloads/star/)
[![Rakudo](https://img.shields.io/badge/Rakudo-2021.09-blue.svg)](https://github.com/rakudo/rakudo/releases/tag/2021.09)
[![Build Status](https://travis-ci.com/sumanstats/raku-notebook.svg?branch=master)](https://travis-ci.com/sumanstats/raku-notebook)


<a href="https://raku.org/"><img src="imgs/raku_jupyter.png" width="300" height="120" align="right"></a>



This is a docker container with **Raku** kernel in jupyter notebook. Also contains [asciinema](https://asciinema.org/) to record and share your terminal sessions, the right way. Enjoy a lightweight, purely text-based approach to terminal recording.

Contains [App::Mi6](https://github.com/skaji/mi6) for building skeleton of **Raku** packages.

Also contains [PyScaffold](https://github.com/blue-yonder/pyscaffold) for building skeleton of Python packages.


## How to run using [Binder](https://mybinder.org/) ?


+ Click the Binder icon <a href="https://mybinder.org/v2/gh/sumanstats/raku-notebook/master"><img src="imgs/binder-logo.svg" width="260" height="150" align="right"></a>

+ Wait a few seconds.
+ Select `New` -> `Raku`

And dive into the **Raku notebook**.


## How to run this image in your local computer ?

Type `docker run -it -p 8888:8888 sumankhanal/raku-notebook` in the docker terminal and access it in your browser with
`docker_ip_address:8888`.

There you are running the notebook.

For detailed instructions, [see here](https://sumankhanal.netlify.app/post/raku/raku_notebook/).


Once you follow the above instructions, you will get notebook as shown here:

![](https://github.com/sumanstats/raku-notebook/blob/master/imgs/notebook.PNG)

Feedback welcome !


