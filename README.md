# Getting Started

casa.finance is a hybrid protocol bridging real estate financing products through decentralized consensus mechanisms funded by liquidity pools. Opening the door to real estate collateralized loans to the decentralized finance ecosystem built on Ethereum.

This site will serve as a project overview for Uniswap - explaining how it works, how to use it, and how to build on top of it. These docs are actively being worked on and more information will be added on an ongoing basis.

Content
 
1 Intro
2 casa.finance protocol
        	2.1 Lending
		        2.1.1 Due diligence 
        	2.2 Borrowing
        	2.3 Consensus
3 Architecture
        	3.1 Contracts
        	3.2 Rate Mechanics
	        3.3 Credit Models
        	3.4 Risk Profile
        	3.5 Default
        	3.6 Controller
        	3.7 Oracles
        	3.8 Governance
4 Summary




## V1 Features

* Add support for any ERC20 token using the Uniswap [factory](https://github.com/Uniswap/contracts-vyper/blob/master/contracts/uniswap_factory.vy)
* [Join liquidity pools](frontend-integration/pool.md#add-liquidity) to collect fees on ETH-ERC20 pairs
* Liquidity-sensitive automated pricing using [constant product formula](https://github.com/runtimeverification/verified-smart-contracts/blob/uniswap/uniswap/x-y-k.pdf)
* Trade [ETH for any ERC20](frontend-integration/swap.md#eth-erc20-trades) without wrapping
* Trade any [ERC20 for any ERC20](frontend-integration/swap.md#erc20-to-erc20) in a single transaction
* Trade and transfer to a different address in a single transaction
* Lowest gas cost of any decentralized exchange
* Support for private and custom uniswap exchanges
* Buy ERC20 tokens from any wallet using ENS
* [Partially verified](https://github.com/runtimeverification/verified-smart-contracts/tree/uniswap/uniswap) smart contracts written in Vyper
* Mobile-optimized open source [frontend implementation](https://github.com/Uniswap/uniswap-frontend)  
* Funded through an [Ethereum Foundation grant](https://blog.ethereum.org/2018/08/17/ethereum-foundation-grants-update-wave-3/)

## Resources

* [Website](https://casa.finance)
* [Github](https://github.com/casa.finance)
* [Twitter](https://twitter.com/casa.finance)
* [Reddit](https://www.reddit.com/casa.finance)
* [Discord](https://)
* [Email](mailto:contact@casa-finance.io)
* [Whitepaper](https://)

## How it works

## 1 Intro
 
Decentralized finance has portrayed the power of the blockchain, creating a new ecosystem on how money works. The next step is the bridge between defy and tangible assets, to do so there is going to be a technology gap that needs to be filled by a hybrid protocol that allows human inputs to be embedded in the blockchain until the technology gap closes and the process is fully automated.
 
Today there’s still many processes that need human interaction, mainly in the real estate financing industry that goes from property appraisals, property titles and transactional inputs.
 
Through decentralized finance and the blockchain, there’s an opportunity to create a hybrid protocol that gathers input from the tangible world and puts it to work in a more secure, cost efficient and democratic way.
 
This paper will serve as an introduction of a protocol that will serve as the bridge for real estate financing products.
 
## 2 casa.finance protocol
 
Casa is a protocol that allows lenders to fund real estate collateralized loans using the Ethereum blockchain and borrowers to access capital to fund their real estate opportunities. It’s a peer to peer network of lenders and borrowers that transact using real estate collateral and a consensus mechanism that determines rates and credit structures. The hybrid component to the protocol is present with local county and city entities that provide registration services for the mortgages filed that back up the lending notes created in the protocol. * This process we expect to grow into a more decentralized ecosystem with blockchain technology in coming years. 

## 2.1 Lending 

The lending process in casa works in liquidity pools, each liquidity pool has its own conditions which are modified by multiple inputs that go through oracles. (This can be done per deal, or by asset - conditions vary by customer profile score? IMPORTANT, is the pool by deal, is the pool funded by staked usdc, do we fund first and then sell the loan in pieces to providers of liquidity?). A liquidity pool is formed when a borrower request gets approved by the due diligence department (a). Example: Borrower Nick requests a loan for $200,000 usd for a property he is buying at $250,000, LTV is 80% there's a 20% risk buffer based on the asset market value. ARV( After Repair Value) on this asset is 320,000, price is determined by comparable analysis of the area for closed sales of similar condition properties. BPO or appraisal (Human Input, today this analysis is done by an individual, tomorrow this will be an automated process where property conditions can be assessed by computers. 

Zone LP(Liquidity pool by geographic area for example south florida): Committed capital between lenders 1,000,000. 4 real estate assets serve as collateral, at an average LTV of 78%. 

These loans will have governance decisions based on off chain data that establishes the interest rate per file, assuming an organic competition between lenders this will create a competitive rate. When they use the protocol they will be receiving governance tokens as long as their loan is open, this can potentially boost the yield for protocol lenders. 

Lenders provide stablecoins to the liquidity pool; this pool locks the stable coins, and then makes the off ramp through an third party escrow service that will be responsible for funding the transaction. As soon as its funded the lenders will receive a casa token into their wallets that will receive both real interest backed by a collateralized asset on a monthly basis, example: 

#Lender A: 

Capital committed: 200,000 USDC 
Consensus Rate: 8% - 1% Exit 
Period: 12 months 

Lender receives casatoken for amount lent, they will receive in this case $1,333 usdc per month, plus their portion of participation in the governance ecosystem.


Hybrid smart contracts: Offering a powerful, general framework for augmenting existing smart contract capabilities by securely composing on-chain and off-chain computing resources into what we call hybrid smart contracts

on-chain and off-chain components in smart contracts.

Hybrid smart contracts are a first step along the way to this vision and to a concept we call meta contracts. Meta contracts are applications coded on a decentralized metalayer and implicitly encompass on-chain logic (smart contracts), as well as offchain computation and connectivity among various blockchains and existing off-chain services.

Data-source authentication: Tools that enable data providers to digitally sign their data and thereby strengthen the chain of custody between the origin and relying contract. • DON minority reports: Flags issued by a minority subset of DON nodes that observes majority malfeasance in the DON. • Guard rails: Logic on a main chain that detects anomalous conditions and pauses or halts contract execution (or invokes other remediations). • Trust-minimized governance: Use of gradual-release updates to facilitate community inspection, as well as decentralized emergency interventions for rapid response to system failures. • Decentralized entity authentication: Use of public-key infrastructure (PKI) to identify entities in the Chainlink network.

## 2.1.1 Due Diligence 

Offramp data, this ecompasses all the inputs needed for borrowers to access our lending pools. In the initial stage this process will be similar to today's process in the real estate investment industry. Data needed:

Credit check *(Credit checks will be used for the initial round of properties but we will be working with oracles that allow us to merge artificial intelligence inputs into this decisions, creating a more comprehensive score for today financial world)
Property Purchase Contract 
Title Search 
Lien Search 
Title Insurance (These data input will be time limited, we believe properties will start utilizing blockchain technology to record folio numbers and property information, to the point where title insurance policies will not be necessary in this extent)
Investing History (Lending home onboarding process)

## 2.2 Borrowing 

Borrowers portal will work as a Dapp, where they will input loan information for their specific need, a loan request will be created and then the due diligence process starts. 

Borrower's advantage is that they will access a new form of liquidity where rates should represent a discount to regular lenders in the industry, they will also receive governance tokens for the use of the platform, potentially lowering their monthly interest responsibility. 

#Example: 

Borrower A

Capital: 200,000 USD 
Payment Commitment: $1,333 USD
Real estate Tax Bill escrow: TBD
Property Insurance: TBD 

Governance Token example: Borrower receives on a daily basis distribution of the governance token of casa protocol. TBD 

## 2.3 Consensus 

Consensus will serve as the mechanism that establishes the interest rate by borrower, off chain data will serve as data inputs for the consensus decision. The more data the more educated the decision is for the appropriate rate. In the beginning this will be a hybrid process where there will be some human interaction until the technology gap allows the protocolo to run in a decentralized manner for this decision making process. 

# Example: 

Borrower A has a internal consensus score of 9 out of 10, his rate bracket differs in the method expressed below: 

Borrower 
Consensus Score
Rate Bracket 
A
9.5
7%
B
7
9%
C
5
12%
D
8.8
7.5%

## 3. Architecture 

#3.1 Contracts 

Technical Data Input 

#3.2 Rate Mechanics 

How are rates established in the protocol? This is why we label casa a hybrid protocol, in order to merge the defy ecosystem with offchain data providers we need to serve as the bridge between them initially. Off Chain data comes from borrower, city and county data providers (Purpose of today title companies). 

Borrower Profile: 


Credit Score*
760
Flip History*
5 properties last 12 months
KYC 


Investment Summary - Rehab explanation

Property Profile: 
Single Family Home 3-2
Purchase Price: $300,000
LOAN TO VALUE: $240,000 - 80%
Rehab Estimate: 40k
After Repair Value: 55% 
Comparable sales: 420k 450k = 435k 
Lien Search 
BPO- Broker Professional Opinion 

Rates are determined by the consensus score of the individual borrower,  metrics are decided by the governance token holders. Loan to value and credit products are determined by the governance token holders in a voting system. (fei protocol example is good start). 

## 3.3 Credit Models

Initially the protocol will be focused on investment property models, due to their short time period the structure can be tested in shorter time periods, where governance decision and credit metrics adjust to the loan requirements and borrower profile needs. The initial focus will be single family properties and residential multifamily (duplex, triplex, fourplex). After the adjustments are made by the protocol governance and technology gaps are filled for offchain data inputs, the casa.finance protocol goal is to democratize long term personal property loans in a decentralized and trustless ecosystem.

Initial lending models, (To be determined by goverance token holders)

Models 
Parameters
1: Single family purchase Loan
LTV: 70 to 90% 
Interest from 5.99% to 12%
Exit: 0 to 2 points. 
2: Single family purchase Loan + Rehab
Parameters: 
LTV: 70 to 90%
Interest from 5.99% to 12%
Exit: 0 to 2 points. 
3: Single family line of credit loan
LTV: 50 to 70%
Interest from 5.99% to 12%
Origination 0 to 2 Points 
4: Portfolio blanket line of credit loan 
LTV: 50 to 70%
Interest from 5.99% to 12%
Origination 0 to 2 Points 



## 3.4 Risk Profile

## Uniswap Info

Uniswap is made up of a series of ETH-ERC20 exchange contracts. There is exactly one exchange contract per ERC20 token. If a token does not yet have an exchange it can be created by anyone using the Uniswap factory contract. The factory serves as a public registry and is used to look up all token and exchange addresses added to the system.

Each exchange holds reserves of both ETH and its associated ERC20 token. Anyone can become a liquidity provider on an exchange and contribute to its reserves. This is different than buying or selling; it requires depositing an equivalent value of both ETH and the relevant ERC20 token. Liquidity is pooled across all providers and an internal "pool token" \(ERC20\) is used to track each providers relative contribution. Pool tokens are minted when liquidity is deposited into the system and can be burned at any time to withdraw a proportional share of the reserves.

Exchange contracts are automated market makers between an ETH-ERC20 pair. Traders can swap between the two in either direction by adding to the liquidity reserve of one and withdrawing from the reserve of the other. Since ETH is a common pair for all ERC20 exchanges, it can be used as an intermediary allowing direct ERC20-ERC20 trades in a single transaction. Users can specify a recipient address if they want to receive purchased tokens at a different address from the one used to make a transaction.

![ERC20 to ERC20 trades in Uniswap](.gitbook/assets/erc20-to-erc20.png)

Uniswap uses a "constant product" market making formula which sets the exchange rate based off of the relative size of the ETH and ERC20 reserves, and the amount with which an incoming trade shifts this ratio. Selling ETH for ERC20 tokens increases the size of the ETH reserve and decreases the size of the ERC20 reserve. This shifts the reserve ratio, increasing the ERC20 token's price relative to ETH for subsequent transactions. The larger a trade relative to the total size of the reserves, the more price slippage will occur. Essentially, exchange contracts use the open financial market to decide on the relative value of a pair and uses that as a market making strategy.

A small liquidity provider fee \(0.3%\) is taken out of each trade and added to the reserves. While the ETH-ERC20 reserve ratio is constantly shifting, fees makes sure that the total combined reserve size increases with every trade. This functions as a payout to liquidity providers that is collected when they burn their pool tokens to withdraw their portion of total reserves. Guaranteed arbitrage opportunities from price fluctuations should push a steady flow of transactions through the system and increase the amount of fee revenue generated.

Since Uniswap is entirely on-chain, prices can change between when a transaction is signed and when it is included in a block. Traders can bound price fluctuations by specifying the minimum amount bought on sell orders, or the maximum amount sold on buy orders. This acts as a limit order that will automatically cancel if it is not filled. It is also possible to set transaction deadlines which will cancel orders if they are not executed fast enough.

The reason only one exchange per token can be registered to the factory is to encourage providers to pool their liquidity into a single reserve. However, Uniswap has built in support for ERC20-to-ERC20 trades using the public pools from the factory on one side of the transaction and custom, user-specified pool on the other. Custom pools could have fund managers, use alternate pricing mechanisms, remove liquidity provider fees, integrate complex three dimensional fomo-based ponzi-schemes and more. They just need to implement the Uniswap interface and accept ETH as an intermediary asset. Custom pools do not have the same safety properties as the public ones. It is recommended users only interact with audited, open-source smart contracts.

Upgrading censorship resistant, decentralized smart contracts is difficult. If significant improvements are made to the system a new version will be released. Liquidity providers can choose between moving to the new system or staying in the old one. If possible, new versions will be backwards compatible and able to trade ERC20-to-ERC20 with the old versions similar to a custom pool.

## How to use it

[Uniswap.io](https://uniswap.io) is the landing page for the Uniswap protocol. It describes the project and directs users where they need to go.

The Uniswap smart contracts live on Ethereum. Anyone can interact with them directly.

The Uniswap frontend is an open source interface designed to improve user experience when interacting with the smart contracts. Anyone can use the source code to host an interface, or build their own. Hosted interfaces are independent of Uniswap, and should comply with their jurisdictional laws and regulations.

### List of interfaces \(updated November 2, 2018\)

* [Uniswap.exchange](https://uniswap.exchange)

