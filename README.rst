####################
IS 210 Assignment 05
####################
******************
Synthesizing Tasks
******************

:College: CUNY School of Professional Studies
:Course-Name: Software Application Programming I
:Course-Code: IS 210
:Points: 10
:Due-Date: YYYY-MM-DDTHH:mm:ss

Overview
========

[overview]

Instructions
============

The following tasks will either have you interacting with existing files in
the assignment repository or creating new ones on the fly. Don't forget to add
your interpreter directive, utf-8 encoding, and a short docstring with any new
files that you create!

.. important::

    In these exercises, you may, on occasion, come across a task that requres
    you to research or use a function or method not directly covered by the
    course text. Since Python is such a large language it would be impossible
    for the author to have included descriptions of each and every available
    function which would largely duplicate the offical Python documentation.

    A *vital* skill to successful programming is being comfortable searching
    for and using official language documentation sources like the
    `Python String Documentation`_ page. Throughout our coursework we will be
    practicing both the use of the language in practice and the search skills
    necessary to become functional programmers.

Synthesizing Tasks
==================

Our final tasks this week explores a more complex case of using multiple
functions, chained together to reduce repetition.

Task 01
-------

Converting a Fahrenheit temperature to Celsius.

Specifications
^^^^^^^^^^^^^^

1.  Create a new file named ``task_01.py``

2.  Create a function called ``fahrenheit_to_celsius()`` that has one parameter:

    1.  ``degrees``

3.  Use the following formula to convert the degrees Fahrenheit to a *decimal*
    representation of degrees Celsius

    1. Deduct 32 from ``degrees``, then multiply by 5, then divide by 9

4.  Return the temperature as a decimal in degrees Celsius

Examples
^^^^^^^^

.. code:: pycon

    >>> fahrenheit_to_celsius(212)
    Decimal('100')

Task 02
-------

Converting a Celsius temperature to Kelvin.

Specifications
^^^^^^^^^^^^^^

1.  Open ``task_01.py``

2.  Below your ``import`` statement but above any function definitions, create
    a new constant called ``ABSOLUTE_DIFFERENCE`` and set it's value to a
    *decimal* of ``273.15``

3.  Create a second function called ``celsius_to_kelvin()`` that has one
    parameter:

    1.  ``degrees``

4.  Use the following formula to convert the degrees Celsius to degrees Kelvin:

    1.  add ``ABSOLUTE_DIFFERENCE`` to ``degrees``

5.  Return the temperature as a decimal in degrees Kelvin

Examples
^^^^^^^^

.. code:: pycon

    >>> celsius_to_kelvin(100)
    Decimal('373.15')

Task 03
-------

Converting a Fahrenheit temperature to Kelvin.

Specifications
^^^^^^^^^^^^^^

1.  Open ``task_01.py``

2.  Create a third and final function ``fahrenheit_to_kelvin()`` that has one
    parameter:
    
    1.  ``degrees``

3.  Use ``fahrenheit_to_celsius()`` and ``celsius_to_kelvin()`` to convert
    Fahrenheit temperatures to Kelvin and return the result as a number.

Examples
^^^^^^^^

.. code:: pycon

    >>> fahrenheit_to_kelvin(212)
    Decimal('373.15')

Executing Tests
===============

Code must be functional and pass tests before it will be eligible for credit.

Linting
-------

Lint tests check your code for syntactic or stylistic errors To execute lint
tests against a specific file, simply open a terminal in the same directory as
your code repository and type:

.. code:: console

    $ pylint filename.py

Where ``filename.py`` is the name of the file you wish to lint test.

Unit Tests
----------

Unit tests check that your code performs the tested objectives. Unit tests
may be executed individually by opening a terminal in the same directory as
your code repository and typing:

.. code:: console

    $ nosetests tests/name_of_test.py

Where ``name_of_test.py`` is the name of the testfile found in the ``tests``
directory of your source code.

Running All Tests
-----------------

All tests may be run simultaneously by executing the ``runtests.sh`` script
from the root of your assignment repository. To execute all tests, open a
terminal in the same directory as your code repository and type:

.. code:: console

    $ bash runtests.sh

Submission
==========

Code should be submitted to `GitHub`_ by means of opening a pull request.

As-of Lesson 02, each student will have a branch named after his or her
`GitHub`_ username. Pull requests should be made against the branch that
matches your `GitHub`_ username. Pull requests made against other branches will
be closed.  This work flow mimics the steps you took to open a pull request
against the ``pull`` branch in Week Two.

For a refresher on how to open a pull request, please see homework instructions
in Lesson 01. It is recommended that you run PyLint locally after each file
is edited in order to reduce the number of errors found in testing.

In order to receive full credit you must complete the assignment as-instructed
and without any violations (reported in the build status). There will be
automated tests for this assignment to provide early feedback on program code.

When you have completed this assignment, please post the link to your
pull request in the body of the assignment on Blackboard in order to receive
credit.

.. _GitHub: https://github.com/
.. _Python String Documentation: https://docs.python.org/2/library/stdtypes.html
