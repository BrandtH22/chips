| CHIP Number   | < Creator must leave this blank. Editor will assign a number.>                                                                                                                                |
|:--------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Title         | Chia Client Puzzles Tab                                                                                                                                                                       |
| Description   | Proposal for a Puzzles tab to be added to the Chia Client. This tab enables users to interact with puzzle primitives (CATs, NFTs, DIDs) and allows community developers to integrate puzzles. |
| Author        | Brandt Holmes (BrandtH22)                                                                                                                                                                     |
| Comments-URI  | < Creator must leave this blank. Editor will assign a URI.>                                                                                                                                   |
| Status        | < Creator must leave this blank. Editor will assign a status.>                                                                                                                                |
| Category      | Process                                                                                                                                                                                       |
| Sub-Category  | Tooling or Environment                                                                                                                                                                        |
| Created       | 2022-09-06                                                                                                                                                                                    |
| Requires      | NA                                                                                                                                                                                            |
| Replaces      | NA                                                                                                                                                                                            |
| Superseded-By | NA                                                                                                                                                                                            |

## Abstract
Proposal for a Puzzles tab to be added to the Chia Client. This tab enables users to interact with puzzle primitives (CATs, NFTs, DIDs) and allows community developers to integrate puzzles (auto-split, gaming, messaging, etc).

For this puzzle tab to be fully functional it should have an associated puzzle store. This puzzle store enables users to view all available puzzles, identify which puzzles have been verified/built by the Chia team, allow community developers to easily integrate new puzzles, monitor users active smart contracts so additional actions can be performed, and establish a donation process for community projects.

These puzzles generally consist of three main parts: a clsp puzzle, driver code, and tests. These components would all need to be accessible for download and integration into the Chia Client at the users request meaning a database of puzzles or a puzzle library would be necessary to support the Puzzles Store.

### Integrating puzzles
Community developers can establish a DID-based identity which enables them to submit their own puzzles and driver code to the Puzzle Library. It is recommended that this puzzle library is created as a consortium of datalayer instances. Each community developer could create 1 or more datalayer instances which houses all three components of their puzzle, an additional datalayer instance hosting the Puzzle Library template would be created. The Puzzle Library template defines a schema for how the Puzzle components datalayer instances should be created for proper integration into the Chia client.

Requirements -
  * Codebase must be functional with the intended Client interface (Chia client, Goby wallet, Evergreen wallet, etc)
  * All required fields in the Puzzle Library Template must be completed
  * All puzzles enter a review period requiring a minimum __ reviews

### Verifying puzzles
Community members can review one another's puzzles using the DID-based identities and provide approvals.
Once __ approvals have been received by community members with at least a __ rating/status then the puzzle will become available in the Puzzle Store.
As developers receive rejections from community members their rating/status is negatively effected

TODO MORE WORDS TO BE ADDED

## Motivation
The Chia Network and community developers have built numerous puzzles that enrich the Chia ecosystem; however, in their current state, these puzzles are difficult for most users to access, integrate, and interact.
The Puzzles Tab and associated Puzzles Store will dramatically reduce this barrier to entry by establishing a single repository for users to access, integrate, and interact with the many puzzles that exist.

Goals:
  * Consolidate puzzles into a single repository
  * Establish a procedure for integrating new puzzles into the ecosystem
  * Ensure that community developers receive appropriate recognition and reward
  * Define a criteria for verifying and reviewing puzzles
  * Reduce entry barriers for accessing, integrating, and interacting with puzzles

  * POTENTIALLY MORE WORDS

Hurdles:
  * Potentially requires integration into the Chia client (this could be integrated into an IDE instead)
  * Time to develop

  * POTENTIALLY MORE??


## Backwards Compatibility
There are no backwards incompatibilities with this proposal, it is designed to be backwards compatible and future-proof.


## Rationale
Describe the reasons for designing your features in the way you have proposed. Make sure to include:
  * Why did you choose your design?
  Backwards compatibility, future-proofing, and removing obfuscations surrounding puzzles
  Forcing users to install a completely separate application to access primitives of the blockchain creates a large barrier to entry
  Users have limited access to current clsp puzzles (chia - cats, nfts, custody solutions, etc ; community - auto-split, gaming, auctions, messaging, etc)
  * What design decisions did you make?
  Integration into the chia client, use of datalayer for puzzle codes, requirement to use DID's for identity
  * What alternative designs did you consider?
  Integration into an IDE, use of IPFS or other decentralized storage, use of public keys for identity
  * How have you achieved community consensus for your design?
  Initial draft will be peer reviewed for community input and consensus, many elements in the proposal enable adaptability for community development.
  * What objections were raised during your discussions with the community, and how does your design address them?


## Specification
List the full technical design specification of any new feature you are proposing. This must include details of all syntax and semantics required to implement each new feature.

This section should be _detailed_. It needs to allow for competing interoperable implementations. When applicable, it may include technical diagrams to accompany your design.

Puzzles Tab -

Puzzles Store -

MEAT AND POTATOES

## Test Cases
  * Addition of puzzles (by Chia or Community dev)
  * Obfuscate or fake ones identity (DID's should be used by developers for proof of identity)
  * Access to another users puzzles
  * Injection of malicious puzzles

  * MORE TEST CASES FOR EDGE CASES


## Reference Implementation
Most Standards Track proposals, as well as some Process proposals, also will require a reference implementation to be included. It should be added to the same folder as your test cases, `assets/chip-<CHIP>`.

Regardless of this proposal's category, the reference implementation does not need to be completed in order to move the CHIP into _Draft_. However, it must be provided before the CHIP can be moved into _Review_.

Puzzles Tab -

Puzzles Store -

EEK THIS IS A LOT OF WORK

## Security
REVIEW TESTS FOR ALREADY IDENTIFIED POTENTIAL EXPLOITS

This section is mandatory for all CHIPs. List all considerations relevant to the security of this proposal if it is implemented. This section may be modified as the proposal moves toward consensus. Make sure to include:
  * Security-related design decisions
  * Important discussions
  * Any security-related guidance
  * All threats and risks, as well as how you are addressing them

## Additional Assets
THIS ONE IS A THINKER

Give a listing of files associated with this CHIP. This list will be added upon as the CHIP moves along the process of approval. All new files should be added to the `assets/chip-<CHIP>` folder. You should link to each individual file here, using relative links.

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
