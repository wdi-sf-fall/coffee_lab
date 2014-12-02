# CoffeeScript Exercises

For this lab we would like you to complete the following exercises in CoffeeScript. You can do this in a Rails app or in a seperate coffee file.

### reverse()

Define a function `reverse()` that reverses a string. For example, `reverse("building")` should return the string `"gnidliub"`.

```
reverse = (word) ->
  characters = word.split("")
  newString = []
  newString.push(characters.pop()) for taco in characters
  newString.join("")
  # word.split("").reverse().join("")

console.log reverse "building"
```

### filterLongWords()

Write a function `filterLongWords()` that takes an array of words and an integer `i` and returns an array of words that are longer than `i`.

```
filterLongWords = (words, count) ->
  result = []
  (result.push word if word.length > count) for word in words

  # for element in words
  #   # if element.length > count
  #   #   result.push element

  # for element in words
  #   result.push element if element.length > count

  result

console.log filterLongWords ["Elie", "Tim", "Markus"], 4
```

### range()

Write a function `range` that takes one argument, a positive number, and returns an array containing all numbers from 0 up to and including the given number.

```
range = (num)-> if num >0 then [0..num] else "NO!"
```

### startsWith

Write a function called `startsWith` that takes two arguments, both strings. It returns `true` when the first argument starts with the characters in the second argument, and `false` otherwise.

```
startsWith = (firstWord, secondWord) ->
  firstWord[0...secondWord.length] == secondWord

console.log startsWith "caterpillar", "cat"
```

### grade()

Write a function named `assignGrade` that:

* takes 1 argument, a number score.
* returns a grade for the score, either "A", "B", "C", "D", or "F".

Call that function for a few different scores and log the result to make sure it works.

```
grade = (value) ->

  console.log value
  switch
    when value >= 90 then console.log  "A"
    when value < 89 and value > 80 then console.log "B"
    when value < 79 and value > 70 then console.log "C"
    when value < 69 and value > 60 then console.log "C"
    else console.log "F"

grade 68.9
```

### pluralizer()

Write a function named `pluralize` that:

* takes 2 arguments, a noun and a number.
* returns the number and pluralized form, like "5 cats" or "1 dog".

Call that function for a few different scores and log the result to make sure it works.

```
pluralize = (thing, count) ->
  result = "#{count} #{thing}"
  result += "s" if count >= 2 || count == 0
  result

console.log pluralize "cat", 5
console.log pluralize "dog", 1
console.log pluralize "dog", 0
```

### tempConvert()

Store a celsius temperature into a variable. Convert it to fahrenheit and output "NN°C is NN°F".

```
tempConvert = (degree) ->
  converted = (degree * 1.8) + 32
  "#{degree}°C is #{converted}°F"

console.log tempConvert 30
console.log tempConvert 0
console.log tempConvert 100
```