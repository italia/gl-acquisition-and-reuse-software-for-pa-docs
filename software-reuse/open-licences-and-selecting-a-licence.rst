Open licences and selecting a licence
---------------------------------------

To release the software source code under an open licence, the
administration must choose appropriate licence text.

Context
~~~~~~~~~~~~~~~~~~~~
It should be noted that the legislator, in drawing up Article 69, has
clearly indicated that the objective is to **encourage the reuse** of
the same software between several administrations. It is therefore
important that the first consideration as regards the importance of the
choice of the licence is to **assess the impact that the licence text
has on the possibility of reuse** by other administrations.

Since the 1980s, the world of computer research and industry has
produced numerous examples of licence texts for open source software,
with the aim of creating a global software sharing model. As the
complexity of applications increases, it has become increasingly
important to work with ready-made components rather than to start
developing code from scratch each time.

Open software licences
~~~~~~~~~~~~~~~~~~~~

An open licence, as understood in Article 69 of the CAD, is a licence
that grants the user of software the following freedoms:

-  Freedom to use the software as desired, for any purpose, without
   additional costs or restrictions;

-  Freedom to analyse how the software works and to modify it in order
   to adapt it to your needs;

-  Freedom to redistribute copies of the software;

-  Freedom to modify the software and publicly distribute the modified
   versions. [5]_

Access to the source code, or equally to the format necessary to
reproduce and modify the software, is a prerequisite for respecting
these freedoms.

Open Source Initiative [6]_ (OSI) is an international organisation,
recognised worldwide for the certification process of software licences
that meet these requirements. An updated list of OSI-certified licences
is available at the following address (in alphabetical order):
https://opensource.org/licenses/alphabetical

Compliance with Article 69 of the CAD, with regard to selecting the
licence, must be carried out **by choosing a licence from those
certified by the Open Source Initiative**. Alternatively, the
administration that wishes to independently provide for the drafting of
text for a licence, may only use this text following certification by
the Open Source Initiative, to verify its adherence with the principles
of open software. The process of sending a licence for approval is
detailed at this link: https://opensource.org/approval.

It should be noted that to uniquely identify licence text, SPDX
categorisation [7]_ may be used, which associates each licence (or
combination) with a unique identifier and full name. An updated list of
identifiers and their licence texts is available at this link:
https://spdx.org/licenses/.

Attached to the guidelines (`Annex C: Guide to open source
licences <#_bookmark83>`__) there is a guide that delves further into
the topic of open source licences, which outlines the categorisation of
the main types of licences and their features.

Choosing a licence
~~~~~~~~~~~~~~~~~~~~

A free software licence allows for the free use of the source code to
which it refers, while imposing certain constraints that must be
respected. As such, the integration of multiple free software components
released under different licences requires a compatibility analysis of
the same. Such an analysis may be overly complex if there are multiple
licences involved, leading to additional costs.

In other words, **a proliferation of different licences makes it more
difficult and costly to reuse software**, contrary to the objectives
outlined in Article 69 of the CAD.

Use of the following decision-making process is recommended for
selecting an open licence:

-  If the software release refers to modifying existing open source
   software (i.e. software picked-up for reuse by another administration
   or owned by third parties), the administration will use the **same
   licence** with which the software was originally distributed, to
   facilitate maximum interoperability and reuse with other users of the
   same software;

-  If it is **new software**, apart from the exceptions specified below,
   use the EUPL v1.2 licence (SPDX identifier: EUPL-1.2):
   https://spdx.org/licenses/EUPL-1.2.html. This licence, developed by
   the European Commission, has been selected as a 'copyleft' licence,
   guaranteeing maximum interoperability at European level, and has also
   been translated into Italian. There are only a few exceptions to this
   general specification:

   -  if **the software is mainly used online (e.g. via a browser)**,
      use the 'GNU Affero General Public Licence' version 3 or above
      (SPDX identifier: AGPL-3.0-or-later):
      https://spdx.org/licenses/AGPL-3.0-or-later.html;

This licence was chosen because, in addition to being compatible with
most open source licences, it requires those who modify the code to
release improvements even if it is used as part of a SaaS service.

-  if **software components** with a wide range of applications (e.g.
   '**software libraries**' and '**SDKs**') are being released, use the
   'BSD 3-Clause' licence (SPDX identifier: BSD-3-Clause)
   https://spdx.org/licenses/BSD-3-Clause.html;

This licence has been chosen to ensure that all stakeholders use it as
freely as possible, allowing applications to be created based on such
libraries, which can be released under any licence. These types of
software components are normally used to facilitate interoperability
with public administrations, and benefit from the emergence of
ecosystems that include third-party applications, including proprietary
software.

-  For software **technical documentation**, use the Creative Commons
   licence CC-BY 4.0 (SPDX identifier: CC-BY-4.0)
   https://spdx.org/licenses/CC-BY-4.0.html. This licence was selected
   because it allows for easy reuse of documentation and code examples
   contained therein.

Please refer to `Annex A: Guide to publishing software as open
source <#_bookmark65>`__ for technical details on how to correctly embed
the licence text to the source code at the time of publication.

Selected licences have a wide use in the open source ecosystem,
therefore the ability to integrate third-party components released with
compatible licences is maximised.

An administration that wishes to select a licence differently from that
outlined here must justify their reasons, analysing the compatibility
between the licenses adopted and those proposed here, ensuring that the
choice does not limit opportunities for reuse and that it does not
entail additional costs for administrations in the reuse phase.
