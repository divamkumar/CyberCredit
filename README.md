## Features

This app includes two features:

#### 1. Connect Wallet

The app allows the current user to connect their wallet.

#### 2. Display Credit Score

The app displays the current user's credit score.

## Credit Score Calculation

The Credit Score of the user is calculated using a complex algorithm that utilizes on-chain data.  
The **first** part of the score is derived from the financial assets of the wallet (how long they've held certain coins, # of POAPs, etc.)  
The **second** part of the score is derived from their social activity on the CyberConnect platform (followers/following count)  

The intricacies of how the social credit calculations are made can be outlined below:
Activity and Age Calculation: 

 - Start off with 50 points, you cannot go above 50 points 
 - Activity: Each transaction gets you 1 points 
 - Transactions within less than a month(730 hours) : no multiplier 
 - Transactions within 1 - 4 months (730.1-2920 hours): 0.1 multiplier  
 - Transactions within 4 - 8 months (2920-5840 hours): 0.2 multiplier 
 - Transactions within 12 - 16 months (8760.01-11680 hours): 0.3 multiplier
 - Transactions within 16 - 20 months(11680.1-14599 hours): 0.4 multiplier  
 - Transactions within 20 - 24 months(14600-17520 hours): 0.5 multiplier


### Assets Calculation:
Assets is calculated through a multiplier system. The highest points achivable in the assets category is 40 points. Multipliers level is achived through the level of assets owned by the user. *For example, if they have 0.05 eth, they would get 0.005 points*
Refer to the table below:

 - 0 - 0.1 ETH = 0.1x multiplier 
 - 0.1 - 0.5 ETH = 0.2x multiplier 
 - 0.5 - 1 ETH: 0.3 x multiplier 
 - 1 ETH - 5 ETH: 0.40 multiplier 
 - 5 ETH - 10 ETH: 0.5 multiplier 
 - 10ETH - 50 ETH: 0.6 multiplier 
 - 50 ETH - 100 ETH: 0.7 multiplier 
 - 100 ETH - 500 ETH: 0.80 multiplier 
 - 500 ETH - 1000 ETH: 0.90 multiplier 
 - 1000 ETH + : 1 x multiplier 


### Social Reputation Calculation: 
Social Reputation is calculated through a multiplier system. The highest point achivable in the scoial reputation category is 10 points. Social Reputation level is achieved through the ammount of flollowers owned by the user. Extra points are erned for the social netweork linked to the account
Refer to the table below:

 - Start off with 10 points, you cannot go above 10 points 
 -  10,000 Followers: 0.50 x multiplier 
 -  5,000 Followers: 0.40 x multiplier 
 -  2,500 Followers: 0.30 x multiplier 
 -  1,000 Followers: 0.25 x multiplier 
 - 500 Followers: 0.20 x multiplier
 - 200 Followers: 0.15 x multiplier 
 -  100 Followers: 0.10 x multiplier 
 - 10 Followers: 0.5 x multiplier 
 - 10 Followers: 0 x multiplier 

After calculating the raw score, add 5 points if they have their twitter linked.
| Level         | Points        |  
| ------------- |:-------------:|  
| 1             | 0 - 10 points |  
| 2             | 10 - 20 points|  
| 3             | 20 - 30 points|  
| 4             | 30 - 40 points|  
| 5             | 40 - 50 points|  
| 6             | 50 - 60 points|  
| 7             | 60 - 70 points|  
| 8             | 70 - 80 points|  
| 9             | 80 - 90 points|  
| 10            | 90 - 100 points|  

Activity (Age + Transactions): 50%

Assets: 40%

Social Rep: 10%

Limit: 100 points of all categories above
 - 50 points to Activity
 - 40 points to Assets
 - 10 points to Social Rep

## Getting Started

Install the dependencies:

```bash
npm install
# or
yarn
```

After installing the dependencies, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

## Learn More

To learn more about CyberConnect, take a look at the following resources:

- [CyberConnect Web Site](https://cyberconnect.me/) - introduction to CyberConnect,
- [CyberConnect Developers Documentation](https://docs.cyberconnect.me/) - dig deeper into CyberConnect API.
