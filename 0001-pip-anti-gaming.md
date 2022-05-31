# PIP-0001 Anti Gaming Proposal
- **Author(s):** @anders462
- **Start Date:** May 20th, 2022
- **Category:** Rewards Gaming
- **Status:** Draft

## Overview
Gaming is unavoidable in any rewards incentivited utility blockchain project. It's important to curb this as soon as possible while the number of network participants is relatively small. If gaming vectors is not actively indentified and addressed these issues will make new and excisting network participants disenfranchised and lose their incentive to build the network. New gaming method will clearly always be developed after we closed the most obvious loop holes and this should be recocnized as a continous process and need communinity envolvement.

## Definitions
- F = Flower
- BC = Buttercup, 20 Hex (outdoor flower CPI required)
- D = Dandellion, 7 Hex (outdoor small cell flower)
- E = ElderFlower, 10 Hex (outdoor small cell flower)
- C = Camelia, 7 Hex (indoor flower)
- BB = Bumblebee (HW validator)
- HB = HoneyBee App with ESIM (SW Validator)
- H = Hummmingbird (regular ESIM)

 This proposal aimes in: 
 * Give overview of gaming schemes that have been already been exploited
 * Indentify new potential gaming exploits which might be used or could be used
 * Propose detailed solution to mitigate or ellimintate expolits these *new* exploits
 * Propose detailed solutions to further enhance mitigation or elliminate *already indentified* exploits (see Appendix 1.)
 * Propose penalities for different types of gaming
 * Actively suggest ways for the community to find possible new gaming schemes, active gamers, incentive bounties etc.


## Rationale
* To curb gaming as soon as possible while the number of network participants is relatively small before it affects network participant confidence in the Pollen project. * Be a role model to quickly indentify and address rewards gaming in the DeWi space.


## Summary of historic gaming activity and what has been done to mitigate or ellinate them
See Appendix 1.

## New potential Gaming Exploits
This exploits might already be going on but at the moment we don't have evidence for this

### Spoofing GPS with SDR (Software Defined Radio)
* Without going into to many details a SDR can create any RF signal and this includes a GPS signal. When SDR is placed close to a Mobile Phone or a Bumblebee it will make these devices think they are in a specific location set my the operator. 
** 1. Could spoof bumblebee Hex validation. Note: Operator still need to have connection to flower for this to work. For example a flower with limted coverage or a flower placed in an apartment could validate the full 7 hexes without the bumblebee ever be in the hex or those hex's actually have coverage.
** 2. Could spoof pollen drops for both BB and HB  

 
#### Potential action could the taken for SDR spoofing (WIP)
 1. Use signal strength and FSPL to filter out impossible validation location (possible to game this as well though)
 2. Use assisted GPS, location of other know celluar network towers, WIFI hotspots etc.


#### New Anti gaming measures for excisting indentified exploits see Appendix 1. (WIP)
1. Reduce max Hex for a Camellia as its the most commonly gamed. 
 * Motivation: Its an indoor flower, a hex is several city block, and its therefore not possible for a Camellia to cover more then 1 hex.
 *  Side effects: A Camellia could be place in an outdoor enclosure on balcony, roof etc plus this would effect C owners that never gamed the rewards as well.
2. Use signal strength FSPL to filter out impossibles validation location for GPS drift and SDR spoofing.
3. Require certain number of GPS satellite looks before validation is possible to minimize drift for reduce GPS Drift exploits.
4. Require a certain amount of time a day a H need to be connected to lessen massive ESIM toggling.
5. If a flower changes GPS location the flower wouldnt get any rewards for that day to reduce C, D and E moves to increase validated hex count 
 * Motivation: Moving a flower would have a fee (similar to Helium) but the fee would be a loss of rewards not something flower owner have to pay.
 *  Side effects: Possible GPS drift could cause rewards loss. Could be mitagted in post process of data.
6. Require uptime for flowers which is benifital and necessary for a mobile data network. Aim should be in time to get to 99%. This has to be done in phases however as flower owners get UPS, backhaul fail over in place:
* Motivation.: Flower owners that do a good job and have a very high uptime will most likely not game and have better installation in general by having stable internet connection backhaul either with Business ISP connection with SLA or alternative backhaul failover as satellite etc. Further this flower owner will have UPS battery packup for incindetial power loss or utility planned rolleing outages during peak months.


### Violation remedies (WIP)
1. Set priority/severity of exploits
2. Set appropriate community approved remedies (rewards reductions, ban-list etc)


- *Technical Requirements*
- *Architectural Requirements*
- *Governance Requirements*

## Implementation Details
*In order to accomplish X, the following needs to be considered...*

- *Who are the stakeholders? Who gets affected by this proposal?*
- *What processes, documentation, tools, etc. need to be updated with this proposal?*
- *What is the timeline?*

## Pros and Cons
*Why would we not do this? How do the pros outweight the cons?*

## Unresolved Questions
*The following questions remain...*

## Success Metrics
*The following metrics should be measured to help us understand...*

- *An increase in performance or stability*
- *A decrease in complexity or frustration*


## Appendix 1. 

### GPS Drift Exploit
* Deliberate exploit of GPS drift in high rises with high energy windows
* By placing BB's in high rises in cities with such buildings, this exploit created a large of amount of false validation in hexes where the BB's never visited. Even if the GPS drift was not spoofed per say, it was exploited and resulted in large rewards in the early state of the project. By using several BB's, each BB could validate max hexes for a flower,. As an example one Camellia with 5 BB's could validate 5 * 7 = 35 Hex's, earning a total of 35 * 1 (BB's) (changed to 2 later) + 35 * (10 + 1) (changed to 2 later)  = 420 Pics early in the project when flowers got 10Pics per hex per BB and there where no total hex limitation. Before anti swarming, both Camellia and all the BB's could be in the same apartment.
* It should be pointed out that gamers have worked with Pollen team after the fact to inform them about this issue and how to discover this in system logs. 


### The moving Flower
* Deliberate exploit by driving around with a flower (C or D), powered by battery and tethered internet connection. 
* Flower and BBs could be in the same vehicle and new hexes could be validated while driving to new hexes. This scheme resulted in the same large rewards as the GPS drift exploit. Early on many BBs could validate hexes at the same time, flowers got 10 pics per BB and hex etc. 


### HoneyBee Mobile Software GPS spoofing
* Any one ever played games knows its pretty easy using software and a connected mobile to spoof GPS location and even pre configure routes that would enable automatic pollen drops. As a HB can earn up to 100drops per day a 0.1pics a total of 10pics could be rewarded per HB without doing any effort. HB require a pollen ESIM that is on in a Band48 device. The Band 48 limitation means its a bit harder to replicate outside the US (at least its my assumption).
* 10 pics is not that significant but if HB is released in masses it could become
 

### Hummingbird ESIM toggle
* Intitally kits was sold with Flower + BB + 5 HB. User of the ESIMS use them on one mobile phone and toggle them off/on daily to get the 1 pic per ESIM
* Relatively small issue as its only 1 Pic per device. Could become a major issue when ESIMS is readly sold with no restrictions.
* As phones need to be relatively new and need flower coverage to work, its hard for users to find neighboors and family to give esims to. Further its crypto project that makes it even harder to "give" these away. Alternative for many is un used ESIMS. 

