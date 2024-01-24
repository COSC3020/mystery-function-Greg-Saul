[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

This function finds the biggest number in the array by checking if there is only one element (that would be the max) and returns it.
If the array has more than one element it recursively calls mystery with the whole array minus the first element and sets that equal to foo.
This process happens as many times as there are elements in the array until foo only has one element and then it keeps comparing foo or a[0] for the rest of the calls.
Once the recursion is done, you will be left with the returned value being the maximum value in the array.

