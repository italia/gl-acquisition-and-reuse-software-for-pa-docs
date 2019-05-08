Annex A: Guide to publishing software as open source
-----------------------------------------------------

This guide is aimed at administrations that, as owners of software, wish
to release it in open source mode (open source code). The guide can be
used by anyone responsible for carrying out the activities described
therein: the internal resources of the administration, the
administration's in-house company, a service provider identified by the
administration. The term 'Responsible party' is equally applied in the
description of activities for all three categories.

The guide has also been produced in order to be annexed to technical
specifications in the context of a contract; in this case the
Responsible party is required to carry out the activities described in
this document as an integral part of the contract, in addition to that
specified in the remainder of the specifications.

The following convention will be adopted in the document:

-  MUST/MUST NOT: mandatory requirements to be met by the Responsible
   party;

-  SHOULD/SHOULD NOT: recommendations to be assessed and implemented by
   the Responsible party if there are no documented reasons for
   obstruction;

-  MAY/MAY NOT: choices that the Responsible party may make at their
   discretion.

Preface
~~~~~~~~~~~~~~~

This document illustrates the technical methods with which software
owned by a public administration is released in open source mode (open
source code). The activities listed below are attributed to the party
made responsible (Responsible party) for the code by the public
administration.

The regulatory context is as follows:

-  Article 69(1) of the Digital Administration Code requires that

‘Public administrations that are owners of solutions and computer
programs made to specific specifications of the public client, have the
obligation to make the relevant source code available, complete with
documentation and released in public repository under an open licence,
for use free of charge for other public administrations or for legal
entities wishing to adapt them to their own requirements, except when
there are ‘justified reasons of public order and safety, national
defence and electoral consultations’.

-  The AgID guidelines (hereinafter referred to as the 'guidelines')
   provide further details on this obligation, detailing the reuse model
   outlined by law and defining the main parameters for the choice of
   licence and the release of the code.

The methods described in this document are inspired by the best
practices adopted in open source development. In addition to the
instructions provided here, please refer to the guide
`https://opensource.guide <https://opensource.guide/>`__ for suggestions
on how to approach the work correctly.

Identifying the code hosting tool
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The owner administration of the software must identify a code hosting
tool to be used for the release. The AgID guidelines specify the minimum
technical parameters, which are listed here for convenience:

-  Free read access to the source code, without authentication;

-  Free and unobstructed registration, open to the public;

-  A web interface for viewing and browsing the code and its
   documentation;

-  The use of a version control system with the functionality of
   managing parallel branches of development;

-  An issue tracker system open to the public for read access without
   authentication and for write access following authentication;

-  Implementation of at least one flow for sending modifications, code
   review and integration of the modification, fully managed by the
   tool, open to the public;

-  A release management system;

-  Availability of an API to interface with the tool and extract data
   and metadata related to the repositories.

The following code hosting tools comply with these requirements and are
recommended because of their reputation and international popularity:

-  GitHub - https://github.com/ (free of charge);

-  BitBucket - https://bitbucket.org/ (free or self-hosted for a fee);

-  GitLab - https://gitlab.com/

-  Phabricator/Phacility - https://www.phacility.com/

-  Gitea - https://gitea.io/

-  Gogs - https://gogs.io/

This list is intended to be illustrative and not exhaustive.

The administration that owns the rights will advise the Responsible
party of a code hosting tool to be used for the release; in the absence
of such advice, the Responsible party may propose a tool of their
preference.

The identified platform MUST be available and maintained independently
of the current process, i.e. it MUST be provided in SaaS mode by third
parties or be established by the awarding administration or by another
administration for more general purposes than the current project.

If the software is a derivative of other existing open source software,
the same platform SHOULD be adopted in order to take advantage of its
collaborative capabilities.

If the administration already has its own area ('organisation’) within
the identified code hosting tool, access will be granted to the
Responsible party’s contact persons. Otherwise, the Responsible party
will open an account with the agreed tool; the name of the area will
reflect the project and not the name of the administration, nor will it
refer to the Responsible party; furthermore, the Responsible party will
provide the administration with access to the tool with the highest
authority. The administration will remain the owner of the area even
after the conclusion of this process.

Within the chosen tool, the Responsible party will open a repository to
host the software in development. If the process is divided into several
logically distinct components with independent purposes, provided that
they are undertaken individually, documented and reused separately,
distinct repositories MUST be opened.

The link to the repository must be recorded in the software interface
available to the public (e.g. with a link in the page footer or within
the help section) so that it is possible for the user to find the
version of the code as it is in execution.

Choosing a licence
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The open licence to be adopted must be identified by the administration
in the specifications or agreed upon in execution, in accordance with
the guidelines. The Responsible party MUST ensure the compatibility of
this licence with those of any reused or incorporated components, with
or without modifications, for which the rights are not owned (e.g.
libraries, graphical assets), including those owned by the Responsible
party themselves. If these components are in separate files, the
separate licence MAY be maintained as long as this is permitted by the
licenses and the relative files clearly indicate the different licence
and the owners of the economic exploitation rights.

Granting of the licence and identification of ownership
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In order to apply the selected licence to the material to be released, a
file called LICENCE must be created in the root of the repository,
containing the full text of the chosen licence, without any
modification. The original texts are available at
https://spdx.org/licenses/. The applied licence MUST be identified
through its SPDX full name (or identifier) at the beginning of each
source file, so that automatic metadating of the used licences is made
easier.

We recommend reading the guide https://reuse.software/practices/2.0/ for
further recommendations on applying the licence to different file
formats.

Pursuant to Article 69(2), of the Digital Administration Code, the
holder of the rights to be specified in the source code MUST be the
awarding administration, which has acquired ownership.

Identification of materials to be released
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following materials are subject to an open source release
obligation:

-  source code;

-  database structure;

-  scripts or other materials required for installation in a development
   or production environment;

-  generic graphical assets (e.g. buttons, graphical elements);

-  documentation for installation of dependencies, compilation (where
   applicable), commissioning.

The following materials are excluded from the release obligation:

-  data used in production or processed with the developed software;

-  specific graphical assets (e.g. company logos) for which the selected
   licence is not applicable.

Release of the code and organisation of the repository
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The source code must be released in full and without omissions, so that
a third party can, by following its documentation, compile (where
applicable) and implement it without the need for modification. The
names of variables, functions, classes and other symbols must be kept
clear and understandable; likewise, the code must not be subjected to
any compression (so-called minification) that impedes its readability.
Any attempt to obfuscate shall be regarded as a breach of the release
obligation.

Maximum attention MUST be paid to the readability of the code, which
MUST be correctly indented and commented on at every step. A coherent
and clean coding style is required. Some examples of conventions:

-  https://github.com/google/styleguide

-  https://www.gnu.org/prep/standards/

-  https://www.kernel.org/doc/Documentation/process/coding-style.rst

-  http://www.php-fig.org/psr/psr-2/

-  http://pear.php.net/manual/en/standards.php

Modular architecture SHOULD be adopted, based on the division of the
logic into specialised and individually reusable libraries, with defined
and documented internal APIs in the code comments. In the event of
integration of external libraries, package managers SHOULD be used, to
facilitate maintenance and updating.

The open source release must not be just considered as an obligation to
be carried out at the end of the process, but SHOULD be provided as
early as the development phase, for example by structuring the software
so that all the specifics of the awarding administration (names,
addresses, servers) are modifiable through configuration files and that
the software is ready for reuse by another party.

The repository MUST be organised with a clear and understandable
directory structure, e.g. by separating documentation, libraries,
executables, service scripts, test suites, etc. into separate
directories.

README file
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The repository must contain a file named README.md containing:

-  (MUST) the title of the repository and a descriptive subtitle;

-  (MUST) extensive description of the repository in a language
   understandable even by non-experts (avoid acronyms and technical
   jargon), in particular:

   -  context of use and use cases;

   -  purpose of the software;

   -  screenshots (if the software has a graphical interface, including
      online);

   -  links to any institutional pages related to the project or context
      of use;

-  (MUST) links to any additional documentation not included in this
   repository;

-  (MUST) repository structure explanation for the benefit of potential
   contributors (directory and branch structure);

-  (MUST) detailed list of prerequisites and dependencies (operating
   systems, libraries, frameworks, etc.) with explicit indication of any
   dependencies on commercial software;

-  (MUST) installation instructions:

   -  procedure for installing requirements and dependencies;

   -  build system (if provided for by the project);

   -  commands for compilation or deployment, possibly automated by a
      script/Makefile (if provided for by the project);

-  (MUST) an indication of the status of the project:

   -  alpha/beta/stable etc.;

   -  important limitations or known issues;

-  (SHOULD) links to any continuous integration systems (TravisCI,
   CircleCI), code coverage and other metrics associated with the
   repository;

-  (SHOULD) documentation on the possible use of systems to simplify and
   accelerate deployment in the development, testing and production
   environment (e.g. Docker images or other virtualisation systems with
   pre-configured image preparation);

-  (MUST) names of copyright holders, i.e. the awarding administration;

-  (MUST) names of the persons in charge of maintaining the open source
   project (the name of the company is required and the names of the
   persons in charge may be added);

-  (MUST) email address to which security reports must be sent (specify
   that security reports must not be sent via the public issue tracker
   but must be sent confidentially to the aforementioned email address);

Documentation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Documentation MUST be attached to the software for the following
purposes:

-  to install dependencies;

-  to install a development environment from scratch (preferably
   accompanied by scripts, container images, Makefiles or other tools to
   make the operation fast);

-  to compile the software (if applicable);

-  to install the software in the production environment;

-  to understand the software architecture (for the benefit of third
   parties who wish to reuse or integrate it).

The attached documentation MUST also follow the instructions on the
release of technical documentation prescribed in the design guidelines
for public administration web services (Content design section) and the
Docs Italia guide, both published by AgID. The documentation must be
written in a textual format that guarantees line by line versioning (for
example, the following formats are allowed): HTML, Markdown,
reStructuredText, LaTeX). Documentation in ODT, DOCX or PDF format is
not allowed as these are formats with which it is not possible to define
different versions ‘line by line’.

If the specifications also provide for the preparation of documentation
on the use of the software for end-users ('user manual' or similar
document), the release obligation also extends thereto. Binary formats
are also allowed for such documentation, provided they are open,
editable and cross-platform (PDF format is therefore excluded).

Release times
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

At the beginning of the process, the Responsible party agrees with the
administration on the plan for the open source release of the software
during development. The guidelines suggest that an open development
model should be adopted, which provides for release from the outset, at
the same time as the development. This model also allows other
administrations to become aware of development activities, even before
they are initially put into production, reducing the likelihood of two
administrations developing similar software independently.

If an open source development model is not chosen, the open source
release MUST be carried out within 15 days from the time of the
acquisition of the software by the awarding administration at the end of
the process, or from the time at which the software goes into testing or
production, or by a request from the administration that may in any case
be forwarded to the Responsible party at any stage. If the process is
carried out in several batches, these release deadlines apply to each
batch.

From the moment of release, any subsequent changes MUST be published in
the repository in a timely manner, regardless of whether they are being
tested or produced. In order to manage such release and testing flows,
the Responsible party MAY use the branching functionalities offered by
the selected version control system.

Security
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Bearing in mind that software security is an important issue to consider
during the development cycle and that it will not be covered in this
document, here are some basic principles on specific precautions to be
adopted during the release process.

Passwords or certificates or other credentials related to real systems
(including test systems) MUST be removed from the source code, using
separate configuration files or blacklists in the version control system
(e.g. a .gitignore or .hgignore file). If you wish to integrate the
repository with an automatic deployment mechanism and therefore need to
maintain the credentials, the secure encryption mechanisms provided for
the code hosting platform and for the continuous integration systems
adopted (e.g. git-crypt) may be used.

It is important to ensure that such credentials (**API keys, secrets,
passwords, . . .** ) have not been mistakenly stored within the
repository, not only in the current version but also in previous
revisions.

Rewriting of algorithms already available in external open source
libraries (e.g. encryption, input sanitisation, network protocols, XML
parsing or other formats, memory management, etc.) MAY be avoided if
possible.

All 'dead’ (i.e. not used) code, MUST be removed because it could lead
to confusion or be taken as maintained and incorrectly reintegrated
without the necessary controls.

If the software is a web application exposed on a public network, or
contains web applications, a file formatted according to the
instructions found at
`https://securitytxt.org <https://securitytxt.org/>`__ SHOULD be
accessible for each installation at the following pathway -
``https://<hostname>/.well-known/security.txt``. This file is aimed at
providing useful information to those who detect vulnerabilities and
intend to send security reports.

Registration of the repository on Developers Italia
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

As soon as the public repository has been opened, registration on
Developers Italia MUST be carried out, to ensure that the repository is
indexed and available in the search engine on the site.

Registration is a two-step process:

1. **Publication of a publiccode.yml file in the root directory of the
   repository.** A ‘publiccode.yml' file is a standard that identifies
   the project as 'useful software for the public administration', and
   at the same time provides a range of useful information for the
   assessment of the software for reuse. This file will be automatically
   detected by the Developers Italia crawler in order to generate the
   relative data sheet in the catalogue. Documentation on the format can
   be found here: https://github.com/italia/publiccode.yml

2. **Adding the code hosting tool to the search engine.** In order to
   ensure that Developers Italia correctly identify the repository as
   belonging to the public administration, the code hosting tool (or
   rather, the 'organisation' within the same) must be registered the
   first time it is used, associating it with the public administration.
   The procedure to be followed is detailed here:
   `https://onboarding.developers.italia.it <https://onboarding.developers.italia.it/>`__

