# BaseV4Quoter
[Git Source](https://github.com/uniswap/v4-periphery/blob/ea2bf2e1ba6863bb809fc2ff791744f308c4a26d/src/base/BaseV4Quoter.sol) - Generated with [forge doc](https://book.getfoundry.sh/reference/forge/forge-doc)

**Inherits:**
[SafeCallback](contracts/v4/reference/periphery/base/SafeCallback.md)


## Functions
### constructor


```solidity
constructor(IPoolManager _poolManager) SafeCallback(_poolManager);
```

### selfOnly

*Only this address may call this function. Used to mimic internal functions, using an
external call to catch and parse revert reasons*


```solidity
modifier selfOnly();
```

### _unlockCallback


```solidity
function _unlockCallback(bytes calldata data) internal override returns (bytes memory);
```

### _swap

if amountSpecified < 0, the swap is exactInput, otherwise exactOutput

*Execute a swap and return the balance delta*


```solidity
function _swap(PoolKey memory poolKey, bool zeroForOne, int256 amountSpecified, bytes calldata hookData)
    internal
    returns (BalanceDelta swapDelta);
```

## Errors
### NotEnoughLiquidity

```solidity
error NotEnoughLiquidity(PoolId poolId);
```

### NotSelf

```solidity
error NotSelf();
```

### UnexpectedCallSuccess

```solidity
error UnexpectedCallSuccess();
```

