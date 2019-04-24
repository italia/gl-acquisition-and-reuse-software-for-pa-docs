Annex B: Open source software maintenance guide
-----------------------------------------------

This guide is aimed at administrations who, as owners of software
already published in open source, intend to carry out maintenance on it.
The guide can be used by anyone responsible for carrying out the
activities described therein: the internal resources of the
administration, the administration's in-house company, a service
provider identified by the administration. The term 'Responsible party'
is equally applied in the description of activities for all three
categories.

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

Obligation to release
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When, as part of maintenance activities, modifications are made to the
original code, even of a minor nature, the obligation to release
pursuant to Article 69 of the Digital Administration Code is imposed.

If the administration already owns a repository for the software being
maintained, created in accordance with the open source *Software
publication guide*, the changes MUST be released by updating the
repository before they are put into testing or production. In order to
manage these release and testing flows, distinguishing the version
already in production from that under development or testing, the
Responsible party MAY use the branching functionalities provided by the
selected version control system.

If, on the other hand, the administration does not already own a
repository for the software being maintained, it must proceed to create
one following the instructions in the *Guide to modifying third-party
open source software*.

2. Obligations relating to the maintenance of software for which the
   administration already has a repository

The following provisions apply where the administration owns a
repository.

Updating dependencies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Throughout the duration of the maintenance role, the Responsible party
MUST monitor the releases of any dependencies incorporated in the
software and implement any updates. If the software is derived from
other software, this obligation to monitor and implement also applies to
the original (so-called upstream) software.

Any incompatibilities or security problems that may arise over time must
be documented, in a timely manner, by opening specific issues, to be
kept open until resolution, and possibly also in the README file. In the
case of new versions that resolve security issues, updating dependencies
must take absolute priority.

Description of the role of maintainer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Within an open source project, the maintainer is the party who carries
out control and development management activities on the project, and to
whom the community connected to the software (e.g. users) can report
problems or discuss improvements.

For the entire duration of the maintenance activity connected to the
software, the owner administration will take on the role of maintainer
of the open source project, entrusting the implementation to the
Responsible party, who will insert the name of their company or body and
contact details in the README and *publiccode.yml* files of the
repository, with any termination date for the role. The Responsible
party will then, on behalf of the administration, manage activities on
the project resulting from interactions with external users.

Interactions on the repository/issue tracker
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

All interactions initiated by external users within the code hosting
platform, and in particular through its issue tracker, SHOULD be
examined by the Responsible party within two working days, and within
this period a response MUST be provided. The answer may not be
exhaustive, and where it is not possible to answer in detail
immediately, it is advisable to provide a courteous response with some
initial considerations.

Bug fixes
++++++++++++++++++++++++

Bug reports received from external users through the issue tracking
system must be analysed in the same way as those received from the
awarding administration. If the fix is compatible (in terms of time and
cost) with the activities provided for in the contract, it may be
executed without further approval. If, on the other hand, the fix is not
compatible (in terms of time and cost) with the maintenance activities
provided for by the contract, the issue must be kept open and the
administration informed of the decision.

The diagnosis and resolution process must be publicly documented within
the issue tracker, with the exception of information that has
implications for the security of the systems in production, which MUST
be kept confidential until the implementation of corrections and only
then MUST it be published for the benefit of other users of the
software. The issue report MUST be kept open until the fix and the
original user SHOULD be asked to personally verify the quality of the
fix before closing it. If there is no response for 30 days, the
Responsible party may close the issue, after having documented the
successful acceptance of the change.

Requests for new functionalities
++++++++++++++++++++++++

Requests for new functionalities must be assessed by the Responsible
party, in agreement with the administration, in relation to their
relevance to the project. If not deemed relevant, they SHOULD be closed
and an explanation provided to the proposer.

If deemed relevant, they MUST be left open until their possible
implementation, but the proposer MUST be provided with rapid feedback
and an assessment of the technical feasibility of the application and
suggestions on any other way to achieve the stated objective. The
Responsible party MAY ask the proposer, if necessary, for more details
on the use case justifying the request.

The implementation of the required functionalities MUST be approved by
the administration in the event that this entails costs for the same
(e.g. in the event that the contract is structured with a consumption
model).

Alternatively, the Responsible party MAY decide to follow up the request
by implementing it in the code, without causing any additional burden to
the administration and within the time-frame of the contract (for
example, pursuant to other commercial agreements on the same software).

Requests for information or support
++++++++++++++++++++++++

Requests for information about the project SHOULD be processed by the
Responsible party within 2 working days. The answers must be limited to
the technical characteristics of the software and to questions posed by
developers or other administrations for the purposes of understanding
technical features, reuse, collaboration or development. The Responsible
party is not required to respond to any other party or to provide
assistance with the use of the software or to provide answers with
regard to the use that the administration makes of the software or in
general with regard to other matters for which the administration is
responsible.

Code contributions
++++++++++++++++++++++++

Code contributions sent through the collaboration mechanisms provided by
the chosen code hosting platform (e.g. through a pull request) MUST be
assessed by the Responsible party who MUST provide feedback to the user
with considerations on the feasibility of integration. The Responsible
party SHOULD incorporate all code contributions that are not
incompatible with the objectives of the provision, providing the
contributor with adequate explanation in the event of refusal.

