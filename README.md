# Data Analytics and Visualization — Course Setup

Everything you need to get your environment running for this course.
Follow the steps in order. This takes about 10 minutes the first time.

## What you need first

- Anaconda or Miniconda installed
- Visual Studio Code installed
- The Python and Jupyter extensions installed in VS Code

If you do not have conda yet, install Miniconda from
https://docs.conda.io/en/latest/miniconda.html

## Step 1: Get the course folder

Download or clone this folder to your computer. Remember where you put it.

## Step 2: Open a terminal in the course folder

Open Anaconda Prompt (Windows) or your terminal (Mac), then move into
the course folder. For example:

    cd path/to/data-analytics-course

The folder you are in should contain the file environment.yml.

## Step 3: Build the environment

Run this once:

    conda env create -f environment.yml

This creates an environment named "analytics" with every package the
course uses. It will take a few minutes. You only do this one time.

## Step 4: Activate it

    conda activate analytics

You will see (analytics) appear at the start of your terminal line.
That means it worked.

## Step 5: Point VS Code at it

1. Open any .ipynb notebook in this course folder in VS Code.
2. Click the kernel picker in the top-right corner of the notebook.
3. Choose "analytics (Python 3.12)".

## Step 6: Confirm everything works

Run this in a notebook cell:

    import pandas, numpy, sklearn, seaborn, statsmodels, matplotlib
    print("Environment ready")

If it prints "Environment ready" with no error, you are set for the
semester.

## If the instructor updates the environment

Sometimes a later module needs a new package. When that happens, you
will be told to re-sync. From the course folder, run:

    conda env update -f environment.yml --prune

## Common problems

- "conda: command not found" — open Anaconda Prompt instead of a plain
  terminal, or reinstall Miniconda and restart your terminal.
- The "analytics" kernel does not show up in VS Code — make sure the
  Python and Jupyter extensions are installed, then restart VS Code.
- A package is missing — confirm your notebook kernel says "analytics"
  in the top-right corner, not "base" or a global Python.
