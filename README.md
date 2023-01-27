# Smart Contracts Bug Classes
Not definitive - in progress

- [ ] Unchecked inputs
- No checks on inputs
- No bounds defined
- No limits on quantities (eg. number of mintable NFTs)
- Src and Dst can be equal (eg. transfer to one-self)
- Address can be zero
- Use of isContract (check can be avoided)

- [ ] Unchecked return values
- Transfer return value is not checked

- [ ] Reentrancy
- Function has no protection
- Function has no Checks-Effects-Interaction pattern
- Function use call instead of transfer
- Function supports ERC777 / ERC721
- Function supports a standard with allows hooks

- [ ] Frontrunning
- Transaction can be queued at the front of another transaction
- Transaction can be repeated

- [ ] Access control
- Function is critical but it's public/external instead of private/internal
- Function can't be reached (eg. onlyOwner but contract has no owner)

- [ ] Contract state confusion
- Contract use critical variables that needs to be constantly checked
- Critical variables are not updated / not checked / outdated / wrong

- [ ] Functionality abuse
- Function can be called indefinitely
- Function allows to split transactions

- [ ] Denial of Service (DOS)
- Function allows reentrancy
- Function can interact with an user smart contract
- Use of SafeTransfer in conditions where it always revert
- Use of call with few gas where fallback will consume more
- For loops can be controlled by the user
- Array lenght can be incremented externally

- [ ] Wrong math
- Division before multiplication
- Division by zero / Denominator can be zero

- [ ] Wrong conditional logic
- Condition is missing / is wrong / is reversed
- Condition can't be reached (eg. return before require or if)
- Condition is always true or false
- Condition does not account for all cases

- [ ] Wrong accounting
- Missing effect (eg. after withdraw no balance[user] -= wad)
- Missing critical condition (eg. no require(balance[user] <= wad))
- Contract implement one effect but not the other (eg. can deposit but can't withdraw)
- Contract does not allow refunds / withdraws
- Contract can't be replenished (no payable functions)
- First user accounting is not properly done

- [ ] Wrong code
- "=" instead of "=="
