# CitizenOne Documentation

This docuumentation is built with Sphinx and the compiled version can be found on http://docs.vivvo.com

For the people contributing to this documentation, please refer to the instructions below for adding content.

## Start Contributing to Documentation

#### Create a Branch
1. On GitHub, navigate to the main page of the repository.
2. Type a unique name for your new branch.
3. Press Enter.

[Read more on creating a branch here](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/).

#### Editing Documentation

1. Go to [docs/source](docs/source) to view exist documents.
2. Create and Edit the files that you want to update.

[Read more on creating and editing files here](docs/source).

#### Create a Pull Request

You can open a pull request to the upstream repository from any branch or commit in your fork.

1. On GitHub, navigate to the [main page](/) of the repository.
2. Branch dropdown menuIn the "Branch" menu, choose the branch that contains your commits.
3. To the right of the Branch menu, click New pull request.
4. Use the base branch dropdown menu to select the branch you'd like to merge your changes into, then use the compare branch drop-down menu to choose the topic branch you made your changes in.
5. Type a title and description for your pull request.
6. Click Create pull request.

[Read more on creating a pull request here](https://help.github.com/articles/creating-a-pull-request/).

#### Create a Pull Request from Fork

You can open a pull request to the upstream repository from any branch or commit in your fork.

1. Navigate to the original repository you created your fork from.
2. To the right of the Branch menu, click New pull request.
3. On the Compare page, click compare across forks.
4. Confirm that the base fork is the repository you'd like to merge changes into. Use the base branch drop-down menu to select the branch of the upstream repository you'd like to merge changes into.
5. Drop-down menus for choosing the head fork and compare branchUse the head fork drop-down menu to select your fork, then use the compare branch drop-down menu to select the branch you made your changes in.
6. Type a title and description for your pull request.
7. If you do not want to allow anyone with push access to the upstream repository to make changes to your PR, unselect Allow edits from maintainers.
8. Click Create pull request.

[Read more on creating a pull request from a fork here](https://help.github.com/articles/creating-a-pull-request-from-a-fork/).


## Getting Development Started with Sphinx

Sphinx is a powerful documentation generator that
has many great features for writing technical documentation including:

* Generate web pages, printable PDFs, documents for e-readers (ePub),
  and more all from the same sources
* You can use reStructuredText or :ref:`Markdown <intro/getting-started-with-sphinx:Using Markdown with Sphinx>`
  to write documentation
* An extensive system of cross-referencing code and documentation
* Syntax highlighted code samples
* A vibrant ecosystem of first and third-party extensions_

.. _extensions: http://www.sphinx-doc.org/en/master/ext/builtins.html#builtin-sphinx-extensions


#### Quick start video

This screencast will help you get started or you can
:ref:`read our guide below <intro/getting-started-with-sphinx:Quick start>`.

.. raw:: html

    <div style="text-align: center; margin-bottom: 2em;">
    <iframe width="100%" height="350" src="https://www.youtube.com/embed/oJsUvBQyHBs?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>


#### Quick start

Assuming you have Python already, `install Sphinx`_:

.. sourcecode:: bash

    $ pip install sphinx

Create a directory inside your project to hold your docs:

.. sourcecode:: bash

    $ cd /path/to/project
    $ mkdir docs

Run ``sphinx-quickstart`` in there:

.. sourcecode:: bash

    $ cd docs
    $ sphinx-quickstart

This quick start will walk you through creating the basic configuration; in most cases, you
can just accept the defaults. When it's done, you'll have an ``index.rst``, a
``conf.py`` and some other files. Add these to revision control.

Now, edit your ``index.rst`` and add some information about your project.
Include as much detail as you like (refer to the reStructuredText_ syntax
or `this template`_ if you need help). Build them to see how they look:

.. sourcecode:: bash

    $ make html

Your ``index.rst`` has been built into ``index.html``
in your documentation output directory (typically ``_build/html/index.html``).
Open this file in your web browser to see your docs.

.. figure:: ../_static/images/first-steps/sphinx-hello-world.png
    :align: right
    :figwidth: 300px
    :target: ../_static/images/first-steps/sphinx-hello-world.png

    Your Sphinx project is built

Edit your files and rebuild until you like what you see, then commit your changes and push to your public repository.
Once you have Sphinx documentation in a public repository, you can start using Read the Docs
by :doc:`importing your docs </intro/import-guide>`.

.. _install Sphinx: http://sphinx-doc.org/latest/install.html
.. _reStructuredText: http://sphinx-doc.org/rest.html
.. _this template: https://www.writethedocs.org/guide/writing/beginners-guide-to-docs/#id1

Using Markdown with Sphinx
--------------------------

You can use Markdown and reStructuredText in the same Sphinx project.
We support this natively on Read the Docs, and you can do it locally:

.. sourcecode:: bash

    $ pip install recommonmark

Then in your ``conf.py``:

.. code-block:: python

    from recommonmark.parser import CommonMarkParser

    source_parsers = {
        '.md': CommonMarkParser,
    }

    source_suffix = ['.rst', '.md']

.. warning:: Markdown doesn't support a lot of the features of Sphinx,
          like inline markup and directives. However, it works for
          basic prose content. reStructuredText is the preferred
          format for technical documentation, please read `this blog post`_
          for motivation.

.. _this blog post: http://ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/


#### External resources

Here are some external resources to help you learn more about Sphinx.

* `Sphinx documentation`_
* `RestructuredText primer`_
* `An introduction to Sphinx and Read the Docs for technical writers`_

.. _Sphinx documentation: http://www.sphinx-doc.org/
.. _RestructuredText primer: http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
.. _An introduction to Sphinx and Read the Docs for technical writers: http://ericholscher.com/blog/2016/jul/1/sphinx-and-rtd-for-writers/
