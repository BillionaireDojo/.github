# Billionaire Dojo NFT    

The biggest clash of the century. 🐲💥 The battle royal of humanity's cream. ⚔️ The Billionaire Dojo opens its gates... ⛩️🥷🏿   
<div align="center">
<img 
  src="https://raw.githubusercontent.com/BillionaireDojo/.github/main/assets/billionairedojo.jpg" 
  style="width:50%; height:50%;"
/>
</div>

## ⛩️ What is the Billionaire Dojo? ⛩️  
Now that Elon Musk and Mark Zuckerberg wanted to fight each other in a cage match, we can take it pretty much for granted that we all live in a strange computer simulation.   
   
But hey, what's stopping us from making the simulation timeline even more weird? What if not just Elon and Zuck, but other famous tech CEOs would also fight each other? Now we can all make this our own reality. Welcome to the Billionaire Dojo, fighter!   
   
Billionaire Dojo is a blockchain-based game where tech billionaires can be minted as NFTs and entered into matches against each other.   

Our goal is to create a fun game that makes people laugh and takes their minds off all the bullshit that's happening in the world right now at least for a little while. We live on <b>the Lukso blockchain</b>, the perfect ecosystem for fun-loving projects tapping into the cultural zeitgeist of our time. 

## 🐲 Game mechanics 🐲   
Each billionaire represents a team (i.e. Team Elon, Team Zuck, etc.), and the game's goal is to take the balance of other teams and make your team more wealthy. Other teams can also be ousted from the game if all their players' balance goes down to zero. In the end, there can be only one.

### 📈 The Stats
When you mint your billionaire, it will get 5 stats and a balance. All stats range between 1 and 100.    

💸 <b>Balance</b>: All new players start with 1000 balance. You put some amount of the player's balance on the line each time you fight another player.    
💰 <b>Wealth</b>: How wealthy your player is. These are billionaires, so expect this to be high for most players.    
💪 <b>Strength</b>: This value is totally random and can be anywhere in the range.    
🥵 <b>Stamina</b>: This value is totally random and can be anywhere in the range.    
😏 <b>Charisma</b>: This value is totally random and can be anywhere in the range.    
🤗 <b>Empathy</b>: Well... don't expect your player's empathy to be sky-high. So if you happen to mint a player with high empathy hold on to it!     

### The Octagon   
This is where the fighting takes place. The outcome of a fight depends on the sum total of a player's stats, the higher the better, plus a degree of randomness that varies from level to level.

The first thing players do here is select the level they want to play on. The Octagon has 3 levels:    
😈 <b>Maniac</b>: For hardcore players. On each round, you risk a 500 balance, and the degree of randomness is high, so players with lower stats can come out victorious.     
🫡 <b>Normal</b>: On each round, players risk 300 balance. There is a medium degree of randomness.    
👼 <b>Baby</b>: Easy-peasy. Best for first-timers. You risk 150 balance and randomness is low.    

<b>💭 Should I stay or should I go?</b>     
You can decide to leave your player in The Octagon for <i>n</i> number of rounds, or just pick a random match, fight it out, and go. If you leave your player in The Octagon, it will fight any random player, until the number of rounds has passed, or its balance hits zero. If you pick a random fight you will know the result instantaneously. 

🤕😴 <b>Recovery zone</b>:
A common trait in all billionaires is that they can come back from setbacks stronger, so don't worry if your player's balance hits zero, they're still useful. Just put them in the recovery zone, wait some time, and their balance will rise again. Keep in mind though, that you can't come back forever, your balance will be a little less each time you recover...    

🔥 <b> Will it all end up in flames...? </b> 🔥    
Once all the players from a given team have hit 0 balance, that team is gone for good. The game ends when there is only one team with a balance above zero.    

## 🥷🏿 For shadowy super coders... 🥷🏿    
Our smart contracts are written in Solidity and deployed on the Lukso blockchain. There are 3 main contracts:    
#### 1. BillionaireDojo.sol:    
- `LSP8IdentifiableDigitalAsset` standard
- This contract is responsible for minting the Billionaire Dojo NFTs, assigning random stats to each NFT, storing balances, and maintaining metadata.
- We make use of unique `LSP8` features such as rich metadata with `_setData()`:
    - We set the creator info so we are attributed on-chain for our work.
    - We set the stats of each NFT here. With other NFT standards, this would've been more difficult. The LSP standards make this operation feel idiomatic.
 
#### 2. FightLogic.sol:     
- Responsible for one thing: deciding the winner in a given fight
- Has one method: `function fight(uint256 player1, uint256 player2) public view returns (uint256 winner)`
- If the community comes up with a more interesting fight logic, this contract can be swapped with a new one any time

#### 3. Octagon.sol:    
- Players use this contract to enter and leave The Octagon, pick fights, and enter and leave the recovery zone
- Contains most of the game logic
- Responsible for announcing the game-winner
- Once the game ends, the octagon contract can be replaced with a new one in `BillionaireDojo.sol`, and a new game can begin. The show can go on forever... 🔥
## 🚀 Roadmap 🚀    
- [ ] Win the 10K prize in the [Lukso BuildUP #2 Hackathon](https://app.buidlbox.io/lukso/build-up-2) for Culture & Entertainment
- [ ] Spend part of the prize money to build our community on socials - our [X (formerly Twitter)](https://twitter.com/BillionaireDojo) already has 1.2K followers
- [ ] Make sure our contracts are robust
- [ ] Launch on <b>Lukso Mainnet</b> and be the biggest, most popular NFT project there
- [ ] Continue to be an integral part of the Lukso community, drive adoption and usage of the Lukso ecosystem
- [ ] Continue improving our game and making it even more FUN
