# Decentralized Cloud Standards (DCS)

Decentralized Cloud Standards (DCSs) describe standards for the [Akash](https://akash.network) Decentralized Cloud platform, including core protocol specifications, client APIs, and SDL standards.

## Contributing

1. Review [DCS-1](spec/dcs-1).
2. Fork the repository by clicking "Fork" in the top right.
3. Add your DCS to your fork of the repository. There is a [template DCS here](dcs-template.md).
4. Submit a Pull Request to Akash's [DCSs repository](https://github.com/ovrclk/dcs).

Your first PR should be a first draft of the final DCS. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new DCS and assign it a number before merging it. Make sure you include a discussions-to header with the URL to a discussion forum or open GitHub issue where people can discuss the DCS as a whole.

If your DCS requires images, the image files should be included in a subdirectory of the assets folder for that DCS as follows: `assets/dcs-N` (where N is to be replaced with the DCS number). When linking to an image in the DCS, use relative links such as `../assets/dcs-1/image.png`.

Once your first PR is merged, we have a bot that helps out by automatically merging PRs to draft DCSs. For this to work, it has to be able to tell that you own the draft being edited. Make sure that the `author` line of your DCS contains either your GitHub username or your email address inside . If you use your email address, that address must be the one publicly shown on your GitHub profile.

When you believe your DCS is mature and ready to progress past the draft phase, open a PR changing the state of your DCS to 'Final.' An editor will review your draft and ask if anyone objects to its being finalized. If the editor decides there is no rough consensus - for instance, because contributors point out significant issues with the DCS - they may close the PR and request that you fix the issues in the draft before trying again.

## DCS Status Terms

* **Draft** - an DCS that is undergoing rapid iteration and changes.
* **Last Call** - an DCS that is done with its initial iteration and ready for review by a wide audience.
* **Accepted** - a core DCS that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author. The process for Core Devs to decide whether to encode an DCS into their clients as part of a hard fork is not part of the EIP process. If such a decision is made, the DCS will move to final.
* **Final (non-Core)** - an DCS that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author.
* **Final (Core)** - an DCS that the Core Devs have decided to implement and release in a future hard fork or has already been released in a hard fork.
