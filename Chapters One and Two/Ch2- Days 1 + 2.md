  ##### Chapter Two - Day Two
<ol>
 <li><b>Explain why we wouldn't call changeGreeting in a script.</b>
  <blockquote>A script is used to view data on the blockchain, and cannot be used to modify. ChangeGreeting is a command which will modify the contract, so one must utilize it within a transaction. </blockquote>
 <li><b>What does the AuthAccount mean in the prepare phase of the transaction?</b>
  <blockquote>The AuthAccount allows access to the data in an account so I user can sign a transaction. 
   </blockquote>
    <li><b>What is the difference between the prepare phase and the execute phase in the transaction?</b>
     <blockquote>The prepare phase is used to access the data in an account. The execute phase is used to call functions to change data on the blockchain.
     </blockquote>
 <li><b>This is the hardest quest so far, so if it takes you some time, do not worry! I can help you in the Discord if you have questions.</b>
  <br>
  <blockquote><b>Part One</b></blockquote>
  
  ```cadence
pub contract HelloWorld {

    pub var greeting: String
    pub var myNumber: Int


    init() {
        self.greeting = "Hello, World!"
        self.myNumber= 0

    }

    pub fun changeGreeting(greeting: String) {
        self.greeting = greeting
    }

    pub fun updateMyNumber(newNumber: Int) {
        self.myNumber = newNumber

    


    }
}
```
  <br>
  <blockquote><b>Part Two</b></blockquote>
  
  ```cadence
import HelloWorld from 0x01

pub fun main(): Int {
return HelloWorld.myNumber

}
```
<br>
  <blockquote><b>Part Three</b></blockquote>
  
  ```cadence
import HelloWorld from 0x01

transaction(myNewNumber: Int) {

prepare(acct: AuthAccount) {}

execute {
HelloWorld.updateMyNumber(newNumber: myNewNumber)

}
}
```
 
 </li>
 </ol>
 <blockquote><b>Before and after changing my number</b></blockquote>
  <img src="https://github.com/BeccaVousAime/qu-est-submit-/blob/307ee45fc9fb5088de1b961210a7aef1ac7d70bc/Screenshots/Ch2Day2%20Script.png">
    <img src="https://github.com/BeccaVousAime/qu-est-submit-/blob/307ee45fc9fb5088de1b961210a7aef1ac7d70bc/Screenshots/Ch2Day2%20Script.png">
