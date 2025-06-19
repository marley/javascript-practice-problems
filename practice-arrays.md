# Array Practice

## 1.

```
let fibonacci = [1, 1, 2, 3, 5, 8, 13];
console.log(fibonacci[2]);
```

**How would you explain this code to someone else? Use your own words.**

<details>
<summary>solution</summary>
<br>
  In line 1, we create an array of numbers called fibonacci. In line 2 we print out the item at index 2.
</details>

**What is the number printed out in the second line of code?**

<details>
<summary>solution</summary>
<br>
  The item at index 2 happens to also be `2`.
</details>

**What is the syntax for adding a new item to the end of the array?**

<details>
<summary>solution</summary>
<br>
 `fibonacci.push(newNumber);` where `newNumber` is a number.
  You can read about `.push()` and other the Array methods on <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">MDN</a>.
</details>

## 2.

```
let sisters = ["paula", "tina", "mara"];
let brothers = ["juan", "edgar"];
let siblings = sisters.concat(brothers);
let eldest = siblings[3];
```

**What is the value of `siblings`?**

<details>
<summary>solution</summary>
<br>
  In line 3, we use the `Array.concat()` method to combine the two arrays. Thus, the value of siblings is `["paula", "tina", "mara", "juan", "edgar"]`. You can read about `.concat()` and other the Array methods on <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">MDN</a>.
</details>

**What is the value of `eldest`?**

<details>
<summary>solution</summary>
<br>
  In line 4 we create a variable called `eldest` which is equal to the item in `siblings` at index 3, i.e. `"mara"`.
</details>

## 3.

```
   let shoppingList = ["eggs", "milk", "bread", "tomato sauce", "garlic"];
   shoppingList[1] = "soy milk";
```

**What is happening in line 2? What is the new value of `shoppingList`?**

<details>
<summary>solution and hint</summary>
<br>
  In line 2 we set a new value at index 1 of `shoppingList`. Thus `shoppingList` now looks like this: `["eggs", "soy milk", "bread", "tomato sauce", "garlic"]`.
</details>

**How can we remove the last two items from the array? In otherwords, we want to modify shoppingList to be `["eggs", "milk", "bread"]`.**

<details>
<summary>hint</summary>
<br>
  HINT: There are several ways to do this. From a google search of "remove last two items of array js", the first results are <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop">Array.pop()</a> and <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice">Array.splice()</a>. Try searching these before you look at final solution.
</details>

<details>
<summary>solution</summary>
<br>
  Using `Array.pop()`: .pop() removes the last item of an array, so you could have to repeat `shoppingList.pop();` twice.

Using `Array.splice()`: .splice() has several options for syntax. Here we can use two parameters which represent starting index and delete count like so: shoppingList.splice(startIndex, deleteCount). Since we want to delete the last 2 items, we have to start at index 2 and delete 2 items: `shoppingList.splice(2, 2);`

</details>

## 4.

```
   let todoArray = ("walk the dog", "cook lunch", "make the bed", "vacuum");
   todoArray.push("water plants");
   console.log(todoArray[6]);
```

**What is wrong with this code?**

<details>
<summary>solution</summary>
<br>
  In the line 1, we see incorrect array declaration with parentheses `()` instead of square brackets `[]`.
  The last line returns an error because we are trying to print an item at index 6. But the highest index is 5, so this is undefined.
</details>

**What changes can you make to fix it?**

<details>
<summary>solution</summary>
<br>
Add square brackets and use an index that is within the range of this array.

```
let todoArray = ["walk the dog", "cook lunch", "make the bed", "vacuum"];
todoArray.push("water plants");
console.log(todoArray[5]);
```

</details>

## 5.

**a) Create an array of strings called `familyArr`. Every item is a name of a family member. The array should have length 6. The family member at index 2 should have the same name as the family member at index 5.**

<details>
<summary>example solution</summary>
<br>

```
let familyArr = ["Gina", "Farah", "Ari", "Stephen", "Ari", "Ralph"];
```

</details>

**b) Create a variable called `daughter` and set it equal to one of the `familyArr` items.**

<details>
<summary>example solution</summary>
<br>

```
let familyArr = ["Gina", "Farah", "Ari", "Stephen", "Ari", "Ralph"];
let daughter = familyArr[0];
```

</details>

**c) Create a variable that is equal to `familyArr` index 3. You can name this variable whatever you like.**

<details>
<summary>example solution</summary>
<br>

```
let familyArr = ["Gina", "Farah", "Ari", "Stephen", "Ari", "Ralph"];
let daughter = familyArr[0];
let grandfather = familyArr[3];
```

</details>
