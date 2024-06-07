
# The code
  
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;
contract ErrorHandling {
   uint256 public value;    
    function setValue(uint256 _value) public {
        require(_value > 100, "Value must be greater than 100.");
        value = _value;
    }

    function doubleValue() public {
        uint256 oldValue = value;
        value = value * 2;
        assert(value == oldValue * 2);
    }
    
    function resetValue() public {
        if (value == 100) {
            revert("Value is already 100.");
        }
        value = 0;
    }
}

        return _num;
    }
}
```

