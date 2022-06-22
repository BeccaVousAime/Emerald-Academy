 ## Chapter Three - Day Three 🤯

<ol>
 <li><b>Define your own contract that stores a dictionary of resources. Add a function to get a reference to one of the resources in the dictionary.
</b>
   
   ```cadence
   pub contract Lasagna {

    pub var dictionaryOfFood: @{String: Food}

    pub resource Food {
        pub let breakfast: String
        pub let lunch: String
        pub let dinner: String
        init() {
            self.breakfast = "BagelnCreamCheese"
            self.lunch = "ChickenSammie"
            self.dinner = "HummusChickenSalad"
        }
    }

    pub fun getFoodReference(key: String): &Food? {
        return &self.dictionaryOfFood[key] as &Food?
        }



    init() {
        self.dictionaryOfFood <- {}

    }

}
                                 
```
 <li><b>Create a script that reads information from that resource using the reference from the function you defined in part 1.
</b>
   
```cadence
