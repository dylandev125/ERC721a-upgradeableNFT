[![Docs][docs-shield]][docs-url]
[![NPM][npm-shield]][npm-url]
[![CI][ci-shield]][ci-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

<!-- OTHER BADGES -->
<!-- [![Contributors][contributors-shield]][contributors-url] -->
<!-- [![Forks][forks-shield]][forks-url] -->
<!-- [![Stargazers][stars-shield]][stars-url] -->

<!-- ABOUT THE PROJECT -->

## About The Project

This repository hosts the Upgradeable variant of [ERC721A](https://github.com/chiru-labs/ERC721A), meant for use in upgradeable contracts. This variant is available as separate package called `erc721a-upgradeable`.

It follows all of the rules for [Writing Upgradeable Contracts]: constructors are replaced by initializer functions, state variables are initialized in initializer functions, and we additionally check for storage incompatibilities across minor versions.

[writing upgradeable contracts]: https://docs.openzeppelin.com/upgrades-plugins/writing-upgradeable

> :warning: **Warning**
>
> There will be storage incompatibilities across major versions of this package, which makes it unsafe to upgrade a deployed contract from one major version to another, for example from 3.4.0 to 4.0.0.
>
> **It is strongly encouraged to use these contracts together with a tool that can automatically guarantee the safety of an upgradeable contract, such as the [OpenZeppelin Upgrades Plugins](https://github.com/OpenZeppelin/openzeppelin-upgrades).**

This repository is generated by a transpiler.

**Chiru Labs is not liable for any outcomes as a result of using ERC721A and ERC721A-Upgradeable.** DYOR.

<!-- Docs -->

## Docs

https://chiru-labs.github.io/ERC721A/

<!-- Installation -->

## Installation

```sh

npm install --save-dev erc721a-upgradeable

```

<!-- USAGE EXAMPLES -->

## Usage

Once installed, you can use the contracts in the library by importing them:

```solidity
pragma solidity ^0.8.4;

import 'erc721a-upgradeable/contracts/ERC721AUpgradeable.sol';

contract AzukiUpgradeable is ERC721AUpgradeable {
  function initialize() initializer public {
    __ERC721A_init('Azuki', 'AZUKI');
  }

  function mint(uint256 quantity) external payable {
    // _safeMint's second argument now takes in a quantity, not a tokenId.
    _safeMint(msg.sender, quantity);
  }
}

```

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Running tests locally

1. `npm install`
2. `npm run test`

<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<!-- CONTACT -->

## Contact

- 2pm.flow (owner) - [@2pmflow](https://twitter.com/2pmflow)
- location tba (owner) - [@locationtba](https://twitter.com/locationtba)
- cygaar (maintainer) - [@cygaar_dev](https://twitter.com/cygaar_dev)
- vectorized.eth (maintainer) - [@optimizoor](https://twitter.com/optimizoor)

Project Link: [https://github.com/chiru-labs/ERC721A-Upgradeable](https://github.com/chiru-labs/ERC721A-Upgradeable)

<!-- MARKDOWN LINKS & IMAGES -->

<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[docs-shield]: https://img.shields.io/badge/docs-%F0%9F%93%84-blue?style=for-the-badge
[docs-url]: https://chiru-labs.github.io/ERC721A/#/upgradeable
[npm-shield]: https://img.shields.io/npm/v/erc721a-upgradeable.svg?style=for-the-badge
[npm-url]: https://www.npmjs.com/package/erc721a-upgradeable
[ci-shield]: https://img.shields.io/github/workflow/status/chiru-labs/ERC721A-Upgradeable/ERC721A%20Upgradeable%20CI?label=build&style=for-the-badge
[ci-url]: https://github.com/chiru-labs/ERC721A-Upgradeable/actions/workflows/run_tests.yml
[issues-shield]: https://img.shields.io/github/issues/chiru-labs/ERC721A-Upgradeable.svg?style=for-the-badge
[issues-url]: https://github.com/chiru-labs/ERC721A-Upgradeable/issues
[license-shield]: https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge
[license-url]: https://github.com/chiru-labs/ERC721A-Upgradeable/blob/main/LICENSE.txt
