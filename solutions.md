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

// f) For the given multiline input string, filter all lines NOT containing the string 2.

let purchases = `items qty
apple 24
mango 50
guava 42
onion 31
water 10`

const regex = new RegExp("^","m")
const numRegex = new RegExp("2")

console.log(
    purchases.split(regex) 
    .map(line => line.trim())
    .filter(string => !numRegex.test(string) )
    .join('\n')
    )
    
items qty
mango 50
onion 31
water 10

// g) For the given array, filter all elements that contains either a or w.

let items = ['goal', 'new', 'user', 'sit', 'eat', 'dinner'];

const regex = new RegExp("(a|w)")

console.log( items.filter((string) => {
          return regex.test(string)
       }) 
       
)
[ 'goal', 'new', 'eat' ]

// h) For the given array, filter all elements that both e && n.

let items = ['goal', 'new', 'user', 'sit', 'eat', 'dinner'];



console.log( items.filter((string) => {
          return ( /e/.test(string) && /n/.test(string)  )
       }) 
)

[ 'new', 'dinner' ]


// i) For the given string, replace 0xA0 with 0x7F and 0xC0 with 0x1F.

 let ip = 'start address: 0xA0, func1 address: 0xC0'
 
 const pattern1 = new RegExp("0xA0")
 const pattern2 = new RegExp("0xC0")
 
 ip = ip.replace(pattern1, "0x7F")
 ip = ip.replace(pattern2, "0x1F")
 console.log(ip)

start address: 0x7F, func1 address: 0x1F

// a) Check if the given input strings contain is or the as whole words.

let str1 = 'is; (this)'
let str2 = "The food isn't good"
let str3 = 'the2 cats'
let str4 = 'switch on the light'

const regex = new RegExp("(\\bis\\b|\\bthe\\b)")

const array = [str1,str2,str3,str4]
    array.forEach((string) => {
        console.log( regex.test(string) )
    }) // T F F T
 

    



