# TRUNK
## User Staking and voting

Set MemeFrame Address

```lua
TRUNK = "OT9qTE2467gcozb2g8R6D6N3nQS94ENcaAIJfUzHCww"
```

First the users need CRED and should transfer the CRED to your MemeFrams

```lua
Send({Target = CRED, Action = "Transfer", Quantity = "1000", Recipient = TRUNK})
```

Stake

```lua
Send({Target = TRUNK, Action = "[Stake quantity]", Quantity = "1000", UnstakeDelay = "1000" })
```

Vote to change the FRAME

```lua
Send({ Target = TRUNK, Action = "Vote", Side = "yay", TXID="..." })
```

## Need Help

[Support channel in AO Discord](https://discord.gg/J6kQXpdPG3)
[Cookbook](https://cookbook_ao.g8way.io)
