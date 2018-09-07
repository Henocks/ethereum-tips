# Smart Contract Connection

### 1. Smart Contracts
  - On small-sized solidity / blockchain project, developers usually write solidity code in a single contract.
  - But in case of bigger projects, developers sometimes have to divide contracts for code visibility enhancement or token security.
  - So developers have to connect multiple contracts.

### 2. Example
  - For example, I wrote test source for explanation.
<pre><code>contract a {
    function alpha(uint8 alp) {
        // blah ...
    }
}

contract b {
    function beta(uint8 bet) {
        // blah ...
    }
}
</code></pre>
  - To connect these contracts, target contract(contract to call) must be arleady published to blockchain network.
  - After target contract creation, we can use contract address for contract instance genetration.
<pre><code>// acontract at 0x0000000000000000000000000000000000001234

contract acontract {
    function alpha(uint8 alp) {
        // blah ...
    }
}

contract bcontract {
    function beta(uint8 bet) {
        // Contract instance(interface) creation
        acontract aInstance = acontract(0x000...0001234);
        
        // Other contract function call
        aInstance.alpha(bet);
    }
}
</code></pre>
  - Just like this.
  - Be careful for GAS spending.
  - Connecting contracts like proxy makes development easy.