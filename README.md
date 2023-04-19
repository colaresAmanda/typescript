
# Typescript Exercises
This is a list of exercises that I made to become familiar with the TypeScript syntax.

Since I already had knowledge of JavaScript and learned OOP with C#, I asked ChatGPT to give me a quick explanation so that I could become accustomed to TypeScript syntax more quickly. 


## 1# Some two numbers
```typescript
// Write a function that takes in two numbers and returns their sum. Add type annotations to the function's parameters and return value.

function addTwoNumbers(num1: number, num2: number){
    return num1 + num2
}

console.log(addTwoNumbers(25, 30))
console.log(addTwoNumbers(0.755, .203))
```

## #2 Create a Book 
```ts
/* Write an interface for a book with the following properties:
        title (string)
        author (string)
        pages (number)
*/

// Describes a book object
interface Book {
  title: string // The title of the book
  author: string // The name of the book's author
  pages: number // The number of pages in the book
}

// Create a book object that implements the Book interface
const book: Book = {
  title: "Sharp Objects",
  author: "Gillian Flynn",
  pages: 256,
}

// Log the book object to the console
console.log(book)

```

### 3# Write a class called Animal

```ts
/*Write a class called Animal that has the following properties:
name (string)
species (string)
age (number)

Add a method called makeSound that logs a message to the console.*/

interface AnimalInterface {
  name: string
  species: string
  age: number
  makeSound(): void
}

class Animal implements AnimalInterface {
  constructor(
    public name: string,
    public species: string,
    public age: number
  ) {}

  makeSound(): void {
    console.log("Sound sound sound")
  }
}

let animal: AnimalInterface = new Animal("Boots", "Felis catus", 2)
console.log(animal)
animal.makeSound()
```

### 4#  Calculate Area


```ts
/* Write a function called calculateArea that 
takes in the width and height of a rectangle and returns its area. 
Use a type alias to define the shape of the function's input and output. */

function calculateArea(width: number, height: number): number {
    if (width < 0 || height < 0) {
        throw new Error("Invalid arguments: width and height must be positive numbers.");
    }
    return width * height;
}

console.log(calculateArea(10, 20))
console.log(calculateArea(30, 40))

```




### 5# Capitalize the first letter of each word



```ts
/*
 * Write a function called capitalizeString that
 * takes in a string and capitalizes the first letter of each word.
 * Use the split and map array methods to split the string into words and
 * capitalize the first letter of each word.
 * Use the join method to join the capitalized words back into a string.
 */


function capitalizeString(str: string): string {
  let words = str.split(" ")

  const capitalizedWords = words.map((word) => {
    const [firstLetter, ...restOfWord] = word
    return `${firstLetter.toUpperCase()}${restOfWord.join("")}`
  })

  return capitalizedWords.join(" ")
}

console.log(capitalizeString("hello world!"))

```
