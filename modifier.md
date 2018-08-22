# Modifier

### 1. Definition
  - Modifier is a function used for smart contract function call
  - If developer write modifier with its own modifying logic inside it, it works like bool-returning functions
  - On function call, by writing modifier in front of the function makes modifier works as function call filter
  - Modifier is most common and easy way for smart contract exception filering and security enhancing

### 2. Example
  - Using keyword <code>modifier</code>, we can define modifier on solidity.
  - We can define it on this way :
<pre><code>modifier foo(bar) {
  if (bar != something) throw; 
  _;

}</code></pre>
  - Or more common and better way :
<pre><code>modifier foo(bar) {
  require(bar != something); 
  _;

}</code></pre>
  - Mostly, developers use second way.

### 3. Why we use this?
  - To make function call requirements clear
  - Make requirement check part clean and easy to refactor