---
title: "An Update to YANG Module Names Registration"
abbrev: "YANG Module Names"
category: std
updates: 6020

docname: draft-ietf-netmod-rfc6020-iana-update-latest
submissiontype: IETF
number:
date:
consensus: true
v: 3
area: "Operations and Management"
workgroup: "Network Modeling"
keyword:
 - NETCONF
 - RESTCONF
 - Automation

stand_alone: yes
pi: [toc, sortrefs, symrefs, strict, comments, docmapping]

author:
 -
    fullname: Andy Bierman
    organization: YumaWorks
    country: USA
    email: andy@yumaworks.com

 -
    fullname: Mohamed Boucadair
    organization: Orange
    role: editor
    country: France
    email: mohamed.boucadair@orange.com

 -
    fullname: Qin Wu
    organization: Huawei
    country: China
    email: bill.wu@huawei.com

normative:

informative:

   IANA-MOD-NAMES:
              title: "YANG Module Names"
              author:
                org: IANA
              date: false
              target: https://www.iana.org/assignments/yang-parameters/

--- abstract

   This document amends the IANA guidance on the uniqueness of YANG module and submodule names.

   The document updates RFC 6020 to clarify how modules and their revisions are handled by IANA.

--- middle

#  Introduction

{{!RFC6020}} defines a registry for YANG module and submodule names, called "YANG Module Names" {{IANA-MOD-NAMES}}.

Specifically, IANA considerations to register YANG module and submodule names are specified in {{Section 14 of !RFC6020}}.
These considerations require that all module and submodule names in the registry must be unique. However,
the practice followed by IANA is not consistent with that guidance.

This document amends the guidance on the uniqueness of names ({{Section 14 of !RFC6020}})
to comply with the IANA practices for registering modules and their revisions.

# Requirements Notation

{::boilerplate bcp14-tagged}

#  IANA Considerations {#sec-iana}

## Update YANG Parameters Registry {#sec-update}

This document requests IANA to update the reference for
the "YANG Module Names" registry under the "YANG Parameters" registry group {{IANA-MOD-NAMES}}
to also list to the RFC number that will be assigned to this document. This update is needed
because the procedure in this document is authoritative for assigning names in that registry.

## Revisions of Published Modules {#sec-amend}

This document amends the guidance on the uniqueness of names, initially defined in {{Section 14 of !RFC6020}}, as follows:

{: vspace="0"}
OLD:
: All module and submodule names in the registry MUST be unique.
: All XML namespaces in the registry MUST be unique.

NEW:
: Modules and their revisions are maintained in the registry.
: All initial version module and submodule names in the registry MUST be unique.
: All XML namespaces of initial version modules in the registry MUST be unique.
: All modules and submodules revisions MUST have the same name as the one in the initial version of the module and submodule.
: All module revisions MUST have the same XML namespace as the initial version of the module.

# Operations and Manageability Considerations

This document aligns an IANA policy with the practice for handling YANG module names ({{sec-amend}}). As such, there are no new operations or manageability requirements introduced by this document.

#  Security Considerations

This document defines a new IANA action ({{sec-update}}) and defines an update ({{sec-amend}}) to an IANA registration procedure defined in {{!RFC6020}}.
It does not introduce any new or increased security risks that need to be discussed.

--- back

# Acknowledgments
{:numbered="false"}

The content of this document was part of {{?I-D.ietf-netmod-rfc8407bis}}.

Mahesh Jethanandani suggested to offload this part from {{?I-D.ietf-netmod-rfc8407bis}}.
Thanks to Mahesh for the discussion and comments.
