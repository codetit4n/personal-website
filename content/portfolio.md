---
title: "Portfolio"
layout: "portfolio"
url: "/portfolio"
summary: portfolio
---

## LYNC WORLD - GameFi Infrastructure

#### [Website](https://www.lync.world/) . [Blog](https://lyncworld.medium.com/) . [Twitter](https://twitter.com/Lyncworld) . [LinkedIn](https://www.linkedin.com/company/lync-world/) . [Discord](https://discord.com/invite/R8s8NGauRn) . [GitHub](https://github.com/LYNC-WORLD)

##### Jan 2023 - Present

LYNC is one stop solution for game developers to push their on chain without Web3 complexities.
Currently I am working here as a full time Blockchain Developer.

### Some things we are building

- NFT Minter: Launch your custom NFT collections on various blockchains like
  [Ethereum](https://ethereum.org/),
  [Polygon](https://polygon.technology/),
  [zkSync era](https://zksync.io/),
  [Polygon zkEVM](https://polygon.technology/polygon-zkevm),
  [Filecoin Virtual Machine](https://fvm.filecoin.io/),
  [Hedera hashgraph](https://hedera.com/),
  [Astar](https://astar.network/),
  [Mantle](https://www.mantle.xyz/),
  [Arbitrum](https://arbitrum.io/) with features like deploying, verifying on block explorers, and
  minting.

- Non-Custodial Marketplaces: Buy, Sell, Rent and Lend your NFTs without giving up the ownership.
- Cross chain NFT Lending & Renting using [axelar network](https://axelar.network/).
- Dynamic NFTs - [ETHGlobal Showcase](https://ethglobal.com/showcase/dna-dynamic-nft-asset-9zx0r).

### Tech stack (day to day work)

1. Blockchain: Solidity, Rust, TypeScript, JavaScript, Hardhat framework, Subgraphs using
   [thegraph](https://thegraph.com/).

2. Frontend: TypeScript, JavaScript, Next.Js, Vite, React.Js, Ethers.js, Web3.Js, GraphQL, thegraph data
   using GraphQL, various API integrations like [Alchemy APIs](https://www.alchemy.com/),
   [Moralis APIs](https://moralis.io/), [biconomy](https://www.biconomy.io/), etc

3. Backend: Node.Js, Express.Js, MongoDB, JavaScript.

4. R&D: Keeping up with the new Blockchain tech like
   [Account abstraction](https://eips.ethereum.org/EIPS/eip-4337),
   [Blockchain Interoperability](https://blog.chain.link/blockchain-interoperability/), etc.

---

## USDAO and OnVault - Defi Projects

#### [Website](https://www.usdao.io/) . [Docs](https://docs.usdao.io/) . [Twitter](https://twitter.com/usdao_io) . [LinkedIn](https://www.linkedin.com/company/usdaoofficial) . [Blog](https://usdao.medium.com/)

##### Jan 2022 - Jan 2023

USDAO is a decentralized crypto-backed stablecoin intended to serve as a global currency.
[OnVault](https://onvault.usdao.io/ "onvault dApp") is a lending protocol which lends out USDAO
taking ETH as collateral.

{{< collapse summary="More Details">}}

### About USDAO and OnVault

- USDAO is a stablecoin pegged 1:1 to the USD.
- Since, it's a DAO we have another token to govern it called ASSET.
- OnVault is another project under USDAO. It is a borrowing protocol for users of USDAO to take out USDAO
  loans giving their ETH as collateral.
- All loans on OnVault can be taken out at 110% collateral ratio. So, to take out 100 USDAO you will need
  at least 110 USD worth of ether.
- OnVault has features like liquidations for undercollateralized debt positions, staking/stability providing,
  etc.
- If you stake/provide stability in OnVault you are rewarded in ASSET tokens which can be used to govern
  USDAO protocol.
- If your debt position goes below the minimum allowed, it will be liquidated.
- When a liquidation happens the debt is offset with the USDAO in the stability pool/ staked USDAO.
- Anyone can do liquidations for undercollateralized debt positions and they will be rewarded for that.
- This system takes inspiration from [Liquity Protocol](https://www.liquity.org/).

### My Work

1.  Blockchain: Solidity, JavaScript, Hardhat, Truffle, TypeScript, [thegraph](https://thegraph.com/ "thegraph website"), GraphQL.

    - Created core smart contracts for OnVault and improved the existing USDAO smart contracts.
    - Created subgraphs using [thegraph](https://thegraph.com/ "thegraph website") and TypeScript to track
      USDAO and OnVault smart contract transactions.
    - Integrated various liquidity pools like [UniSwap](https://uniswap.org/),
      [Yearn](https://yearn.finance/), [Compound](https://compound.finance/), [Aave](https://aave.com/), etc
      with our smart contracts.
    - Wrote test cases for various smart contract functionality.
    - Did some simulations regarding how the USDAO peg will hold in various market conditions using
      historical data.
    - Documented the code on [GitHub](https://github.com/USDAO-Protocol) and
      [GitBook](https://docs.usdao.io/).

2.  Frontend: JavaScript, React.Js, Ethers.js, Web3.js, GraphQL, thegraph etc.

    - Integrated various smart contracts functionality with the frontend using ethers.js, web3.js,
      GraphQL(for thegraph), etc.

3.  Looked into various protocols like [Liquity](https://www.liquity.org/),
    [OlympusDAO](https://www.olympusdao.finance/), [MakerDAO](https://makerdao.com/),
    [UniSwap](https://uniswap.org/), [Curve.fi](https://curve.fi/), etc and studied their smart contracts.

{{< /collapse >}}

---

## Nalnda - NFT based e-books Marketplace

#### [Website](https://nalnda.com/) . [Docs](https://docs.nalnda.com/) . [Twitter](https://twitter.com/nalndamktplace) . [LinkedIn](https://www.linkedin.com/company/nalnda) . [Blog](https://nalndamktplace.medium.com/) . [GitHub](https://github.com/nalndamktplace)

##### May 2022 - June 2022

Social marketplace for NFT based e-books (or nBooks), with features like primary sales, secondary sales,
commissions, etc.

{{< collapse summary="More Details">}}

### About Nalnda

- Every e-book is represented by an ERC721 contract.
- The NFTs/tokens under a particular ERC-721 contract(or e-book) are called book covers.
- If you own a book cover/ NFT you own a copy of that book and can read it on the platform.
- The actual book is not stored publicly on IPFS. It is rather stored on a private IPFS node using the
  [submarine service](https://www.pinata.cloud/submarine) from [Pinata](https://www.pinata.cloud/)
- [Submarine service](https://www.pinata.cloud/submarine) gives access to a particular e-book if you own
  an NFT of that book.
- The marketplace has 2 types of sales happening on it:
  1. Primary sale: This is basically when a cover or NFT gets minted (lazy minting) for a fixed cost.
  2. Secondary sale: This is when some cover or NFT owner puts its NFT up for sale on our marketplace.
- Nalnda also implements something called as Initial Title Offering(or ITO):

  - Initial Title Offering allows authors to safeguard the minimum no. of books they can sell. On avg.,
    a title doesn't sell more than 450 copies. Nalnda helps authors to cross this chasm by providing a
    platform where they can market their books and launch them for a minimum no. of readers.
  - Readers who will participate in ITO will get a %age of royalty from all the future sales on Nalnda
    platform as well as from the sale of printed books.
  - This model benefits both the readers and the authors. Authors can earn optimal revenue from the sale
    of their book from ITO and readers who take the risk by investing in the book are rewarded with
    royalty %age from the future sale of the books.
  - Also, since these readers have invested in the book, they would market it on behalf of the authors
    thus helping him with the marketing without additional cost.

### My Work

- Worked part time here as a Blockchain Developer.
- Created all the smart contracts like Initial Title Offering(ITO) model, ERC721 contracts(representing
  each e-book), Escrow contract for trading NFTs, etc using solidity, Hardhat framework, JavaScript.
- These smart contracts are public on GitHub: https://github.com/nalndamktplace/smart-contracts
- Wrote test cases for all smart contract functionality.
- Helped in implementing Pinata's submarine service along with the frontend team.
- Created subgraphs to track transactions happening on the platform using TypeScript and
  [thegraph](https://thegraph.com/ "thegraph website").

{{< /collapse >}}

---

## Niftomania - NFT trading platform

#### [Twitter](https://twitter.com/niftomania) . [Instagram](https://www.instagram.com/niftomania)

##### May 2021 - Nov 2021

NFT trading platform with features like creating, buying, selling, auctioning NFTs.

{{< collapse summary="More Details">}}

### About Niftomania

- Creators can mint their own NFTs.
- Creators can choose type of NFT contract(ERC721/ERC1155) to mint.
- Creators can set a royalty percentage which will be sent to them on every transaction.
- Anyone can list the NFTs they own for sale/auctions.
- There are 2 types of transactions happening here:
  1. Direct sales: People buy listed NFTs at sale price.
  2. Auctions: People bid on the NFT and the highest bid in a particular timeframe (set by the lister)
     wins the auction and gets the NFT.

### My Work

- Worked as an intern on this project during my college time.
- Created smart contracts(written in solidity) for the protocol.
- Created the frontend app using Web3.Js, React, JavaScript.
- Integrated GraphQL APIs to get data from the blockchain using [thegraph](https://thegraph.com/ "thegraph 
website") protocol.

{{< /collapse >}}

---

## Pharmaceutical Supply Chain Simulation

#### [Code](https://github.com/codeTIT4N/supply-chain-truffle-react) . [Video](https://www.youtube.com/watch?v=2e-NGuT1PnY)

Simulating a Pharmaceutical Supply Chain use case using blockchain.

{{< collapse summary="More Details">}}

- This was an old side project.
- All medicines go through various stages of the supply chain like supplying of raw materials, manufacturing,
  distributing and retail.
- All of the above mentioned stages are stored on the blockchain using transactions.
- Anyone can track medicines through the various stages using the interface as it is stored on a
  public ledger(blockchain).
- Tech Stack
  - Blockchain: Solidity, Truffle framework, JavaScript.
  - Frontend: React.Js, JavaScript, Web3.js.

{{< /collapse >}}

---

## BlockVote - Blockchain based e-voting system

#### [PPT](https://docs.google.com/presentation/d/1IhWUhTT83LxtYjHR52xJUV2uIY6eam8v/edit?usp=sharing&ouid=116527115944155558520&rtpof=true&sd=true)

Simple Blockchain based e-voting system.

{{< collapse summary="More Details">}}

- My first blockchain project.
- Admin starts/ends elections, Adds candidates, Deletes candidates.
- Voters can login using their email password (built using firebase) and vote.
- All the candidates are stored on blockchain and their vote count increases as people vote for them.
- Anyone can view the election results after the election.
- Tech Stack
  - Blockchain: Solidity, Truffle framework, Ganache.
  - Frontend: [Firebase](https://firebase.google.com/), React.Js, Web3.Js, [Drizzle framework](https://trufflesuite.com/drizzle/).

{{< /collapse >}}

---
