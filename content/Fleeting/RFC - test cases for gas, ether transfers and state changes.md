Hey w1nt3r,

First of all, thank you for the open sourcing this repo. The tests (and hints) have been very useful to me while building and testing [Tiviem](https://github.com/yashkarthik/tiviem) (Typescript EVM). I very recently passed all the test cases in this repo. However, I noticed that there are no test cases for testing gas, ether transfers, and state changes.

I am planning to write some tests to cover the above cases but I wanted to know if you have any plans / specifics about how to implement them.

My `evm()` function returns a `Result` object, as of now only `success`, `stack`, `logs` and `returndata` are tested against the expected values.

```ts
type Result = {
  success: boolean,
  stack: bigint[],
  memory: Uint8Array,
  gas: number,
  returndata: Uint8Array,
  logs: Log[],
  state: Map<bigint, AccountState>, // address -> AccountState
}

type AccountState = {
  balance: bigint,
  code?: {
	  asm?: string,
    bin: Uint8Array
  },
  storage?: Map<bigint, bigint>,
  nonce: bigint
}
```

My plan I to compare test gas and state in a similar manner.

I just wanted to put this out there to thank you for open sourcing this repo and wanted some insight into if/how you plan on implementing the remaining tests.