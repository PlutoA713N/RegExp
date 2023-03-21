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

d. Replace all occurrences of 5 with five for the given string.

 let ip = 'They ate 5 apples and 5 oranges'
 const regex = new RegExp("5", "g");
 console.log( ip.replace(regex, "five") );
 // They ate five apples and five oranges

// e) Replace all occurrences of note irrespective of case with X.

 let ip = 'This note should not be NoTeD'
 
 const regex = new RegExp("note", "ig");
 
 console.log( ip.replace( regex, "X"))
 // This X should not be XD


