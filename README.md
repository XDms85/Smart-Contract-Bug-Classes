# Smart Contracts Bug Classes
Not definitive - in progress

- [ ] Unchecked inputs
- No checks on inputs
- No ranges of values
- [ ] Unchecked return values
- Transfer return value
- [ ] Reentrancy
- [ ] Frontrunning
- Operation can be replied by another user
- [ ] Access control
- Function is critical but it's public/external instead of private/internal
- Function can't be reached (eg. onlyOwner but contract has no owner)
- [ ] Function abuse
- [ ] Function denial (DOS)
- Function can cause reentrancy
- Function can interact with an user smart contract
- [ ] Wrong math
- Division before multiplication
- Division by zero / Denominator can be zero
- [ ] Wrong conditional logic
- Condition is missing / is wrong / is reversed
- Condition can't be reached (eg. return before require or if)
- Condition is always true or false
- Condition denies some cases
- [ ] Wrong accounting
- Missing effect (eg. after withdraw no balance[user] -= wad)
- Missing critical condition (eg. no require(balance[user] <= wad))
