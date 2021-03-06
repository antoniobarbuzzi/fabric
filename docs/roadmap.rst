===================
Development roadmap
===================

This document outlines Fabric's intended development path. Please make sure
you're reading `the latest version
<http://docs.fabfile.org/en/latest/roadmap.html>`_ of this document! 

.. warning::
    This information is subject to change without warning, and should not be
    used as a basis for any life- or career-altering decisions!


Near-term feature releases
==========================

* Fabric **1.3**: Parallel task execution, using Morgan Goose's
  `multiprocessing`-based work.
* Fabric **1.4**: Logging integration and other UI tweaks, possibly including
  colored output by default.
* Fabric **1.5**: Network-related improvements, such as an option for skipping
  or retrying unreachable or otherwise "bad" hosts.


Longer-term but probably still 1.x plans
========================================

In no particular order, some potential future feature releases:

* Fork Paramiko and fix `a number of outstanding issues/deficiencies
  <https://github.com/fabric/fabric/issues/275>`_ that cause problems for
  Fabric itself (authentication failure reasons being unclear, lack of SSH
  agent forwarding and/or gateway support, etc.)
* Re-examine `Tav's fork
  <http://tav.espians.com/fabric-python-with-cleaner-api-and-parallel-deployment-support.html>`_
  and see if anything remains which A) has not already been implemented based
  on older work, such as ``@task`` and parallel execution, and B) fits well
  with the current vision for Fabric's feature set and style/behavior.
* Improve core execution mechanisms, mostly by chopping up ``fab``'s action
  loop and exposing chunks of it via the API.
* Improved object-oriented design, both internal refactoring and at the API
  level (for example, ``Host`` objects as an alternative to host strings.)


Fabric 2.0
==========

* As a lead-in, any additional 1.x-compatible internal refactorings or API
  add-ons, such as aforementioned OO design patterns. Get as much done as
  possible without breaking backwards compatibility.
* Make decisions about what old ways of doing things should be axed in 2.0, or
  which can be easily "wrapped" in newer mechanisms without requiring lots of
  legacy code.
* Any other 2.x-marked tickets introducing new, clearly-backwards-incompatible
  features (`see list <https://github.com/fabric/fabric/issues?labels=2.x>`_.)
