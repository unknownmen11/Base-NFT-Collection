**Base NFT Collection
**```markdown
# Base NFT Collection
npm install @openzeppelin/contracts
// SPDX-License-Identifier: MIT
pragma  ^0.8.0;
import "@openzeppelin/contracts/token/ERC721/ERC721.sol";
contract BaseNFT is ERC721 {
    uint256 private _tokenIdCounter;
    constructor() ERC721("BaseNFT", "BNFT") {}

    function safeMint(address to) public {
        uint256 tokenId = _tokenIdCounter++;
        _safeMint(to, tokenId);
    }
}
