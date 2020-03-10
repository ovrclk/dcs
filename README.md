# Akash Improvement Proposals (AIPs)

Akash Improvement Proposals (AIPs) describe standards for the Akash platform, including core protocol specifications, client APIs, and SDL standards.

## Contributing

1. Review [AIP-1](AIPS/aip-1.md).
2. Fork the repository by clicking "Fork" in the top right.
3. Add your AIP to your fork of the repository. There is a [template AIP here](aip-template.md).
4. Submit a Pull Request to Akash's [AIPs repository](https://github.com/ovrclk/EIPs).

Your first PR should be a first draft of the final AIP. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new AIP and assign it a number before merging it. Make sure you include a discussions-to header with the URL to a discussion forum or open GitHub issue where people can discuss the AIP as a whole.

If your AIP requires images, the image files should be included in a subdirectory of the assets folder for that AIP as follows: assets/aip-N (where N is to be replaced with the AIP number). When linking to an image in the AIP, use relative links such as ../assets/aip-1/image.png.
Once your first PR is merged, we have a bot that helps out by automatically merging PRs to draft AIPs. For this to work, it has to be able to tell that you own the draft being edited. Make sure that the 'author' line of your AIP contains either your GitHub username or your email address inside . If you use your email address, that address must be the one publicly shown on your GitHub profile.

When you believe your AIP is mature and ready to progress past the draft phase, open a PR changing the state of your AIP to 'Final.' An editor will review your draft and ask if anyone objects to its being finalized. If the editor decides there is no rough consensus - for instance, because contributors point out significant issues with the AIP - they may close the PR and request that you fix the issues in the draft before trying again.

## AIP Status Terms

* **Draft** - an AIP that is undergoing rapid iteration and changes.
* **Last Call** - an AIP that is done with its initial iteration and ready for review by a wide audience.
* **Accepted** - a core AIP that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author. The process for Core Devs to decide whether to encode an AIP into their clients as part of a hard fork is not part of the EIP process. If such a decision is made, the AIP will move to final.
* **Final (non-Core)** - an AIP that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author.
* **Final (Core)** - an AIP that the Core Devs have decided to implement and release in a future hard fork or has already been released in a hard fork.

## Credits

This repository is inspired by Ethereum Improvement Proposal Repository ([EIPs](https://github.com/ethereum/EIPs))
