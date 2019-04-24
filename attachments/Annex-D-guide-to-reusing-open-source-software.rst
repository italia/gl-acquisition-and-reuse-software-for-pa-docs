Annex D: Guide to reusing open source software
--------------------------------------------------

This guide is aimed at administrations that wish to reuse software or
adopt third-party open source software and make modifications to it. The
guide can be used by anyone charged with carrying out the activities
described therein: the internal resources of the administration, the
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

Modifying open source software adopted for reuse
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In the event of reuse of open source software, owned by a public
administration, the provisions of `Annex A: Guide to publishing software
as open source <#_bookmark65>`__, together with the instructions
contained in this guide apply.

Furthermore, the procedures described in this guide may also be applied
to modifications made to software components distributed under an open
source licence which are not owned by the public administration and
which must be integrated into software owned by the public
administration.

In the event of adoption of software released by a public
administration, the decision to adopt for reuse must be notified by
opening a ticket (or similar mechanism such as a pull request) in the
repository of the owner public administration, so that it can specify
references to reuse within the publiccode.yml file, in the appropriate
section.

Modification of the source code
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Responsible party MUST operate carefully in order to minimise the
degree of divergence between the original source code and the modified
code resulting from the work carried out. When making the necessary
changes to the adaptation, not only must the required functionalities be
taken into account, but the code base must also be kept compact and
uniform.

The modification of source code MUST be kept to the minimum required,
with the following interventions taking priority:

-  where the original software provides a plugin mechanism, the new
   functionalities MUST be developed through the plugin without
   modifying the core (for example, in the case of a content management
   system);

-  where it is possible to extend existing classes or modules in general
   without modifying their code (i.e. for

an *addition*, by exploiting existing extension points), this path MUST
be followed.

If it is not possible to perform all the functions through the
aforementioned extension mechanisms, but the original source code
requires modification, the modifications must be inspired by minimalism,
i.e. in order of preference:

-  only essential functions should be implemented in order to operate in
   one of the extension modes described above;

-  the new functionalities must be implemented not with a view to
   specialising the original software in its own context, but rather as
   an intervention for strengthening and generalising the original
   software.

Modifications that limit the functionalities or use of the original
software MUST NOT be allowed; each intervention should be an improvement
and SHOULD be designed in such a way that it can be accepted as a
contribution by the maintainers of the original software.

In any case, the README file must clearly explain what has been changed
since the original project.

The published repository SHOULD contain the entire history of the ‘code
commit’ changes that the Responsible party has carried out during the
development process, preserving the history of the development activity,
creating a useful tool for all developers who wish to contribute to
reducing the learning curve.

Interaction with the original project maintainer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Responsible party SHOULD maximise interaction with the original
project maintainer with a collaborative approach and with the objective
of consolidating the work into a single code base for the benefit of
subsequent reuse.

In the case of bug fixes, the Responsible party MUST send the fix
proposal to the original maintainer using the collaboration tools
provided by the code hosting platform (e.g. pull request).

In the case of changes required to implement the new functionalities,
the Responsible party MUST contact the maintainer through the public
channels of the repository (issue tracker) in order to present the new
use case, propose the change and receive feedback on how to follow-up,
especially with a view to making changes that may be incorporated from
the original maintainer. The maintainer should be given a few days to
respond; however, if the response time is too long, the Responsible
party MAY also proceed independently.

At the end of development, the Responsible party MUST propose their own
changes to the original maintainer, with granular pull request code
proposals, i.e. separate proposals for individual functionalities, so as
to allow the maintainer to assess them individually.

The Responsible party MUST also keep track of all contributions to the
software sent to the maintainer of the original software, documenting
the integration status within the README file of the repository.

Publication of open source code not originating in the context of the PA
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In the event that the maintainer of open source software whose ownership
is not attributed to a public administration has fully implemented the
modification proposals (see previous paragraph) presented by the
Responsible party, the latter is still required to publish the code in
the code hosting tool of the administration to allow it to be reused,
specifying in the README file that this code has been transposed from
the original project, with a link to the repository of the same.

As prescribed by the guidelines, 'reusable software' is software
released by a public administration in compliance with Article 69 of the
CAD. Therefore, a public administration that adopts open source software
not originating in the context of the PA, is required to make it
available for reuse, indicating its origin.
