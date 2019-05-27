This is the deep reinforcement learning project for CS 182 / 282A
(Designing, Visualizing, and Understanding Deep Neural Networks) at Berkeley for
Spring 2019.

**Important note**: the DQN part for Pong may take a long time to run and
evaluate, especially without a GPU. Please start coding early!


## Installing

We have tested this code on the following systems:

- Python 3.5.2 and Ubuntu 16.04
- Python 3.6.3 and OS X 10.13.6

To get started, 
(1) create a virtualenv:
```bash
virtualenv .env --python=python3
````
(2) activate a virtualenv:
```bash
source .env/bin/activate
```
(3) install packages in the virtualenv, like this:

```
pip install -r requirements_gpu.txt
```

If you are not using a GPU, run this instead:

```
pip install -r requirements.txt
```

We have tested the code using the exact package versions as described in the
requirements file, but it is likely that minor version changes will still be
OK.


## Usage and Submitting the project

There are two Jupyter notebooks, one for Policy Gradients and the other for Deep
Q-networks. Make sure you complete those. For grading purposes, each is worth
half of the grade.

To submit the project, run

```
bash prepare_project.sh
```

and submit the zipped file to bCourses. If the script doesn't work, adjust
permissions via:

```
chmod +x prepare_submission.sh
```

and try again.

The entire zipped file should be on the order of 10MB in size. If it's much
larger than that, check if you have older models saved in `data_pg` and
`data_dqn` that you are not using for evaluation. These can be deleted, as we're
only interested in the models that you used for evaluation and to generate your
plots in the notebooks.


## Acknowledgments

The starter code is a mix of code provided by various researchers at Berkeley
and OpenAI, including at least Szymon Sidor, John Schulman, Sergey Levine,
Abhishek Gupta, Joshua Achiam, Michael Chang, and Soroush Nasiriany.
