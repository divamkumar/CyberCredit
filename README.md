## Features

This app includes two features:

#### 1. Connect Wallet

The app allows the current user to connect their wallet.

#### 2. Display Credit Score

The app displays the current user's credit score.

## Credit Score Calculation

The Credit Score of the user is calculated using a complex algorithm that utilizes on-chain data.  
The **first** part of the score is derived from the financial assets of the wallet (how long they've held certain tokens (ERC-20 & ERC-721), # of POAPs, etc.)  
The **second** part of the score is derived from their social activity on the CyberConnect platform (followers/following count)  

The intricacies of how the social credit calculations are made can be outlined below:  
Activity and Age Calculation: 

 - Start off with 50 points, you cannot go above 50 points 
 - Activity: Each transaction gets you 1 point 

| Age (Hours)   | Multiplier    |  
|:-------------:|:-------------:|  
| < 730         | 0.005         |  
| 730 - 2920    | 0.01          |  
| 2920 - 5840   | 0.02          |  
| 5840 - 8760  | 0.03          |  
| 8760 - 11680 | 0.04          |  
| 11680 - 14599 | 0.05          |  
| > 14600    | 0.06          |  


### Assets Calculation:
Assets is calculated through a multiplier system. The highest points achivable in the assets category is 40 points. Multipliers level is achived through the level of assets owned by the user. *For example, if they own 0.05 ETH in their wallet, they would get 0.005 points*  
Refer to the table below:

| Assets Value   | Multiplier    |  
|:-------------:|:-------------:|  
| 0 - 0.1 ETH   | 0.10          |  
| 0.1 - 0.5 ETH | 0.20          |  
| 0.5 - 1 ETH   | 0.30          |  
| 1 - 5 ETH     | 0.40          |  
| 5 - 10 ETH    | 0.50          |  
| 10 - 50 ETH   | 0.60          |  
| 50 - 100 ETH  | 0.70          |  
| 100 - 500 ETH | 0.80          |  
| 500 - 1000 ETH| 0.90          |   
| > 1000 ETH    | 1.00          |


### Social Reputation Calculation: 
Social Reputation is calculated through a multiplier system. The highest point achivable in the scoial reputation category is 10 points. Social Reputation level is achieved through the amount of followers owned by the user. Extra points are earned for the social network linked to the account
Refer to the table below:

| Followers     | Multiplier    |  
| ------------- |:-------------:|  
| 10,000        | 0.50          |  
| 5,000         | 0.40          |  
| 2,500         | 0.30          |  
| 1,000         | 0.25          |  
| 500           | 0.20          |  
| 200           | 0.15          |  
| 100           | 0.10          |  
| 10            | 0.5           |  
| < 10          | 0             |   


After calculating the raw score, add 5 points if they have their Twitter linked.
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


Final score out of **100**:
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
