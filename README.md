# TRUNK
## User Staking and voting
*Note: TRUNK denomination adds 3 zeros. 1000 = 1 TRUNK

### TestTRUNK

```lua
tTRUNK = "qNDkAsFfwuzB-DodQ1UQtuMFMcSrLfbub2ZdzIB4LIQ"
```
### Set The DAO/Token Address

```lua
TRUNK = "wOrb8b_V8QixWyXZub48Ki5B6OIDyf_p1ngoonsaRpQ"
```
### Stake

```lua
Send({Target = TRUNK, Action = "Stake", Quantity = "[Stake_quantity]"})
```
### See Staked Balance

```lua
Send({Target = TRUNK, Action = "Stakers"})
-- wait for response

TRUNKStakers = require('json').decode(Inbox[#Inbox].Data)

TRUNKStakers["your_staked_address"]
```
### Unstake

```lua
Send({Target = TRUNK, Action = "Unstake", Quantity = "Unstake_quantity" })
```
## Vote/Propose A Vote

```
Send({Target = TRUNK, Action = "Vote", Side = "yay", VoteID = "Insert Vote#", Command = [[Insert command here and use escape quotes]], Prop = "Insert your Porposal text here"})
```
### Propose a vote to change the FRAME

```lua
Send({ Target = TRUNK, Action = "Vote", Side = "yay", Command = [[FrameID= "Arweave_tx_ID_here"]], Prop = "Insert your Porposal text here"})
```

### Vote yay(yes)

```lua
Send({ Target = TRUNK, Action = "Vote", Side = "yay",  VoteID = "current_vote_number" })
```
### Vote nay(no)

```lua
Send({ Target = TRUNK, Action = "Vote", Side = "nay", VoteID = "current_vote_number" })
```

