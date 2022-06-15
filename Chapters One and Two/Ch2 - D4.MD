## Chapter Two - Day Four

<ol>
 <li><b>Deploy a new contract that has a Struct of your choosing inside of it (must be different than Profile). Create a dictionary or array that contains the Struct you defined.Create a function to add to that array/dictionary.
</b>
   
```cadence
//Part One: Here is where I deploy my contract
pub contract Quest {
    //Part Two: Here is my dictionary
    pub var socials: {Address: Profile}
    
    //Part One: Here is where I define my struct 
    pub struct Profile {
        pub let twitter: String
        pub let instagram: String
        pub let discord: String
        pub let account: Address

        
        init(_twitter: String, _instagram: String, _discord: String, _account: Address) {
            self.twitter = _twitter
            self.instagram = _instagram
            self.discord = _discord
            self.account = _account
        }
    }
    //Part Three: Here is where I create my fuction to add to the dictionary
    pub fun addProfile(twitter: String, instagram: String, discord: String, account: Address) {
        let newProfile = Profile(_twitter: twitter, _instagram: instagram, _discord: discord, _account: account)
        self.socials[account] = newProfile
    }

    init() {
        self.socials = {}
    }
}
   ```
<li><b>Add a transaction to call that function.</b>
        
```Cadence 
        
        import Quest from 0x01

transaction(twitter: String, instagram: String, discord: String, account: Address) {

    prepare(signer: AuthAccount) {}

    execute {
        Quest.addProfile(twitter: twitter, instagram: instagram, discord: discord, account:account)
        log("Socials Logged.")
    }
}
```
<li><b>Add a script to read the Struct:</b>

```Cadence 
import Quest from 0x01

pub fun main(account: Address): Quest.Profile {
  return Quest.socials[account]!
  }
 ```
