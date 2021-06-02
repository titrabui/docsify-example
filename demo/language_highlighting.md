# Language Highlighting
### 1. Command
Type: \```bash ... ```
```bash
NODE_ENV=development PROCESS_TYPE=web docker-compose up
```

### 2. Javascript
Type: \```javascript ... ```

```javascript
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
}
```

### 3. Solidity
Type: \```solidity ... ```

```solidity
pragma solidity >=0.4.25 <0.7.0;

contract MetaCoin {
	mapping (address => uint) balances;

	event Transfer(address indexed _from, address indexed _to, uint256 _value);

	constructor() public {
		balances[tx.origin] = 10000;
	}

	function sendCoin(address receiver, uint amount) public returns(bool sufficient) {
		if (balances[msg.sender] < amount) return false;
		balances[msg.sender] -= amount;
		balances[receiver] += amount;
		emit Transfer(msg.sender, receiver, amount);
		return true;
	}
}

```

### 3. Python
Type: \```python ... ```

```python
class Dog:

    kingdom = "Animalia"

    def __init__(self, name, age):
        self.name = name
        self.age = age
```