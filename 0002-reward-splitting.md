Pollen Improvement Proposal-0002 Reward Splitting

•	Author(s):  Max Gold
•	Start Date: July 12, 2022
•	Category: Economic


Overview


The purpose this proposal is to create an on-chain reward split for any PCN earnings derived from flowers by giving flower owners the ability to split reward payouts based on fixed percentages to their hosts, installers, etc.

Rationale

The flower-as-an-NFT system is currently designed to pay out PCN rewards to a single wallet. This design can be problematic whenever the work or resources necessary to deploy a flower are provided by multiple people as the PCN rewards must be split up equitably between several wallets. Many of the common workarounds for this problem require more trust, time, energy, technical expertise, or resources than is desirable. The ability to split rewards on-chain would help resolve this issue by eliminating the need for these workarounds in many use cases.
An additional motivation for this transition is the added possibility of flower securitization. Flower securitization could offer various benefits to both flower owners ('sellers') and flower investors ('buyers'). Sellers would be able to access advantages such as lower capital requirements, reduced deployment risk, and the ability to access various goods and services that would otherwise be unattainable. Buyers would be able to access advantages such as increased portfolio diversification, the ability to invest solely in high-value hotspot placements, and the ability to mine PCN with relatively little effort.

Details

I propose a system of masterNFTs and subNFTs to accomplish this goal.  Every flower currently exists on chain as an NFT with rewards being emitted daily based on their performance to the wallet that holds that NFT.  Under the proposed system, those NFTs would be considered the masterNFT and have the ability to mint more NFTs, subNFTs.  Similar to a gaming NFT that has the ability to update its attributes, the masterNFT would be able to be editable to direct percentages of its rewards to its different subNFTs.  The flower owner would simply sent a subNFT to a host and control what percentage of the rewards were apportioned to each subNFT.  If a host decides they no longer wish to host a flower, or that host has its wallet compromised in any way, the masterNFT can simply change that subNFT’s payout percentage to 0.  
More work needs to be done to figure out how to get this mechanism to be functional and any help from community would be greatly appreciated to accomplish the NFT piece.  It is my assumption that an app would need to be developed to make the NFT editing possible.

Implementation Details

In order to accomplish this, the following needs to be considered...
•	What are the technical hurdles to creating editable NFTs?
•	Will an app need to be built on top?
•	What is cost of creating these NFTs?
•	How will the additional payouts affect the scaling of the PCN payout system?
•	Should this be “opt-in” and require a payment in either SOL or PCN to cover any added transaction costs that Pollen Opco will incur as a result?

Pros and Cons

The cost of setting up this type of a structure with automatic reward splitting will be cheaper than the current legacy systems of paying third party applications like Hotspotty to calculate reward splits.  These third party applications as well as privately developed internal applications by some fleet operators will require a large number of API pulls that will be detrimental to the UX of the Pollen explorer as the network scales.  Any money spent calculating reward splitting off chain either through dashboard as a service companies or developing internal tools would likely be spent on purchasing and deploying more equipment, strengthening the network as a whole.  This would also create a clear differentiator for potential enterprise fleets over other options like Helium 5G which does not have the ability to do on-chain reward splitting, nor will they with the current architecture of the Helium L1.

Unresolved Questions

What is the potential cost of per day to do this? 
What are the added legal complexities associated with securitization?
Will network participants misinterpreting a rewards split as being determinant in ownership?

Success Metrics
I believe that many flowers will have their rewards split between multiple addresses after this functionality is deployed. I also believe that this deployed functionality will have a notable impact on the positive-feedback loop that will drive Pollen Network deployment as it will reduce the friction associated with establishing relationships between flower owners and flower hosts.  If Pollen is able have large scale deployments operating on revenue share agreements without the need for third party apps to be built to manage fleet payouts this will be deemed a success.

