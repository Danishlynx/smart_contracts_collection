NFT Game and Item Contracts
This repository contains two Solidity smart contracts for a simple NFT (Non-Fungible Token) game:

Item Contract (Item.sol): An ERC721-compliant contract responsible for minting and managing in-game items as NFTs.

Game Contract (Game.sol): A contract that acts as a game platform and NFT repository. Players can deposit and withdraw NFTs to and from the game.

Item Contract
The Item contract inherits from the ERC721 standard and represents in-game items as NFTs.

Functions
constructor(): Initializes the contract and mints 10 initial items, assigning them to the contract deployer.
Game Contract
The Game contract is an NFT game platform that interacts with the Item contract.

Functions
constructor(IERC721 _address): Initializes the game contract with the address of the Item contract.

onERC721Received(...): A required function for handling incoming NFTs. Records the original owner's address when an NFT is received.

depositNFT(uint256 tokenId): Allows a player to deposit their NFT into the game by transferring it to the game contract.

withdrawNFT(uint256 tokenId): Allows the original owner to withdraw their NFT from the game.

Storage
itemNFT: A reference to the Item contract for interaction.

originalOwner: A mapping that stores the original owner's address for each NFT token ID.

Prerequisites
Solidity version 0.8.18
OpenZeppelin library (ERC721 and related contracts)
How to Use
Deploy the Item contract to create the in-game items.

Deploy the Game contract, passing the address of the deployed Item contract.

Players can deposit their NFTs into the game using the depositNFT function.

The original NFT owner can withdraw their NFT from the game using the withdrawNFT function.

Disclaimer
This code is provided as-is without any warranties or guarantees. Use it at your own risk.

License
This code does not specify a license (SPDX-License-Identifier). Make sure to review and apply an appropriate license before using or distributing the code.

For more information about SPDX licenses, visit https://spdx.org/licenses/.
