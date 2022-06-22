 ## Chapter Three - Day Two 🧠

<ol>
 <li><b>Write your own smart contract that contains two state variables: an array of resources, and a dictionary of resources. Add functions to remove and add to each of them. They must be different from the examples above.
</b>

```cadence
   
   pub contract Lasagna {

    pub var dictionaryOfFood: @{String: Food}
    pub var arrayofFoods: @[Food]

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

    pub fun addFoodDict(today: @Food) {
        let key = today.breakfast
        self.dictionaryOfFood[key] <-! today
    }

    pub fun removeFoodDict(key: String): @Food {
        let food <- self.dictionaryOfFood.remove(key: key)!
        return <- food
}
    pub fun addFoodArray(food: @Food) {
     self.arrayofFoods.append(<- food)
}


    pub fun removeFoodArray(index: Int): @Food {
        return <-self.arrayofFoods.remove(at: 1)
}


    init() {
        self.dictionaryOfFood <- {}
        self.arrayofFoods <- []
    }

}
```
