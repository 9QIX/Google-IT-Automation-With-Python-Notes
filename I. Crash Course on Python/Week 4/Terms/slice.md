You can also access a portion of a string, called a [[slice]] or a substring. This allows you to access multiple characters of a string. You can do this by creating a range, using a colon as a separator between the start and end of the range, like [2:5].

This range is similar to the range() function we saw previously. It includes the first number, but goes to one less than the last number. For example:

```
>>> fruit = "Mangosteen" >>> fruit[1:4] 'ang'
```

The slice _includes_ the character at index 1, and _excludes_ the character at index 4. You can also easily reference a substring at the start or end of the string by only specifying one end of the range. For example, only giving the end of the range:

```
>>> fruit[:5] 'Mango'
```

This gave us the characters from the start of the string through index 4, _excluding_ index 5. On the other hand this example gives is the characters _including_ index 5, through the end of the string:

```
>>> fruit[5:] 'steen'
```

You might have noticed that if you put both of those results together, you get the original string back!

```
>>> fruit[:5] + fruit[5:] 'Mangosteen'
```
