## Chapter Three - Day One 🧠

<ol>
 <li><b>In words, list 3 reasons why structs are different from resources.
</b>
   <blockquote>Three reasons structs are different than resources are that structs can be created whenever you want, they aren't as secure as resources, and they can be copied and overwritten.</blockquote>
     
<li><b>Describe a situation where a resource might be better to use than a struct.</b>
       <blockquote>A resource would be better utlitized when handling sensitive or important data that one never wants to replace or lose: for example, when handling NFTs. For example, if snomobeels wants to transfer me one of those ugly BAYC that are worth a bazillion dollars, using a struct would ensure that piece of data didn't happen to go missing because of some sort of error in coding.</blockquote>
     <li><b>What is the keyword to make a new resource?</b>
       <blockquote>Create</blockquote>
          <li><b>Can a resource be created in a script or transaction (assuming there isn't a public function to create one)?</b>
       <blockquote>Nope!</blockquote>
                  <li><b>What is the type of the resource below?</b>
       <blockquote>String</blockquote>
     <li><b>Let's play the "I Spy" game from when we were kids. I Spy 4 things wrong with this code. Please fix them.</b>
       
  ```Cadence 
 
       pub contract Test {

    // Hint: There's nothing wrong here ;)
    pub resource Jacob {
        pub let rocks: Bool
        init() {
            self.rocks = true
        }
    }

       pub fun createJacob(): Jacob { //We need to use @Jacob here since it is a resource
        let myJacob = Jacob() // You must use <- instead of = since it is a resource, and you have to specify create
        return myJacob //You must either move or delete the resource here
    }
}
```

The corrections will look as follows:
                                                 
```Cadence

   pub contract Test {

    pub resource Jacob {
        pub let rocks: Bool
        init() {
            self.rocks = true
        }
    }

       pub fun createJacob(): @Jacob { 
        let myJacob <- create Jacob() 
        destroy myJacob 
    }
}
       ```
