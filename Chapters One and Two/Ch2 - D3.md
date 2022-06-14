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
      The force unwrap operator ! 
