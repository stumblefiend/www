A beginner's guide to writing documentation
===========================================

.. note:: This is a write up of a `Presentation <https://speakerdeck.com/ericholscher/writing-docs-a-beginners-guide-to-writing-documentation>`_ .
          Please provide feedback to `@ericholscher`_.
          You can view the source on `GitHub`_.

.. _@ericholscher: http://twitter.com/ericholscher
.. _GitHub: https://github.com/writethedocs/www/blob/master/docs/guide/writing/beginners-guide-to-docs.rst

..

	| Camera pans from stage left.
	| It shows a text editor, open to a blank page.
	| A person hunched in front, head to desk.

The scene above is well known to everyone who writes for a living;
the mixed emotions of a blank page.
Full of excitement, fresh with a new beginning.
Yet also full of despair, where do you even start?

I am here to stop this scene from playing out.

This is a guide to documenting your first project.
The first time is always the hardest,
and I hope this guide will get you started down the righteous path.
At the end,
you should have a project that is ready for public release.

Feel free to read this document straight through,
or simply use it as a reference.

.. _why:

Why write docs
--------------

You will be using your code in 6 months
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Code that you wrote 6 months ago looks similar to code that someone else wrote.

As you untangle things that were once obvious months ago,
you will start to empathize with your users who need good documentation.

Documentation allows you to transfer the *why* behind code.
Much like how code comments explain the *why*,
and not the *how*.

.. sidebar::  Sidebar on open source

	There is a magical feeling that happens when you release your code.
	It comes in a variety of ways, but it always hits you the same.
	*Someone is using my code?!*
	A mix of terror and excitement.

		| I made something of value!
		| What if it breaks?!
		| I am a real open-source developer!
		| Oh god, someone else is using my code...

	Writing good documentation helps alleviate the fear that comes from putting something into the world.
	My favorite quote about this is something along these lines:

		| Fear is what happens when you're doing something important.
		| If you are doing work that isn't scary,
		| it isn't improving you or the world.

	Congrats on being afraid!
	It means you're doing something important.

You want people to use your code
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Documentation helps people see why your code is useful for them. Common reasons they
won't use your code include:

* They don't know why your project exists or how it relates to their needs.
* They can't find how to install your code.
* They can't see how to use your code.

There are decreasingly few people who will source dive and use any code out there
compared to the number of people who will use properly documented code.
If you love your project, document it so others can use it.

You want people to help out
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Open source is amazing in many ways,
but potential contributors need guidance through documentation.

Also, documentation provides another way for people to contribute.
For people who have never contributed, documentation changes are less scary than code changes.
Without documentation, you'll miss out on a whole class of contributors and impede others.

You want your code to be better
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Documentation requires a distillation of thought that improves code design.
Writing out API and design decisions allows you to formally think about them.
It also allows people to contribute code that follows your original intentions.

You want to be a better writer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Technical writing is an art that doesn't come naturally. Writing documentation requires different writing skills than most people have.  
Writing documentation allows you to be a better technical writer, a useful skill for programmers.

Writing becomes easier over time. Keep up your writing skill by documenting your projects.

Starting simple is the best way to achieve actual results.
Writing tools should be powerful and easy to use to remove obstacles to putting words on the page.

.. _markup_languages:

.. sidebar:: Sidebar on markup languages.

   The examples in this document are both valid `Markdown`_ and `reStructuredText`_.
   reStructuredText is a bit harder to use,
   but is more powerful. Check them both out.

.. _reStructuredText: https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
.. _Markdown: http://daringfireball.net/projects/markdown/

Version-controlled plain text
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Programmers live in a world of plain text.
Their documentation tooling and workflows should function similarly.
Tools should turn plain text into pretty HTML and track changes to files.

Basic example
~~~~~~~~~~~~~

::

	Resources
	---------

	* Online documentation: http://docs.writethedocs.org/
	* Conference: http://conf.writethedocs.org/

This will render a nice HTML header and a list.
The URLs will be hyperlinked automatically.
It's easy to write and
still makes sense as plain text.

README
~~~~~~

Your project's README is often the first time users interact with your project.
Code hosting services will automatically render your README into HTML if you provide the proper extension.
Having a solid README will serve your project well.

Some people even go as far as to `start your project with a README`_.

.. _start your project with a README: http://tom.preston-werner.com/2010/08/23/readme-driven-development.html

.. _write:

What to write
-------------

Now we're getting down to the brass tacks.
Making sure that you give your users all the information that they need,
but not too much.

First, ask yourself who you're writing for.
At first, you generally just need to appeal to two audiences:

* Users
* Developers

Users are people who simply want to use your code,
and don't care how it works.
Developers are people who want to contribute back to your code.

What problem your project solves
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A lot of people will come to your docs trying to figure out what exactly your project is. Someone will mention it, or they'll google a phrase randomly. You should explain what your project does and why it exists. Fabric_ does a great job of this.

.. _Fabric: http://docs.fabfile.org/

A small code example
~~~~~~~~~~~~~~~~~~~~

Show a telling example of what your project would normally be used for. Requests_ does a great example of this.

.. _Requests: https://requests.kennethreitz.org/en/master/

A link to your code & issue tracker
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

People like to browse the code sometimes. They might be interested in filing bugs against the code for issues they've found. Make it really easy for people who want to contribute back to the project in any way possible. I think the `Python Guide`_ does a good job with the link to the code portion.

.. _Python Guide: http://docs.python-guide.org/en/latest/index.html

Frequently asked questions (FAQs)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A lot of people have the same problems. If things happen all the time, you should probably fix your documentation or the code, so that the problems go away. However, there are always questions that get asked about your project, things that can't be changed, etc. Document those, and **keep it up to date**. FAQs are generally out of date, but when done well, they are a golden resource. Tastypie_ did a great job with this, with their "Cookbook" concept.

.. _Tastypie: http://django-tastypie.readthedocs.org/en/latest/cookbook.html

How to get support
~~~~~~~~~~~~~~~~~~

Mailing list? IRC Channel? Document how to get help and interact with the community around a project. Django_ does a great job with this.

.. _Django: https://docs.djangoproject.com/en/1.8/faq/help



Information for people who want to contribute back
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

People usually have standards for how they expect things to be done in their projects. You should document these so that if people write code, they can do things in the norm of the project. `Open Comparison`_ does a great job of this.

.. _Open Comparison: https://packaginator.readthedocs.io/en/latest/contributing.html


Installation instructions
~~~~~~~~~~~~~~~~~~~~~~~~~

Once people figure out whether they want to use your code or not, they need to know how to actually get it and make it run. Hopefully your install instructions should be a couple lines for the basic case. A page that gives more information and caveats should be linked from here if necessary. I think at `Read the Docs`_ we do a good job with this.

.. _Read the Docs: http://read-the-docs.readthedocs.org/en/latest/install.html


Your project's license
~~~~~~~~~~~~~~~~~~~~~~~

BSD? MIT? GPL? This stuff might not matter to you, but the people who want to use your code will care about this a whole lot. Think about what you want to accomplish with your license, and please only pick one of the standard licenses that you see around the web.

.. _template:


Next steps
----------

After you follow the above guide,
we know your project will be successful!
For further reading,
check out this post on `how to maintain an open source project`_.

.. _how to maintain an open source project: https://medium.com/p/aaa2a5437d3a

Template
--------

A simple template for you to start with,
for your ``README``.
Name the file ``README.md`` if you want to use markdown,
or ``README.rst`` if you want to use reStructuredText.
More information about these can be found in the :ref:`sidebar on markup <markup_languages>`.

::

	$project
	========

	$project will solve your problem of where to start with documentation,
	by providing a basic explanation of how to do it easily.

	Look how easy it is to use:

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

	If you are having issues, please let us know.
	We have a mailing list located at: project@google-groups.com

	License
	-------

	The project is licensed under the BSD license.









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

Conversations with experts help highlight the workflows to cover and the product features or technical concepts to explain. You might also get ideas about organizing and presenting the details.  For example:

* For a product that first needs installation, a system administrator audience may benefit from seeing several installation scenarios or complex scenarios compared to a less technical audience.
* A GUI application that offers specific ways for users to accomplish each task might need a step-by-step guide through those workflows. 
* A product with many APIs might need an alphabetical listing and description of what each API does for quick reference. 

Overall, understanding the product and the expected user base helps define *what* to write about and *how* to write about it.

