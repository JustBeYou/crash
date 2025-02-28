.. _compatibility:

=============
Compatibility
=============

.. rubric:: Table of contents

.. contents::
   :local:

.. _versions:

Version notes
=============

.. _python-versions:

Python
------

You must be running the following versions of Python:

+----------------+-----------------+
| Client Version | Python Version  |
+================+=================+
| >= 0.23        | >=3.4           |
+----------------+-----------------+
| 0.23.x         | 3.3             |
+----------------+-----------------+
| 0.23.x         | 2.7             |
+----------------+-----------------+
| 0.16.x         | 2.6             |
+----------------+-----------------+

.. NOTE::

    If you are using `pip`_, the highest compatible version of the client will
    be installed according to the version of Python you are using.

.. _cratedb-versions:

CrateDB
-------

Consult the following table for CrateDB compatibility notes:

+----------------+-----------------+-------------------------------------------+
| Client Version | CrateDB Version | Notes                                     |
+================+=================+===========================================+
| <= 0.19        | >= 0.57         | Not supported.                            |
+----------------+-----------------+-------------------------------------------+
| Any            | <= 0.38.x       | It is not possible to insert nested       |
|                |                 | arrays or nested objects via Crash. You   |
|                |                 | must use `CrateDB REST endpoint`_ or a    |
|                |                 | `client library`_.                        |
|                |                 |                                           |
|                |                 | CrateDB versions 0.39 and later allow you |
|                |                 | to insert nested arrays using `array      |
|                |                 | constructors`_, and nested objects using  |
|                |                 | `object literals`_.                       |
+----------------+-----------------+-------------------------------------------+
| Any            | >= 2.1.x        | Client needs to connect with a valid      |
|                |                 | database user to access CrateDB.          |
|                |                 |                                           |
|                |                 | The default CrateDB user is ``crate`` and |
|                |                 | has no password is set.                   |
+----------------+-----------------+-------------------------------------------+

.. _array constructors: https://crate.io/docs/crate/reference/en/latest/general/ddl/data-types.html#data-types-array-literals
.. _client library: https://crate.io/docs/crate/clients-tools/en/latest/
.. _CrateDB REST endpoint: https://crate.io/docs/crate/reference/en/latest/interfaces/http.html
.. _create your own users: https://crate.io/docs/crate/reference/en/latest/admin/user-management.html
.. _object literals: https://crate.io/docs/crate/reference/en/latest/general/ddl/data-types.html#data-types-object-literals
.. _pip: https://pypi.org/project/pip/
