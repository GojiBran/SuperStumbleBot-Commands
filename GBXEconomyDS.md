The code you've provided outlines a complex economy system with multiple currencies, user interactions, and commands. Let's break down the mathematical and economic principles behind this system:

### 1. **Currencies and Resources**
   - **GojiBux (GBX)**: The primary currency in the economy. Users can earn, spend, and store GBX.
   - **Weed (grams)**: A secondary resource that users can grow, buy, sell, and stash.
   - **Spaghetti (SPG)**: A fun, secondary currency that users can collect and trade.
   - **Pizza (PZA)**: Another fun, secondary currency that users can collect and trade.
   - **Joints**: A derivative of weed, which users can roll and smoke.

### 2. **Economic Principles**
   - **Supply and Demand**: The price of weed is dynamically adjusted based on the global supply (`wghBank`) and demand. The more weed in the global stash (`wghBank`), the lower the price, and vice versa.
   - **Taxation**: Transactions like selling weed are taxed (5% in this case), which reduces the amount of GBX users receive from selling weed.
   - **Inflation Control**: The total supply of GBX is capped at 1,000,000 GBX (`maxGbxSupply`), preventing infinite inflation. Similarly, the total supply of weed is capped at 50,000 grams (`maxWeedSupply`).
   - **Randomness and Risk**: Many commands involve randomness, such as earning a random amount of GBX or losing a random amount when gambling. This introduces risk and unpredictability into the economy.

### 3. **Key Commands and Their Math**
   - **`.gojibux`**: Users earn a random amount of GBX between 5 and 250 GBX. The amount is deducted from the global LGH Bank (`lghBank`), ensuring that the total GBX in circulation doesn't exceed the cap.
     ```javascript
     const actualIncrease = Math.floor(Math.random() * (250 - 5 + 1)) + 5;
     lghBank -= actualIncrease;
     userBalances[username].balance += actualIncrease;
     ```

   - **`.grow`**: Users can grow a random amount of weed between 0 and 1792 grams. The amount is added to their personal stash.
     ```javascript
     const grownGrams = Math.floor(Math.random() * 1793);
     userWeedStashes[username] = (userWeedStashes[username] || 0) + grownGrams;
     ```

   - **`.buyweed` and `.sellweed`**: Users can buy and sell weed at dynamically adjusted prices. The buy price includes a 2% tax, and the sell price includes a 5% tax.
     ```javascript
     const cost = Math.ceil(amount * weedBuyPrice * 1.02); // 2% tax
     const earnings = applyTax(amount * weedSellPrice, 0.05); // 5% tax
     ```

   - **`.gamble`**: Users can gamble a specified amount of GBX. The outcome is random, with a 5% chance of a jackpot (5x payout), a 30% chance of doubling the bet, a 30% chance of losing half, and a 35% chance of losing everything.
     ```javascript
     const roll = Math.random();
     if (roll < 0.05) { // 5% chance - JACKPOT (5x payout)
         winnings = betAmount * 5;
     } else if (roll < 0.35) { // 30% chance - Double the money (2x payout)
         winnings = betAmount * 2;
     } else if (roll < 0.65) { // 30% chance - Lose half (Half goes to LGH Bank)
         winnings = -Math.floor(betAmount / 2);
     } else { // 35% chance - Lose everything (Full amount goes to LGH Bank)
         winnings = -betAmount;
     }
     ```

   - **`.bankrob`**: Users can attempt to rob the LGH Bank. The success rate is dynamically calculated based on the user's balance relative to the bank's total GBX. If successful, they steal a percentage of the bank's GBX. If they fail, they lose a significant portion of their GBX and all their weed.
     ```javascript
     let successChance = Math.max(0.05, Math.min(0.95, (1 - (userBalance / lghBank)) * 0.75);
     let success = Math.random() < successChance;
     ```

### 4. **Global Limits and Constraints**
   - **LGH Bank (`lghBank`)**: The total amount of GBX in the economy is controlled by the LGH Bank. Users can earn GBX from the bank, but the bank's supply is limited.
   - **WGH Bank (`wghBank`)**: The total amount of weed in the economy is controlled by the WGH Bank. Users can grow, buy, and sell weed, but the bank's supply is limited.
   - **Cooldowns**: Many commands have cooldowns to prevent users from spamming them. For example, the `.gojibux` command has a 1-minute cooldown.

### 5. **User Balances and Stashes**
   - **User Balances**: Each user has a balance of GBX, which can be increased or decreased through various commands.
   - **Stashes**: Users can stash GBX, weed, spaghetti, and pizza. Stashed items are protected from certain commands like `.snarfbux` (which randomly deducts GBX from users).

### 6. **Leaderboards and Rankings**
   - **`.topbux`**: Shows the top 10 users with the most GBX.
   - **`.topweed`**: Shows the top 10 users with the most weed.
   - **`.topspaget`**: Shows the top 10 users with the most spaghetti.
   - **`.toppizza`**: Shows the top 10 users with the most pizza.

### 7. **Dynamic Pricing**
   - The price of weed is dynamically adjusted based on the global supply (`wghBank`). The more weed in the global stash, the lower the price, and vice versa.
   ```javascript
   const weedRatio = wghBank / maxWeedSupply; // % of total weed available
   weedBuyPrice = Math.max(5, Math.floor(10 * (1 + (0.5 - weedRatio)))); // Base ±50%
   weedSellPrice = Math.max(4, Math.floor(8 * (1 + (0.5 - weedRatio)));
   ```

### 8. **Random Events**
   - **Police Bust**: When users buy weed, there's a 5-10% chance they will get busted by the police and lose a portion of their weed.
   - **4:20 Auto-Weed Giveaway**: Every hour at 4:20, all users receive 420 grams of weed.

### 9. **Stocks and Investments**
   - Users can buy and sell stocks (e.g., WEED, DANK, GOJI) at dynamically changing prices. The stock prices fluctuate randomly every minute.
   ```javascript
   let change = Math.floor(Math.random() * 21) - 10; // Random +/- 10 GBX
   stocks[stock].price = Math.max(1, stocks[stock].price + change); // Ensure price never goes below 1
   ```

### 10. **Extraction and Processing**
   - Users can extract hash from weed, which requires a certain amount of weed and GBX. The extraction process is governed by specific rates.
   ```javascript
   const extractRates = {
       "hash": { weedPerGram: 10, gbxPerWeed: 1 }
   };
   ```

### Conclusion
This economy system is a blend of resource management, risk-taking, and dynamic pricing. It uses randomness to create unpredictability, while also implementing caps and constraints to prevent inflation and maintain balance. The system encourages user interaction through commands that allow earning, spending, and trading resources, while also introducing elements of risk and reward through gambling and theft mechanics.
