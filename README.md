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
does for StyleGAN and 
[this blog](https://affinelayer.com/pixsrv/)
does for pix2pix.


## Did I already mention...?

All this stuff usually happens in
the terminal. Some people also call it
the command line, bash, or the shell.
There are subtle differences between
those names that we will ignore for 
today. 
* On Mac, you can open a terminal
by using the spotlight (`Cmd+Space`)
and typing in `terminal`
    * open a new
terminal tab with `Cmd+T`
    * close current
tab with `Cmd+W` an
    * close the terminal
by typing `Cmd+Q`
* On Ubuntu,
you can open a terminal by typing
`Ctrl+Alt+T`
    * open a new tab with 
`Ctrl+Shift+T`
    * and close a tab by
typing `exit` - this will also close
the terminal, if the last tab is exited.


Mac and Linux share most of the commands
in the terminal, so if you know your way
around in one operating system, you will
already have a huge head start with the 
other. This does not apply to Windows, 
though. Here, the instruction set is very
different and I don't know much about
it `¯\_(ツ)_/¯`.


## Why bother?

But why should you even bother going 
through all this trouble with the
terminal? Well, two reasons. First, if
you really want to take control over
the tools that are available as open
source projects on the internet, the
terminal gives you access on a very
detailed level. Second, since machine
learning centers around having lots
and lots of data handy, it is very
helpful, if not crucial to the success
of a project, to be able to move, 
copy, evaluate and manipulate data
fast. Imagine going through an image
folder of 2000 images and checking
manually if they are all of the same
size. A command line script can do
that for you in 3 lines. Unfortunately,
a command line script can also easily
overwrite, corrupt or delete your data,
and usually not in a way that you could
restore it from the waste bin. With
great power comes great responsibility.
On the other hand, if your project does
not need to have much control over the
data or the script, then it might just
be fine to just skim over the details
and use a well-tested tool with a nice 
user interface.

## Your turn.

As a small exercise and to prepare for
Wednesday, use the break to install
[git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git), 
[python](https://realpython.com/installing-python/),
and [anaconda](https://docs.anaconda.com/anaconda/install/). 
Then [clone](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)
this git repository to your computer
and try to run `hello_world.py`. It
probably won't. Figure out what's 
missing and [use anaconda to configure
a virtual environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands)
so you can
run the script.



