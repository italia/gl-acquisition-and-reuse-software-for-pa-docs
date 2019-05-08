Annex C: Open source licence guide
------------------------------------

Open source licences may be multiple, with slight differences that may
present important incompatibilities at the time of reuse of the
software. This guide aims to provide the reader with a brief
introduction to the different licences that can be adopted, and make
suggestions regarding the adoption of a number of specific licences.
Limiting the number of licences in the software range has the advantage
of greatly simplifying integration, thus allowing for savings by the
public administration.

Versioning of licences
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Each licence listed below has a version number, which provide issuing
bodies with the ability to update them. In order to ensure compatibility
and reusability of the code in the future, in particular for copyleft
licences, it is recommended that software is released according to the
latest available version of the licence, clarifying compatibility with
any subsequent changes.

Public domain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A public domain licence is a licence in which the holder of the rights
renounces the intellectual property rights.

This is the recommended licence for the release of open data databases,
where you do not deal with original databases of choice or availability
of works. Please note that the rights to the individual elements
contained in a database are still covered by their individual licence,
which is not affected by their inclusion in a database.

This licence provides reusers with total flexibility and reduces
complications associated with operating under various and different
licences with the potential conflicting provisions that this entails.

The most popular licence in this area is the Creative Commons Zero (SPDX
Code: ``CC0-1.0``).

Non-copyleft licences
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Non-copyleft licences are open licences that provide considerable
freedom and flexibility for users to reuse.

In fact, with these licences, the rights holder only requires a phrase
identifying the source of the document and, where feasible, a link to
the relevant licence information, and does not restrict the use or
modification of the original work.

These licences are used for software components that implement adapters
or components that are created to be integrated into third-party
applications. The main focus of these licences is on reuse in as many
programs as possible.

Unlike copyleft licences, there is no obligation for those who adapt
these components to release any changes and improvements, but only a
reference to obtain a copy of the original source code.

Examples of these licences are the BSD licence, the MIT licence and the
Apache licence - SPDX identifiers:

``BSD-3-Clause``, ``MIT`` and ``Apache-2.0``.

**Note:** use of the Apache licence is not recommended as it is
incompatible with the GNU GPL version 2 (SPDX identifier:
``GPL-2.0-or-later``).

Copyleft licences
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Copyleft licences are licences that require attribution to the original
author but that add so-called 'viral' clauses. The concept of virality
requires any subsequent modification to be released under a licence that
does not impose additional restrictions on the user.

They are used to preserve the freedom of the software at each subsequent
modification, requiring the release for reuse of any updates by third
parties.

It is essential to provide a copy of the source code only during the
distribution or licensing of the software, not at the time of
development.

This type of licence is recommended for all complete software
applications.

The most widely used licence in this area is the GNU GPL (SPDX
identifier: ``GPL-3.0-or-later``) or the GNU AGPL, its modification that
also covers the scope of software distributed online (SPDX identifier:
``AGPL-3.0-or-later``).

Copyleft licences - for libraries
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In order to ensure flexibility in reuse, i.e. to allow for the use of a
software component in an application under any licence, the virality
clause may be weakened. These licences are also called 'weak copyleft'
licences.

This additional clause keeps virality intact with respect to changes to
the component code, but allows for external integration by software
distributed under any licence.

Please note that these licences contain the so-called 'reproducibility
clause': it must always be possible for the user of third-party software
to replace the component released under the LGPL licence with a modified
version, without changing the functionalities of the third-party
software. This clause can be problematic and unsatisfactory in some
embedded environments, such as iOS.

The most used version is the GNU LGPL (SPDX identifier:
``LGPL-3.0-or-later``), modified version of the GNU GPL licence.

Licences not included in the newly introduced classification
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   -  The Mozilla Public Licence (SPDX identifier: ``MPL-2.0``) is a
      copyleft licence, comparable to the GNU GPL licence, which
      guarantees free distribution of the code but dictates that it may
      not be reused, if required, for modifications, logos, names or
      other registered trademarks of the rights holder, without further
      authorisation.

   -  The European Union Public Licence (EUPL) is a weak copyleft
      licence, developed by the European Commission, and officially
      translated into all EU languages. This licence includes a
      compatibility table with some of the most common open licences.
      SPDX identifier: ``EUPL-1.2``.

Creative Commons licences
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There are many versions of Creative Commons licences. These licences, as
suggested by Creative Commons itself, cannot be used to protect
software, but only other original works (e.g. documentation or text).

The only Creative Commons licences that can be considered as open
licences, as described in 3.3, are:

-  Creative Commons Zero - public domain (SPDX identifier: ``CC0-1.0``).

-  Creative Commons Attribution (version 4 or above) - a non-copyleft
   licence (SPDX identifier: ``CC-BY-4.0``)

-  Creative Commons Attribution-Share Alike (version 4 or above) - a
   copyleft licence (SPDX identifier: ``CC-BY-SA-4.0)

Licence applicable to software documentation and attachments
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

All attachments to the raw source code of the software, such as comments
in the source code, documentation, examples, demo screens, videos, etc.
are considered to be included under the same licence as the software
itself. Therefore, in general, it is not necessary to determine
different licences for such content, if they are released at the same
time as the software and as an integral part of it.

In the event of the release of separate documentation with respect to
the software, or in the case of the latter being particularly
substantial (more than 10 printed pages), it is recommended to grant a
licence to the work in any case. Please refer to 4.4 for guidance on
selecting the best licence.

Compatibility between licences
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Compatibility of licences depends on the transfer of intellectual
property rights by the author. In order to preserve the freedom and
reusability of software created over time, copyleft licences are the
licences that yield fewer rights in this context.

As regards compatibility, two scenarios must be differentiated:

-  The creation of a new work from existing components, with a single
   licence

-  The assembly and distribution of multiple interacting components,
   each with a different licence.

As regards the case of creating a new work under a single licence, the
compatibility matrix can be explained as follows:

-  Works released under a public domain can be released under any other
   licence

-  Works released under non-copyleft licences are releasable with
   copyleft licences

-  Works released under copyleft licences may only be released with
   copyleft licences, provided that the two licences are compatible

On the other hand:

-  Works licensed under a public domain, non-copyleft or weak copyleft
   may interact as stand-alone components with any other application,
   while respecting any provisions regarding references to the original
   code and the distribution of any modifications.

-  Works released under a copyleft licence may only interact as
   stand-alone components with other components released under a
   compatible copyleft licence.

