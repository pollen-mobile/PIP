# PIP-0001 Anti Gaming Proposal
- **Author(s):** @anders462
- **Start Date:** May 20th, 2022
- **Category:** Rewards Gaming
- **Status:** Draft

## Overview
Gaming is unavoidable in any rewards incentivited utility blockchain project. It's important to curb this as soon as possible while the number of network participants is relatively small. If gaming vectors is not surfaced and addressed these issues will make new and excisting disenfranchised and lose their incentive to build the network. New gaming method will clearly always be developed after we closed the most obvious loop holes and this should be recocnized as a continous process.


 This proposal aimes in: 
 * Highligthing the current known gaming vectors and potenital not yet exploited ones
 * Actively suggest ways for the community to find possible new gaming schemes, active gamers etc.
 * Make suggestion to solve/or mitigate known gaming vectors
 * Enable a discussion to acheive the best approach to address the gaming that community supports
 * Suggest other solution to early detect, incentatives bounties to find gamers or discover loop holes.
 

## Rationale
* To curb gaming as soon as possible while the number of network participants is relatively small before it affects network participant confidence in the Pollen project. * Be a role model to quickly indentify and address rewards gaming in the DeWi space.


## Summary of current gaming activity and implemented remidies
See Appendix 1.


### Spoofing GPS with SDR (Software Defined Radio)
* A bit more technical but not that hard todo. The basic principal is to use SDR to transmitt low power fake GPS transmissions that could re loacate BB's to game hex validation as long as the BB is in the coverage area of a Flower. HB drops could also be spoofed in this manner.

 
#### Pollen addressing this exploit:
 1. No current fix known to be implemented. 
 2. Use signal strength and FSPL to filter out impossible validation location (possible to game this as well though)
 3. Use assisted GPS, location of other know celluar network towers, WIFI hotspots etc.


### Violation remedies
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

#### Pollen addressed this exploits in phases:
 1. BB Anti Swarming (Rewards split if 2 or more BB's validate a hex at the same time).
 2. Max hex validation per flower set to fixed number regardless if BB's validate more unique hexes (D = 7, C = 7, E = 10 and BC = 20). Flower and BB's still get 2 pics each for each unique hex however up to max for flower per BB.

#### What could further be done. 
1. Reduce max Hex for a Camellia as its the most commonly gamed. 
 * Motivation: Its an indoor flower, a hex is several city block, and its therefore not possible for a Camellia to cover more then 1 hex.
 *  Side effects: A Camellia could be place in an outdoor enclosure on balcony, roof etc plus this would effect C owners that never gamed the rewards as well.
2. Use signal strength FSPL to filter out impossibles validation location.
3. Require certain number of GPS satellite looks before validation is possible to minimize drift.

### The moving Flower
* Deliberate exploit by driving around with a flower (C or D), powered by battery and tethered internet connection. 
* Flower and BBs could be in the same vehicle and new hexes could be validated while driving to new hexes. This scheme resulted in the same large rewards as the GPS drift exploit. Early on many BBs could validate hexes at the same time, flowers got 10 pics per BB and hex etc. 

#### Pollen addressed this exploits in phases (Same fixes as for GPS drift):
 1. BB Anti Swarming (Rewards split if 2 or more BB's validate a hex at the same time).
 2. Max hex validation per flower set to fixed number regardless if BB's validate more unique hexes (D = 7, C = 7, E = 10 and BC = 20). Flower and BB's still get 2 pics each for each unique hex however up to max for flower per BB.

#### What could further be done. 
1. If a flower changes GPS location the flower wouldnt get any rewards for that day. 
 * Motivation: Moving a flower would have a fee (similar to Helium) but the fee would be a loss of rewards not something flower owner have to pay.
 *  Side effects: Possible GPS drift could cause rewards loss. Could be mitagted in post process of data.
2. Require uptime for flowers. This has already been discussed due this exploit but also from network availabilty point of view. Doesnt really solve the issue as USP could be used

### HoneyBee Mobile Software GPS spoofing
* Any one ever played games knows its pretty easy using software and a connected mobile to spoof GPS location and even pre configure routes that would enable automatic pollen drops. As a HB can earn up to 100drops per day a 0.1pics a total of 10pics could be rewarded per HB without doing any effort. HB require a pollen ESIM that is on in a Band48 device. The Band 48 limitation means its a bit harder to replicate outside the US (at least its my assumption).
* 10 pics is not that significant but if HB is released in masses it could become
 
#### Pollen addressing this exploit:
 1. Pollen is currently testing an iphone solution to detect this type of spoofing. Android dont have a HB app at the moment so no spoofing an be done.

### Hummingbird ESIM toggle
* Intitally kits was sold with Flower + BB + 5 HB. User of the ESIMS use them on one mobile phone and toggle them off/on daily to get the 1 pic per ESIM
* Relatively small issue as its only 1 Pic per device. Could become a major issue when ESIMS is readly sold with no restrictions.
* As phones need to be relatively new and need flower coverage to work, its hard for users to find neighboors and family to give esims to. Further its crypto project that makes it even harder to "give" these away. Alternative for many is un used ESIMS. 
 
#### Pollen addressing this exploit:
 1. No current fix known to be implemented. 
 2. Using IMEI wouldn't work as H is supposed to be private and the only identifier being a NFT.
 3. Possibly a check of how long a device ESIM been active could be used, short attach to flower wouldnt give the 1pic for example.
