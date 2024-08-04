=====================
Versions and Releases
=====================

The ``asyncstdlib`` versioning closely follows
versioning of the Python standard library.
New versions are published via `PyPI`_ and `Conda-Forge`_
for installation via ``pip`` and ``conda``.

Versioning and feature coverage
===============================

The ``asyncstdlib`` mimics the versioning of the Python standard library:

* *Major and Minor version* indicate which Python feature set is supported, and
* *Patch version* indicates the iteration of this feature set.

For example, ``asyncstdlib`` version 3.9.2 provides the feature set of Python 3.9,
such as :py:func:`~asyncstdlib.functools.cache` added in 3.9
and :py:func:`~asyncstdlib.functools.cached_property` added previously.

The ``asyncstdlib.asynctools`` feature set does not follow a strict version model.
New features may be added at minor or patch releases.

Release workflow
================

.. note::

    This section is only relevant for maintainers of ``asyncstdlib``.

Releases are performed manually but should happen at least when
an important fix or major feature is added.
Most releases will bump the *patch* version number;
only bump the *minor* or *major* version number to match a new Python release.

1. Review all changes added by the new releases:
    * Naming of functions/classes/parameters
    * Docs are up to date and consistent
    * Unittests cover all obvious cases

2. Bump the version number:
    * Adjust and commit ``asyncstdlib.__init__.__version__``
    * Create a git tag such as ``git tag -a "v3.9.2" -m "description"``
    * Push the commit and tags to github

3. Publish the new release:
    * Create a new `GitHub release`_ from the recent version tag
    * PyPI will be automatically published to via GitHub actions
    * Handle the automatic PR at the `Conda-Forge asyncstdlib recipe`_

.. _PyPI: https://pypi.org
.. _Conda-Forge: https://conda-forge.org
.. _`PyPI asyncstdlib project`: https://pypi.org/project/asyncstdlib/
.. _`GitHub release`: https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases
.. _`Conda-Forge asyncstdlib recipe`: https://github.com/conda-forge/asyncstdlib-feedstock
.. _`PyPI release`: https://pypi.org/project/asyncstdlib/#files
