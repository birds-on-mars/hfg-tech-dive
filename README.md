# hfg-tech-dive

## Fantastic Algorithms and where to find them 

Machine learning tools come in
various shapes and forms, and some
are available in a ready-to-use
package. [**RunwayML**](https://runwayml.com/) provides
a collection of such tools. Not all
current tools are available though and
some need to be paid for. To take full
control over the scripts you are using,
you can go directly to the source.

Most machine learning tools are
developed, updated and distributed
via github. **[github](https://github.com/)**
is a hosting service where you can
host **git repositories**. 

[**git**](https://git-scm.com/) is a software
that lets developers organise their code
base in a way that keeps track of different
versions of the code - it's like saving
the state of a whole directory, so you can
restore previous versions of your project.
git doesn't store the files on your computer
alone, but puts them on a server where the
server can handle back-ups and where other
developers can pull the newest version of
the project or push their addition to the
project to. git is **version control**, **back-up**,
and **collaborative workspace** all in one.
A folder that is tracked by git is called 
a **git repository**.

A git repository hosted on github can be
accessed either by the web front end through
your browser or by the git software, usually
from the terminal. From the website, you can
download the files and run the script. If
you instead use git to access the repository,
you also get the project history, different
versions and updates in the future.

Install git following these 
[instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

## StyleGAN

Let's have a look at the 
[StyleGAN landing page](https://nvlabs.github.io/stylegan2/versions.html).
It links to a github-repo with the code
as well as to a repo with the *data set*
plus a scientific paper explaining the
algorithm from a conceptual point of
view. The video previews can give you
an indication about whether this algorithm
is useful for your project or not.

## Ingredients of a Machine Learning Algorithm

A ml-algorithm usually consists of three parts:
the code, the data set, and the model. The code
either uses the data set to train the model or
it uses a model to make the model do what it
was trained for. You can either use an existing
model for your project, which is rather easy.
Interesting results can be achieved by using
the model in an unintended way, by hacking the
model. Or you can train your own model, which
is rather hard but gives you deeper control
over how the model will integrate into your
project.

## Where do I begin?

Now you have access to a script that looks
promising. How do you start it? Most algorithms
are written in a programming language called
`python`. To start `python`, go to your terminal
and type in `python`. If `python` is already
installed on your machine, this opens an
interactive session where you can type python
code and it will immediately be evaluated. If
`python` is not yet installed on your machine,
follow 
[these](https://realpython.com/installing-python/) 
instructions.

Additionally, most machine learning scripts
make extensive use of code that has already
be written and manages standard tasks of 
certain domains, so-called *libraries* or
*frameworks*. Depending on the script you are
running, you might need to get a few of those,
too. Notable libraries for machine learning
are `tensorflow`, `numpy`, `scipy`, `torch`, 
`keras`, and many more. Unfortunately, the
requirements of some scripts might collide,
for example if one script depends on
`tensorflow v1.0` and another script depends
on `tensorflow v2.1` - which version should
you then install? Well, to manage different
dependencies, people use *virtual environments*.
With tools like `anaconda` or `virtualenv`
you can activate an environment from scratch
and install all dependencies needed for
a given script. If you then want to run 
another script with conflicting dependencies,
you can deactivate that first environment,
activate a new one and install the
dependencies as needed. You will end up
with different environments for different
scripts, and you can switch between those
depending on which script you want to run.

## But really, how do I begin?

With python in place, your virtual
environments preconfigured and the git
repository cloned to your hard drive,
to run a script, you have to activate
the respective virtual environment
and then run the script by calling 
the main `.py`-file with python like so:
```
python generate_figures.py
```
The name of the main file might differ
and there might be different files to
run for different tasks, as for example
the StyleGAN repository has a separate
file for starting the training. Also,
the behaviour of a script can usually
modified by either setting the options
in a *configuration file* (often called
`config.py`) or calling the script
with so-called *flags*, or both.
Calling a script with flags looks like 
this:
```
python pix2pix.py --mode train --output_dir facades_train
``` 
Usually a repository comes with a 
README-file that gives more or less
detailed information on how to set
options for a given script. If the 
script had a lot of exposure on the
internet, you also might find
accompanying blog posts that might give
hints on successful use, as for example
[this blog](https://www.gwern.net/Faces)
does for StyleGAN.







