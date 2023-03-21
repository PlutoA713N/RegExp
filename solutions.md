a. const regex = new RegExp("two", "i");

* console.log(
regex.test(s1),
regex.test(s2),
regex.test(s3)
) 
// true, false, true;

b. console.log( 
    items.filter((string) => {
    const regex = new RegExp("e");
    return !regex.test(string);
    }) 
) // [ 'goal', 'sit' ]

c. Replace first occurrence of 5 with five for the given string.

let ip = 'They ate 5 apples and 5 oranges'

const regex = new RegExp(5);
 
console.log( ip.replace(regex, "five") ) // They ate five apples and 5 oranges
