.. _developer-add-port-example:

Add a new example or port one
=============================

Adding examples is a good exercise for people wanting to become familiar with
the modules and its functionality.

You can either design an example from scratch or inspired in another
application, or simply you can port an existing Qt example that does not have
a Python counterpart.

Add a new example
-----------------

- Check if the topic your example covers is not in an existing example already.
- Create a new directory inside the ``examples/<module>`` you think
  is more relevant.
- Inside, place the code of the example, and also a ``.pyproject``
  file listing the files the example needs.
- If you want the example to be automatically displayed on the
  example gallery, include a ``doc`` directory that contains a ``rst``
  file and a screenshot. Check other examples for formatting questions.

Port a Qt example
-----------------

- Quickly check the C++ example, fix outdated code.
- Port the sources using ``tools/tools/qtcpp2py.py`` (front-end for
  ``snippets-translate``).
- Note that our examples need to have unique names due to the doc build.
- Verify that all slots are decorated using ``@Slot``.
- Add a ``.pyproject`` file (verify later on that docs build).
- Add a ``doc`` directory and descriptive ``.rst`` file,
  and a screenshot if suitable (use ``optipng`` to reduce file size).
- Add the ``"""Port of the ... example from Qt 6"""`` doc string.
- Try to port variable and function names to snake case convention.
- Verify that a flake check is mostly silent.
- Remove C++ documentation from ``sources/pyside6/doc/additionaldocs.lst``.
