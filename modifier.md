# Modifier

### 1. Definition
  - Modifier is a function used for smart contract function call
  - If developer write modifier with its own modifying logic inside it, it works like bool-returning functions
  - On function call, by writing modifier in front of the function makes modifier works as function call filter
  - Modifier is most common and easy way for smart contract exception filering and security enhancing

### 2. Example
Using keyword <code>modifier</code>, we can define modifier on solidity.
We can define it on this way :
<pre><code>modifier foo(bar) {
  if (bar != something) throw; 
  if (bar == something2) revert();
  _;
}</code></pre>
Or more common and better way :
<pre><code>modifier foo(bar) {
  require(bar != something); 
  _;
}</code></pre>
Mostly, developers use the second way.
<pre><code>modifier foo(bar) {
  require(bar != something, "error message!"); 
  _;
}</code></pre>
For better event tracking & debugging!

To call(use) modifier, simply add modifier like this :
<pre><code>function baz(bar) 
foo(bar) // here!
{
  return bar + 1;
}</code></pre>

### 3. Why we use this?
  - To make function call requirements clear
  - Make requirement check part clean and easy to refactor
  - Additionally, processing <code>revert()</code> inside of modifier makes code more oriented.

### 4. Use Cases
  - One of the most common case is **Overflow Checking**. In most of secure, asset-related contracts use overflow-checking modifiers to prevent these problems.
<pre><code>modifier overFlowChecker(uint256 a, uint256 b, uint256 c) {
  if((a - b) != c) revert("overflow!");
  _;
}

function addValue(uint256 num1, uint256 num2)
overFlowChecker((num1+num2), num1, num2) //checks overflow
{
  return (num1 + num2);
}</code></pre>