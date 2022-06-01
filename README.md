<h1 align="center">FireWorks/Atomate Tutorial</h1>

**:warning: WARNING:** This tutorial does not provide any licensed code or file.

## Introduction
[FireWorks](https://materialsproject.github.io/fireworks/) is a free, open-source code for defining, managing, and executing scientific workflows. It can be used to automate calculations over arbitrary computing resources, including those that have a queueing system.

[Atomate](https://atomate.org) makes it possible to perform complex materials science computations using very straightforward statements.

[Pymatgen](https://pymatgen.org) is a robust, open-source Python library for materials analysis.

## Content

- `fireworks_tutorial.ipynb`: Basic introduction to FireWorks with simple examples from their documentation.

- `fireworks_tutorial_vasp.ipynb`: FireWorks/Atomate tutorial for materials science (VASP).

- `fireworks_tutorial_fakevasp.ipynb`: Same tutorial but using RunFakeVasp (FireTask) instead of VASP code.

## Guide for webgui
[laikapack side]
1. launch a notebook with an image kubeflow_vasp:atomate_stack (atomate, mongodb, pymatgen)
2. set config file (copy the whole atomate directory at home directory): cp -r atomate/ ../
3. make mongod run in the background: mongod --quiet>/dev/null & python /home/jovyan/atomate/config/db_reset.py
4. launch a web gui: lpad webgui --port 27020 

[local side]
1. create fw_webgui.yml file (refer to the reply for the information which should be written in the file)
2. create a service: kubectl create -f fw_webgui.yml (can confirm whether it's launched with kubectl get services )
3. port-forwarding: kubectl port-forward <notebook name> 8000:27020

## Citation

There is no citation! Feel free to fork (:fork_and_knife:) and leave a start (:star:)
