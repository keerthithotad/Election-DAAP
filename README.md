# Election-DAAP
ELECTION - DAPP PROJECT:-

1)SMOKE TEST:-

Install dependencies :

  1.NPM : https://nodejs.org
  2.Truffle: https://github.com/trufflesuite/truffle
  3.Ganache: http://truffleframework.com/ganache/
  4.Metamask: https://metamask.io/
  5.Sublime text3 : www.sublimetext.com

  Step 1:-make project folder as follows

      $mkdir election
      $cd election

  Step 2:-Unbox pet-shop truffle package.

        truffle unbox pet-shop
  Step 3:- Make a file election.sol[election contract]

      $touch Election.sol

      pragma solidity ^0.4.17;
    /**
    * The contractName contract does this and that...
    */
    contract Election {
    // Store candidate
    // Read Candidate
    string public candidate; //state variable
    //constructor
    constructor () public {
    candidate = "candidate 1";
    } 
    }
  Step 4:- 
			Create 2_deploy_contracts.js under migrations folder
     var Election = artifacts.require("./Election.sol");
     module.exports = function(deployer) {
     deployer.deploy(Election);
    };
    
   Migrate the contract using Truffle
   within the Terminal at election folder run the below code.
     $truffle migrate

     truffle console
    truffle(development)> Election.deployed().then(function(instance) {app = instance })
    undefined
    truffle(development)> app.address
    'xxxxxxxxxxxxxxxxxxxxx.......' (your address)
2) List Candidates
   Step 5:-Change the contract code (Download the code).
   Open Election.sol in sublime text and edit the code.
   open Ganache and check the change in Balance.
     truffle migrate --reset
    console
    Election.deployed().then(function(i){app =i; })
    app.candidates(1)
    app.candidates(2)
    app.candidates(1).then(function(c) {candidate =c; })
    candidate
  fetch candidate
  step 6:- web3
    This will help us pull the voter details . Web.eth.getAccounts should give you the list of accounts / addressses connected to the blockchain. In our case, this is the list of accounts within the Ganache (local blockchain)

Step 7:Testing -
	we create the election.js file under test folder.
	(download the code.)
	test the code using.
       truffle test
3) FRONT END CODE - HTML & JAVASCRIPT:-
Step 8 :- we design front end page using html & javascripts 
   1.index.html is the front end file.
   2.app.js is the javascript file.
   where we completely replace the previous pet-shop code by our designed interactive web page.
Step 9 :- Terminal -Migrate the contract.
          connect to custom RPC-http://localhost:7545/ — you can see your port number from the Ganache block chain
          
     truffle migrate --reset
     npm run dev

Step 10:-   Create account in Metamask and connect it.

3)Cast vote:-
 Step 11:- vote
			Test for the voting function

4) Watching events:-
  Step 6:- Run the Front End Application
       $ npm run dev Visit this URL in your browser: http://localhost:3006.
