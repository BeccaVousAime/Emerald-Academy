## Chapter Two - Day Three

<ol>
 <li><b>In a script, initialize an array (that has length == 3) of your favourite people, represented as Strings, and log it.</b>
   
```cadence
pub fun main() {

var myFavoritePeople: [String] = 
["C3PFLO", "WildTurkey", "MrsWildTurkey"]
log(myFavoritePeople)

}
   ```
<li><b>In a script, initialize a dictionary that maps the Strings Facebook, Instagram, Twitter, YouTube, 
  Reddit, and LinkedIn to a UInt64 that represents the order in which you use them from most to least. For example, YouTube --> 1, Reddit --> 2, etc.
  If you've never used one before, map it to 0!</b>
  
  ```cadence
pub fun main() {

var socials: {String: UInt64} = 
  {"Facebook":2, "Instagram": 6, "Twitter": 4, "Youtube": 3, "Reddit": 5, "LinkedIn": 1}
log(socials)

}
  ```
  
  <li><b>Explain what the force unwrap operator ! does, with an example different from the one I showed you (you can just change the type).</b>
    <blockquote>
  When you access values in a dictionary, it returns the value as an optional. This means that the value is either the type specified or nil. With the force unwrap operator, one can 'unwrap' the optional and display the actual value. This is useful if you know the value is definitely not nil; however, if you make an error and the value <i>is</i> nil, the program will crash.  
<br>     </br>
For the example above, if we use 'return' as shown below, its shows an error of "mismatched types. Expected UInt64, got UInt64?"  <br>     </br> 
       
```Cadence
pub fun main(): UInt64 {

var socials: {String: UInt64} = 
{"Facebook":2, "Instagram": 6, "Twitter": 4, "Youtube": 3, "Reddit": 5, "LinkedIn": 1}
return(socials["Instagram"])

}
   ```     

To fix this, we use the force unwrap and the script will execute:
  
   ```Cadence
   pub fun main(): UInt64 {

var socials: {String: UInt64} = 
{"Facebook":2, "Instagram": 6, "Twitter": 4, "Youtube": 3, "Reddit": 5, "LinkedIn": 1}
return(socials["Instagram"])!

}
   ```
   </blockquote>
   Now, the script will return the appropriate value of "6".
   <br>     </br> 
   <li><b>Using this picture below, explain...</b>

What the error message means, why we're getting this error, and how to fix it?
 <blockquote>As above, the error means that the type is an optional. We're getting this error, because String is used instead of String?. We fix this by unwrapping the type, as in the above example. 
 </blockquote>
 
 ```Cadence 
 pub fun main(): String {
let thing: {Address: String} = {0x01: "One", 0x02: "Two", 0x03: "Three"}
return(thing[0x03])!
}```
