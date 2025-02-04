.. _testing:

Running the Tests
=================

A ``Makefile`` is included to take care of setting up a virtualenv for running tests. All you need to do is run::

    $ make test

To change the Python version used to run the tests (default is Python 2.7), change the ``PYTHON_MAJOR`` and ``PYTHON_MINOR`` variables at the top of the ``Makefile``.

You can run on all supported versions with::

    $ make test-all

Individual tests can be run using a command with the format::

    pytest <filename>:ClassName.func_name

Example::

    $ source env/bin/activate
    $ pytest tests/test_reqparse.py:ReqParseTestCase.test_parse_choices_insensitive
