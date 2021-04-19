# Unit 20 - "Solidity Homework"

![contract](Images/smart-contract.png)

## AssociateProfitSplitter.com

The AssociateProfitSplitter contract splits the profit equally amongst the 3 employees specified at deployment.

* At deployment we initialize the contract by specifying the 3 address that we denote as the 3 employees. We use the constructor to initialize this and to prevent from typing addresses directly in the code.
* The deposit() method takes the amount we specified and splits it equally amongst the 3 employees. Whatever is left is send back to the account. 

* We call the deposit() function from withing the function() external payable to ensure that the logic in deposit() executes if the Ether is sent directly to the contract, since we dont have a withdraw() function in this case.

The screenshots of executing the AssociateProfitSplitterContract are as follows.
![Screenshot1](/Images/AssociateProfitSplitter/AssociateProfitSplitterCompiled.png)
![Screenshot2](/Images/AssociateProfitSplitter/GanacheAccountsUsedForContract.jpg)
![Screenshot3](/Images/AssociateProfitSplitter/EmployeeAccountsInitializedBeforeDeploying.jpg)
![Screenshot4](/Images/AssociateProfitSplitter/MetaMaskConfirmationDuringDeploymentAssoicateProfitSplitter.jpg)
![Screenshot5](/Images/AssociateProfitSplitter/AssociateProfitSplitterContractDeployedSuccessfully.jpg)
![Screenshot6](/Images/AssociateProfitSplitter/AssoicateProfitSplitter-9ETH.jpg)
![Screenshot7](/Images/AssociateProfitSplitter/AssoicateProfitSplitter-4ETH.jpg)
![Screenshot8](/Images/AssociateProfitSplitter/GanacheAccountsUpdatedAfterAssociateProfitSplitterContractExecutedDepositMethod-4ETH.jpg)

##  AssociateProfitSplitter.com

The tiered contract splits the profits based on the level with the CEO getting 60% of profits, CTO getting 25% and Bob getting 15%
* At deployment we initialize the contract by specifying the 3 address that we denote as the 3 employees. We use the constructor to initialize this and to prevent from typing addresses directly in the code.

* The deposit() method takes the amount and diviedes it by 100 to make it easy to split amongst 3 employees
* THe CEO gets 60% and we calculate it by multiplying units by 60.
* We send this to the CEO.
* We then set total to the amount ( the variable total is used to maintain a running sum, in case there is some left over after sending to all 3)
* We repeat the same steps for the CTO and Bob. the CTO gets 25% and Bob gets 15%.
* If there is anything left over we send that amount ( msg.value-total) to employee_one (CEO)

The screenshots of executing the TieredProfitSplitterContract are as follows
![Screenshot1](/Images/TieredProfitSplitter/GanacheAccountsBeforeExecutingTieredContract.png)
![Screenshot2](/Images/TieredProfitSplitter/TieredContractConstructorInitializationwith3EmployeeAddresses.png)
![Screenshot3](/Images/TieredProfitSplitter/TieredContractDeployedSuccessfully.png)
![Screenshot4](/Images/TieredProfitSplitter/TieredContractDepositing10ETH.png)
![Screenshot5](/Images/TieredProfitSplitter/GanacheAccountsAfterSplitting10ETH.png)

