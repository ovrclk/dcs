---
aip: 1
title: AIP Purpose and Guidelines
status: Active
type: Meta
author: Greg Osuri <greg@akash.network>, Adam Bozanich <adam@akash.network>
        https://github.com/ovrclk/AIPs/blob/master/AIPS/aip-1.md
created: 2020-03-09
updated: 2020-03-09
---

## What is an AIP?

AIP stands for Akash Improvement Proposal. An AIP is a design document providing information to the Akash community, or describing a new feature for Akash or its processes or environment. The AIP should provide a concise technical specification of the function and a rationale for the feature. The AIP author is responsible for building consensus within the community and documenting dissenting opinions.

## AIP Rationale

We intend AIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into Akash. Because the AIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For Akash implementers, AIPs are a convenient way to track the progress of their implementation. Ideally, each implementation maintainer would list the AIPs that they have implemented, which end users a convenient way to know the current status of a given implementation or library.

## AIP Types

There are three types of AIP:

- A **Standard Track AIP** describes any change that affects most or all Akash implementations, such as a change to the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using Akash. Furthermore, Standard AIPs can be broken down into the following categories. Standards Track AIPs consist of three parts, a design document, implementation, and finally if warranted an update to the formal specification.
  - **Core** - improvements requiring a consensus fork, as well as changes that are not necessarily consensus critical but may be relevant to "core dev" discussions.
  - **Economics** - includes improvements Akash Economic Model with regards to Staking or Subsidy distribution.
  - **Interface** - includes improvements around client API specifications and standards, and also certain language-level standards like method names. 
- A **Meta AIP** describes a process surrounding Akash or proposes a change to (or an event in) a process. Process AIPs are like Standards Track AIPs but apply to areas other than the Akash protocol itself. They may propose an implementation, but not to Akash's codebase; they often require community consensus; unlike Informational AIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in Akash development. Any meta-AIP is also considered a Process AIP.
- An **Informational AIP** describes an Akash design issue, or provides general guidelines or information to the AIPs community, but does not propose a new feature. Informational AIPs do not necessarily represent AIPs community consensus or a recommendation, so users and implementers are free to ignore Informational AIPs or follow their advice.

It is highly recommended that a single AIP contain a single key proposal or new idea. The more focused the AIP, the more successful it tends to be. A change to one client doesn't require an AIP; a change that affects multiple clients, or defines a standard for various apps to use, does.

An AIP must meet specific minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be robust and must not complicate the protocol unduly.

## AIP Work Flow

### Shepherding an AIP

Parties involved in the process are you, the champion, or *AIP author*, the [*AIP editors*](#aip-editors), and the *Akash Core Developers*.

Before you begin writing a formal AIP, you should vet your idea. Ask the Akash community first if an idea is original to avoid wasting time on something that will be rejected based on prior research. It is thus recommended to open a discussion in the [Akash Technical Chat].

In addition to making sure your idea is original, it will be your role as the author to make your concept clear to reviewers and interested parties, as well as inviting editors, developers, and community to give feedback on the channels above. You should try and gauge whether the interest in your AIP is commensurate with both the work involved in implementing it and how many parties will have to conform to it. Negative community feedback will be taken into consideration and may prevent your AIP from moving past the Draft stage.

### Core AIPs

For Core AIPs, given that they require client implementations to be considered **Final** (see "AIPs Process" below), you will need to either provide an implementation for clients or convince clients to implement your AIP.

The best way to get client implementers to review your AIP is to present it to the team online at [Akash Technical Chat]. You can request to do so by posting a comment linking your AIP. First, to discuss the technical merits of AIPs. Second, to gauge what other clients will be implementing. Third, to coordinate AIP implementation for network upgrades.

These calls generally result in a "rough consensus" around what AIPs should be implemented. This "rough consensus" rests on the assumptions that AIPs are not contentious enough to cause a network split and that they are technically sound.

### AIP Process

Following is the process that a successful non-Core AIP will move along:

```
[ WIP ] -> [ DRAFT ] -> [ LAST CALL ] -> [ FINAL ]
```

Following is the process that a successful Core AIP will move along:

```
[ IDEA ] -> [ DRAFT ] -> [ LAST CALL ] -> [ ACCEPTED ] -> [ FINAL ]
```

Each status change is requested by the AIP author and reviewed by the AIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your AIP. The AIP editors will process these requests as per the conditions below.

* **Idea** -- Once the champion has asked the Akash community whether an idea has any chance of support, they will write a draft AIP as a [pull request]. Consider including an implementation if this will aid people in studying the AIP.
  * :arrow_right: Draft -- If agreeable, AIP editor will assign the AIP a number (generally the issue or PR number related to the AIP) and merge your pull request. The AIP editor will not unreasonably deny an AIP.
  * :x: Draft -- Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backward compatibility, or not in keeping with the Akash philosophy.
* **Draft** -- Once the first Draft has been merged, you may submit follow-up pull requests with further changes to your Draft until you believe the AIP to be mature and ready to proceed to the next status. An AIP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core AIPs).
  * :arrow_right: Last Call -- If agreeable, the AIP editor will assign Last Call status and set a review end date (`review-period-end`), normally 14 days later.
  * :x: Last Call -- A request for Last Call status will be denied if material changes are still expected to be made to the Draft. We hope that AIPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed.
* **Last Call** -- This AIP will be listed prominently on the https://aips.akash.network/ website (subscribe via RSS at [last-call.xml](/last-call.xml)).
  * :x: -- The Last Call, which results in material changes or substantial unaddressed technical complaints, will cause the AIP to revert to Draft.
  * :arrow_right: Accepted (Core AIPs only) -- A successful Last Call without material changes or unaddressed technical complaints will become Accepted.
  * :arrow_right: Final (Non-Core AIPs) -- A successful Last Call without material changes or unaddressed technical complaints will become Final.
* **Accepted (Core AIPs only)** -- This status signals that material changes are unlikely, and Akash client developers should consider this AIP for inclusion. Their process for deciding whether to encode it into their clients as part of a hard fork is not part of the AIP process.
  * :arrow_right: Draft -- The Core Devs can decide to move this AIP back to the Draft status at their discretion. E.g., a major, but correctable, a flaw was found in the AIP.
  * :arrow_right: Rejected -- The Core Devs can decide to mark this AIP as Rejected at their discretion. E.g., a major, but uncorrectable, a flaw was found in the AIP.
  * :arrow_right: Final -- Standards Track Core AIPs must be implemented in at least three viable Akash clients before it can be considered Final. When the implementation is complete and adopted by the community, the status will be changed to “Final.”
* **Final** -- This AIP represents the current state-of-the-art. A Final AIP should only be updated to correct errata.

Other exceptional statuses include:

* **Active** -- Some Informational and Process AIPs may also have a status of “Active” if they are never meant to be completed. E.g., AIP 1 (this AIP).
* **Abandoned** -- the original authors no longer pursue this AIP, or it may not be a (technically) preferred option anymore.
  * :arrow_right: Draft -- Authors or new champions wishing to pursue this AIP can ask for changing it to Draft status.
* **Rejected** -- An AIP that is fundamentally broken or a Core AIP that was rejected by the Core Devs and will not be implemented. An AIP cannot move on from this state.
* **Superseded** -- An AIP which was previously Final but is no longer considered state-of-the-art. Another AIP will be in Final status and reference the Superseded AIP. An AIP cannot move on from this state.


## What belongs in a successful AIP?

Each AIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the AIP, including the AIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See [below](https://github.com/ovrclk/AIPs/blob/master/AIPS/aip-1.md#aip-header-preamble) for details.
- Abstract - A short (~200 word) description of the technical issue being addressed.
- Motivation (*optional*) - The motivation is critical for AIPs that want to change the Akash protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the AIP solves. AIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations Akash platform.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g., how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during the discussion.
- Backward Compatibility - All AIPs that introduce backward incompatibilities must include a section describing these incompatibilities and their severity. The AIP must explain how the author proposes to deal with these incompatibilities. AIP submissions without a sufficient backward compatibility treatise may be rejected outright.
- Test Cases - Test cases for implementation are mandatory for AIPs that are affecting consensus changes. Other AIPs can choose to include links to test cases if applicable.
- Implementations - The implementations must be completed before any AIP is given the status "Final," but it need not be completed before the AIP is merged as a draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of "rough consensus and running code" is still useful when it comes to resolving many discussions of API details.
- Security Considerations - All AIPs must contain a section that discusses the security implications/considerations relevant to the proposed change. Include information that might be important for security discussions, surface risks, and can be used throughout the life cycle of the proposal. E.g., include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks, and how they are being addressed. AIP submissions missing the "Security Considerations" section will be rejected. An AIP cannot proceed to status "Final" without a Security Considerations discussion deemed sufficient by the reviewers.
- Copyright Waiver - All AIPs must be in the public domain. See the bottom of this AIP for an example copyright waiver.

## AIP Formats and Templates

AIPs should be written in [markdown] format. Image files should be included in a subdirectory of the `assets` folder for that AIP as follows: `assets/aip-N` (where **N** is to be replaced with the AIP number). When linking to an image in the AIP, use relative links such as `../assets/aip-1/image.png`.

## AIP Header Preamble

Each AIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order. Headers marked with "\*" are optional and are described below. All other headers are required.

` aip:` *AIP number* (this is determined by the AIP editor)

` title:` *AIP title*

` author:` *a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.*

` * discussions-to:` *a url pointing to the official discussion thread*

` status:` *Draft | Last Call | Accepted | Final | Active | Abandoned | Rejected | Superseded*

`* review-period-end:` *date review period ends*

` type:` *Standards Track | Informational | Meta*

` * category:` *Core | Interface | Economics* (Standards Track AIPs only)

` created:` *date created on*

` * updated:` *comma separated list of dates*

` * requires:` *AIP number(s)*

` * replaces:` *AIP number(s)*

` * superseded-by:` *AIP number(s)*

` * resolution:` *a url pointing to the resolution of this AIP*

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses or usernames of the authors/owners of the AIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

#### `resolution` header

The `resolution` header is required for Standards Track AIPs only. It contains a URL that should point to an email message or other web resource where the pronouncement about the AIP is made.

#### `discussions-to` header

While an AIP is a draft, a `discussions-to` header will indicate the mailing list or URL where the AIP is being discussed. 

No `discussions-to` header is necessary if the AIP is being discussed privately with the author.

As a single exception, `discussions-to` cannot point to GitHub pull requests.

#### `type` header

The `type` header specifies the type of AIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, interface, or economics).

#### `category` header

The `category` header specifies the AIP's category. This is required for standards-track AIPs only.

#### `created` header

The `created` header records the date that the AIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `updated` header

The `updated` header records the date(s) when the AIP was updated with "substantial" changes. This header is only valid for AIPs of Draft and Active status.

#### `requires` header

AIPs may have a `requires` header, indicating the AIP numbers that this AIP depends on.

#### `superseded-by` and `replaces` headers

AIPs may also have a `superseded-by` header indicating that an AIP has been rendered obsolete by a later document; the value is the number of the AIP that replaces the current document. The newer AIP must have a `replaces` header containing the number of the AIP that it rendered obsolete.

## Auxiliary Files

AIPs may include auxiliary files such as diagrams. Such files must be named AIP-XXXX-Y.ext, where “XXXX” is the AIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## Transferring AIP Ownership

It occasionally becomes necessary to transfer ownership of AIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred AIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the AIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the AIP. We try to build consensus around an AIP, but if that's not possible, you can always submit a competing AIP.

If you are interested in assuming ownership of an AIP, send a message asking to take over, addressed to both the original author and the AIP editor. If the original author doesn't respond to email in a timely manner, the AIP editor will make a unilateral decision (it's not like such decisions can't be reversed).

## AIP Editors

The current AIP editors are

` * Greg Osuri (@gosuri)`

` * Adam Bozanich (@boz)`

` * Jack Zampolin (@jack_zampolin)`

` * Sunny Aggarwal (@sunnya97)`

## AIP Editor Responsibilities

For each new AIP that comes in, an editor does the following:

- Read the AIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the AIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

If the AIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the AIP is ready for the repository, the AIP editor will:

- Assign an AIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this AIP)

- Merge the corresponding pull request

- Send a message back to the AIP author with the next step.

Many AIPs are written and maintained by developers with write access to the Akash codebase. The AIP editors monitor AIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on AIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [Ethereum's EIP-1] written by Martin Becze, Hudson Jameson, and others, which in turn was derived from [Bitcoin's BIP-0001]. In many places, the text was copied and modified. Although Amir Taaki wrote the BIP-0001 text, Amir is not responsible for its use in the Akash Improvement Process, and should not be bothered with technical questions specific to Akash or the AIP. Please direct all comments to the AIP editors.

## Bibliography

[EIP]: https://github.com/ethereum/EIPs
[Ethereum's EIP-1]: https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1.md
[Bitcoin's BIP-0001]: https://github.com/bitcoin/bips
[Akash Technical Chat]: https://akash.network/chat
[pull request]: https://github.com/ovrclk/AIPs/pulls

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
