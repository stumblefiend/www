A beginner's guide to writing open source documentation
=========================================================

Professional writers know the mixed emotions of a blank page: 
you're eager for a new beginning but despair at where to start.

Have no fear! Use this guide to document your first open-source project for 
public release. 

.. _why:

Why write docs
--------------

You will use your code in 6 months
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Your code from 6 months ago looks like code that someone else wrote.
Once obvious things are now unclear. You can now empathize with your 
users who need good documentation.

Documentation allows you to transfer the *why* behind code.
Much like how code comments explain the *why*,
and not the *how*.

.. sidebar::  Sidebar on open source

	There is a magical feeling that happens when you release your code.
	*Someone is using my code?!*
	A mix of terror and excitement.

	Good documentation helps alleviate the fear of putting something into the world. And remember, that fear means you are doing something important to improve yourself or the world.

You want people to use your code
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Documentation shows people why your code is useful. There are a few 
common reasons people don't use your code:

* They don't know why your project exists or how it relates to their needs.
* They can't find how to install your code.
* They can't see how to use your code.

Few people will source dive and use any code out there, but most people
people will use properly documented code.
If you love your project, document it so others can use it.

You want people to help out
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Potential contributors need guidance through documentation and documentation provides another way for people to contribute.
Also, for people who have never contributed, documentation changes are less scary than code changes.
Overall, without documentation, you impede or even lose contributors.

You want your code to improve
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Documentation requires a distillation of thought that improves code design.
Writing out API and design decisions allows you to formally think about them.
It also allows people to contribute code that follows your original intentions.

You want to write better
~~~~~~~~~~~~~~~~~~~~~~~~~

Technical writing is a useful skill for programmers, but it doesn't come naturally. 
Writing documentation requires different writing skills than most people have and
allows you to be a better technical writer.

Writing becomes easier over time. Keep up your writing skill by documenting your projects.

Starting simple is the best way to achieve results.

Version-controlled plain text
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Programmers live in a world of plain text.
Their documentation tooling and workflows should function similarly.
Tools should turn plain text into pretty HTML and track changes to files.

Basic example
++++++++++++++

::

	Resources
	---------

	* Online documentation: http://docs.writethedocs.org/
	* Conference: http://conf.writethedocs.org/

This will render a nice HTML header and a list with automatically hyperlinked URLs.
It's easy to write and still makes sense as plain text.

Writing tools should be powerful and easy to use to remove obstacles to putting words on the page.

.. _markup_languages:

.. sidebar:: Sidebar on markup languages.

   The examples in this document are both valid `Markdown`_ and `reStructuredText`_.
   reStructuredText is a bit harder to use,
   but is more powerful. Check them both out.

.. _reStructuredText: https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
.. _Markdown: http://daringfireball.net/projects/markdown/

.. _write:

What to write
-------------

Give your users the information that they need,
but not too much.

First, know which of these common audiences you're writing for:

* Users - want to use your code and don't care how it works.
* Developers - want to contribute to your code.

Tell what problem your project solves
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Many people will use your docs to learn what your project is. 
Perhaps they will hear about your project from others or will find it from a search engine. 
Regardless, clearly state what your project does and why. Fabric_ does a great job of this.

.. _Fabric: http://docs.fabfile.org/

A small code example
~~~~~~~~~~~~~~~~~~~~

Show a common example use case for your project. Requests_ is a great example.

.. _Requests: https://requests.kennethreitz.org/en/master/

A link to your code & issue tracker
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

People sometimes like to browse the code. They might want to file bugs for issues they've found, 
so make your code easy to contribute. The `Python Guide`_ does a good job of this.

.. _Python Guide: http://docs.python-guide.org/en/latest/index.html

Frequently asked questions (FAQs)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Many people have the same problems. If certain issues happen often, fix your documentation or the code 
to resolve the issues. However, there are always questions about your project, things that can't be changed, etc. 
Document those and **keep them up to date**. FAQs get outdated fast, but they are a great resource when done well. Tastypie_ did a great job of this with their "Cookbook" concept.

.. _Tastypie: http://django-tastypie.readthedocs.org/en/latest/cookbook.html

How to get support
~~~~~~~~~~~~~~~~~~

Whether it is a mailing list or IRC Channel, document how to get help and interact with the community. 
Django_ does a great job at this.

.. _Django: https://docs.djangoproject.com/en/1.8/faq/help

Information for people who want to contribute
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

People have expectations of how things should be done. Document these so that people write code in the norm of the project. 
`Open Comparison`_ does a great job of this.

.. _Open Comparison: https://packaginator.readthedocs.io/en/latest/contributing.html

Installation instructions
~~~~~~~~~~~~~~~~~~~~~~~~~

Once people decide whether to use your code, they need to know how to install and run it. Your install instructions should be a couple of lines for the basic case. Link to a page with more information and caveats. `Read the Docs`_ does a good job with this.

.. _Read the Docs: http://read-the-docs.readthedocs.org/en/latest/install.html


Your project's license
~~~~~~~~~~~~~~~~~~~~~~~

BSD? MIT? GPL? A project's license might not matter to you, but the people who want to use your code will care. Think about what you want to accomplish with your license and only pick one standard license.

.. _template:

Next steps
----------

After following this guide,
we know your project is ready for success!
But, if you'd like to learn more,
see `how to maintain an open source project`_.

.. _how to maintain an open source project: https://medium.com/p/aaa2a5437d3a

README template
----------------

Your project's README is often the first time users interact with your project. Therefore, having a solid README is key.
Code hosting services automatically render your README into HTML if you provide the proper extension.

Some people even `start a project with a README`_.

.. _start a project with a README: http://tom.preston-werner.com/2010/08/23/readme-driven-development.html

Below is a simple ``README`` template to start with.
Name the file ``README.md`` to use markdown,
or ``README.rst`` to use reStructuredText.

Find more details in the :ref:`sidebar on markup <markup_languages>`.

::

	$project
	========

	$project solves the problem of where to start with documentation
	by providing a basic explanation of how to do it easily:

	    import project
	    # Get your stuff done
	    project.do_stuff()

	Features
	--------

	- Be awesome
	- Make things faster

	Installation
	------------

	Install $project by running:

	    install project

	Contribute
	----------

	- Issue Tracker: github.com/$project/$project/issues
	- Source Code: github.com/$project/$project

	Support
	-------

	Let us know if you have issues.
	See our mailing list at: project@google-groups.com

	License
	-------

	The project is licensed under the BSD license.

.. note:: This is a write up of a `Presentation <https://speakerdeck.com/ericholscher/writing-docs-a-beginners-guide-to-writing-documentation>`_ .
          Please provide feedback to `@ericholscher`_.
          You can view the source on `GitHub`_.

.. _@ericholscher: http://twitter.com/ericholscher
.. _GitHub: https://github.com/writethedocs/www/blob/master/docs/guide/writing/beginners-guide-to-docs.rst

..







============
Starting off
============

how do you write docs and how do you get the time to write docs?
What should you be striving for with those docs?
Here are tactics for a few different groups.

Open-source developers
----------------------

Good documentation improves the chances of discovery and use of your awesome open-source code.

Start with the :doc:`writing/beginners-guide-to-docs`,
which provides practical advice on getting started.

Developers at a company
-----------------------

Here are some ways to show value to your boss and justify writing documentation for your project despite tight deadlines:

Get started with :doc:`writing/mindshare`,
for a blueprint for implementing a documentation solution at your company.

Enterprise users
----------------

For a SAAS or Services company with developers as your target
audience, lack of great documentation will increase your support costs and give an advantage to competitors that have great documentation.

See :ref:`interesting-approaches` for examples of good documentation.













Starting new documentation for an unfamiliar product
=====================================================

Where should you start when writing new documentation for an unfamiliar product?

A solid first step is talking to the product experts (developers, product managers, or project managers) to learn the product and its expected audience. Answers to questions such as the following can help you decide what details to focus on in the documentation:

* What does the product do and what does it enable users to achieve?
* What user base or business role does this product cater to and what do those users care about?

Conversations with experts help highlight the workflows to cover and the product features or technical concepts to explain. You might also get ideas about organizing and presenting the details. For example:

* For a product that first needs installation, a system administrator audience may benefit from seeing several installation scenarios or complex scenarios compared to a less technical audience.
* A GUI application that offers specific ways for users to accomplish each task might need a step-by-step guide through those workflows. 
* A product with many APIs might need an alphabetical listing and description of what each API does for quick reference. 

Overall, understanding the product and the expected user base helps define *what* to write about and *how* to write about it.

