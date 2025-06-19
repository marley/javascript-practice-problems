# Object Practice (including some object arrays)

## 1.

```
let fridge = {
    eggs: 10,
    milk: 1,
    soyMilk: 1,
    hummus: 0,
    chicken: 2,
    yogurt: 1
};
console.log(fridge["eggs"]);
```

**How would you explain this code to someone else? Use your own words.**

<details>
<summary>solution</summary>
<br>
  In line 1, we create an object called fridge. The key seem to represent food in the fridge and the values represent how much of each thing is there. In the last line we print out the value for "eggs". Refresher on accessing object properties with bracket notation and dot notation <a href="https://www.w3schools.com/js/js_object_property.asp">here</a>.
</details>

**What is the number printed out in last line of code?**

<details>
<summary>solution</summary>
<br>
  The value for fridge["eggs"] is `10`. (You could also do `fridge.eggs`).
</details>

**What is the syntax for adding a new key-value pair to an object?**

<details>
<summary>solution</summary>
<br>
  You can use bracket or dot notation to add a new property. For example:

```
fridge["cucumber"] = 12;
fridge.lemon = 2;
```

If you were to write this code and then console log the object again, you would see 2 new key-value pairs added.

</details>

## 2.

```
    let cafe = {
      chaiLatte: "4.50",
      greenTea: "3.00",
      espresso: "3.00",
    };
   cafe["cappuccino"] = "4.00";
   cafe["chaiLatte"] = "4.60";
   delete cafe.greenTea;
```

**What is the final value of `cafe`?**

<details>
<summary>solution and hint</summary>
<br>
  In line 1 we create an objecy called `cafe` with 3 items. The items represent menu items and their associated prices.
  In the next line, we add a new menu item called `"cappuccino"`. Then we assign a new price to `"chaiLatte"`.
  In the last line, we use the `delete` operator to remove the key-value pair `"greenTea"` and `"3.00"`.
  So ultimately, our object looks like this:

```
  {
    chaiLatte: "4.60",
    espresso: "3.00",
    cappuccino: "4.00"
  }
```

</details>

## 3.

```
let students = [
    {name: "katie", age: 5},
    {name: "abina", age: 7},
    {name: "cole", age: 8},
    {name: "eva", age: 6}
];
let absent = students[3];
console.log(absent["name"]);
```

**How data type is `students`? Is it an object or an array?**

<details>
<summary>solution</summary>
<br>
  `students` is an array. We know this because of the square brackets. Arrays can contain any kind of datatype. In this case it is an array of objects.
</details>

**What is the value of `absent`?**

<details>
<summary>solution</summary>
<br>
    Just like any array, we can get each item using the index. `absent` has been defined as the value of the item at index 3. The item at index 3 is `{name: "eva", age: 6}`.
</details>

**What is the value of `absent["name"]`?**

<details>
<summary>solution</summary>
<br>
    The item at index 3 is `{name: "eva", age: 6}`. It is an object with two key-value pairs. This code `absent["name"]` is using bracket notation to get the value from the key "name". Thus, the value of `absent["name"]` is equivalent to `"eva"`.
</details>

## 4.

```
   let forSaleObj = [
    mirror: "5.00";
    bedframe: "20.00";
    lamp: "6.00";
    blender: "15.00";
    microwave: "40.00";
   ];
   forSale["microwave"] = "35.00";
   console.log(forSale[3]);
```

**What is wrong with this code?**

<details>
<summary>solution</summary>
<br>
  In the line 1, we see incorrect object declaration with parentheses `[]` instead of square brackets `{}`.
  Each item in the object should be separated by commas `,` instead of semi-colons `;`.
  The last line would not work because it is trying to reference an index (which only works for arrays).
</details>

**What changes can you make to fix it?**

<details>
<summary>solution</summary>
<br>
Add curly brackets, replace the semi-colons with commas and use a key instead of number index.

```
    let forSaleObj = {
        mirror: "5.00",
        bedframe: "20.00",
        lamp: "6.00",
        blender: "15.00",
        microwave: "40.00",
    };
    forSale["microwave"] = "35.00";
    console.log(forSale["lamp"]);
```

</details>

## 5.

**a) You are writing an app for a school. The app contains information about all students. Create an object called `studentData` which contains all the following information about a student: name, age, schoolYear, allergies (true or false).**

<details>
<summary> example solution</summary>
<br>

```
let studentData = {
    name: "Abbi",
    age: 6,
    schoolYear: 1,
    allergies: false
};
```

</details>

**b) In a new line, create a variable that is equal to the age of the student.**

<details>
<summary>example solution</summary>
<br>

```
let studentData = {
    name: "Abbi",
    age: 6,
    schoolYear: 1,
    allergies: false
};
let studentAge = studentData["age"];
```

</details>

**c) In a new line, set the `studentData` name to `"Abi"`. (hint, check the last Example on the w3schools Objects documentation).**

<details>
<summary>example solution</summary>
<br>

```
let studentData = {
    name: "Abbi",
    age: 6,
    schoolYear: 1,
    allergies: false
};
let studentAge = studentData["age"];
studentData["name"] = "Abi";
```

</details>
