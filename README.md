# Becca's Quest Submissions 🥂

## Chapter One
##### Chapter One - Day One
First off, thank you so much to Jacob and the rest of the team! I know zero to nothing, and what I do know is likely terribly outdated. I look forward to learning a bit, and hopefully this old lady can figure some of it out. ;)
<ol>
 <li><b>Explain what the Blockchain is in your own words.</b>
   <blockquote>
    <p>To me, the blockchain is a big mess that I hardly understand. From what I've been reading, the blockchain is a decentralized database where anyone can store information publicly and securely. This information is stored in structured 'blocks', which when closed, are linked together in a 'chain' of data.</p>
   </blockquote>
  
 <li><b>Explain what a Smart Contract is.</b>
   <blockquote>
    <p>A smart contract is a program with set specificiations that a developer creates, which is then deployed on the blockchain. It can be interacted with by any user, and is considered efficiant, transparent, and secure. The transaction will only take place if all the conditions of the smart contract are met, and are processed automatically without a middle-man.</p>
   </blockquote>
   
   <li><b>Explain the difference between a script and a transaction.</b>
  <blockquote>
    <p>A transaction changes the data stored on the blockchain, while a script simply allows the user to view the data. There is always a cost to execute a transaction; whereas, there is no cost associated for <i>viewing</i> the information via script.</p> One benefit of Flow over more popular blockchains (<i>cough cough Ethereum</i>) is lower transaction costs for users. 
   </blockquote>
    

  </li>
</ol>

##### Chapter One - Day Two
<ol>
  <li><b>What are the 5 Cadence Programming Language Pillars?</b>
    <blockquote>
    <p>Safety and Security, clarity, approachability, developer experience, and resource oriented programming</p>
  </blockquote>
    <li><b>In your opinion, even without knowing anything about the Blockchain or coding, why could the 5 Pillars be useful</b>
      <blockquote>If the smart contracts we deploy using Candence are clear and understandle, it not only allows for a higher degree of trust and transparency for users, but also provides an elevated experience for developers when it comes to writing and debugging their code. 
        </blockquote>
          </li>
        </ol>
   
   
## Chapter Two   
##### Chapter Two - Day One

<ol>
 <li><b>Deploy a contract to account 0x03 called "JacobTucker". Inside that contract, declare a constant variable named is, and make it have type String. Initialize it to "the best" when your contract gets deployed.</b>
<blockquote> 
<img src = https://github.com/BeccaVousAime/qu-est-submit-/blob/09553780203b2a89f1f8bc29526dca7184f08f9a/Screenshots/Ch2Day1.1.png width="600" height ="600">
 </blockquote>
 
<li><b>Check that your variable is actually equals "the best" by executing a script to read that variable. Include a screenshot of the output.</b>
 <blockquote> 
  <img src = https://github.com/BeccaVousAime/qu-est-submit-/blob/09553780203b2a89f1f8bc29526dca7184f08f9a/Screenshots/Ch2Day1.2.png width="600" height ="600">
  </blockquote?>
 </li>
  </ol>
  
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
 <blockquote><b>Before and after changing my number**</b></blockquote>
  <img src="https://github.com/BeccaVousAime/qu-est-submit-/blob/307ee45fc9fb5088de1b961210a7aef1ac7d70bc/Screenshots/Ch2Day2%20Script.png">
  <img src="Screenshots/Ch2Day2 Script2.png">

