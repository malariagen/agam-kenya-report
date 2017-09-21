# agam-kenya-report

This is a work in progress. It has not been reviewed, approved or
endorsed by anyone. If you have any questions, please contact Alistair
Miles (alimanfoo@googlemail.com), Nick Harding (njh@well.ox.ac.uk) or
Janet Midega (tjmidega@yahoo.com).

## Contributor guide

### Getting started

The following steps describe how to set up a development environment
for working on the manuscript and the supporting notebooks.

**Step 1**: Fork this repository into your own GitHub account.

**Step 2**: Clone your fork to your local system. E.g.:

```bash
$ git clone git@github.com:username/agam-kenya-report-2017.git
$ cd agam-kenya-report-2017
$ git submodule update --init --recursive
$ git remote add upstream git@github.com:malariagen/agam-kenya-report-2017.git
```

...replacing 'username' with your GitHub username.

**Step 3**: Install dependencies (TeX Live, Miniconda):

From the repo working directory, run:

```bash
$ ./agam-report-base/install/install.sh
```

This will install Tex Live and Miniconda into the ``dependencies``
directory within the repository root directory.

### Running a Jupyter notebook server

The install script will install Miniconda locally and create an
environment with various scientific Python packages installed. To launch 
a Jupyter notebook server:

```bash
$ source env.sh
$ jupyter notebook
```

### Installing Python or TeX Live packages

If there are additional Python packages that you need to install that
are not already installed via the install script, please add them to
the relevant file in the agam-report-base submodule. If the package is
available via conda, add the dependency to the file
``agam-report-base/install/conda.txt``. If the package is only
available via PyPI, add to the file
``agam-report-base/install/pypi.txt``.

If there are additional TeX Live packages that you need to install,
add them to the file ``agam-report-base/install/texlive.packages``.

Once you have added the new dependencies to the relevant file, rerun
the install script:

```bash
$ ./agam-report-base/install/install.sh
```

Please also submit these changes back to the agam-report-base via a
pull request.
