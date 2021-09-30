# CS351- Project 5: Distributed Auction

## Jiajun Guo, Rajesh Upadhayaya, Steven Chen


### Program Functionality

#### Initialization
- Transfer all jar files along with data.db into a directory (ie. "project5")
- Initialize programs in following order:

##### Start Bank Server
- Log into any basement machine (ie. ssh username@b146-30.cs.unm.edu)
- Command: ifconfig to record ip address (ie. 64.106.21.159)
- Change directory into "project5"
- Command: java –cp . –jar BankServer.jar 9001
- -cp: Class path is set to the current working directory

##### Start Data Server
- Log into any basement machine (ie. ssh username@b146-31.cs.unm.edu)
- Command: ifconfig to record ip address (ie. 64.106.21.160)
- Change directory into "project5"
- Command: java –cp . –jar DataServer.jar 9002
- cp: Class path is set to the current working directory

##### Start Auction Server
- Log into any basement machine (ie. ssh username@b146-32.cs.unm.edu)
- Command: ifconfig to record ip address (ie. 64.106.21.161)
- Change directory into "project5"
- Command: java -cp . –jar House.jar **9003 64.106.21.159 9001 64.106.21.160 9002 12**
- cp: Class path is set to the current working directory
- **HousePort BankServer-IP BankServer-Port DataServer-IP DataServer-Port numItems**
- Repeat for multiple Auction Houses, increasing port number by 1 each time

##### Start Agent Client
- Log into any basement machine (ie. ssh username@b146-32.cs.unm.edu)
- Change directory into "project5"
- Command: java –cp . –jar agent.jar **64.106.21.159 9001** 
- cp: Class path is set to the current working directory
- **BankServer-IP BankServer-Port**


#### Commands

##### Before Contacting Auction House
- B : Get balance from the Bank
  - Returns current user balance
  - Displays funds held 
  - Make payment after item purchase
- A : Contact Auction House
  - Will display list of all auction houses
  - Displays Auction House command list
- X : Exit
  - Exit program


##### After Contacting Auction House
- B : Bid
  - Bid on an item 
  - Asks user for which house
  - Asks user for item number
  - Asks user for bid amount
- R : Request list of items
  - Asks user for which house
  - Displays list of items and their item number
- X : Go back





