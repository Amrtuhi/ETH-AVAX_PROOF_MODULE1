# Project Title
Error Handling and its methods

This is the Module 1 assesment of Eth+AVAX proof course . This is a solidity program for implementing the error handling concept and its method which consist of require() revert() and assert() methods  .

## Description

This is a program which is created in solidity for using the concept of errror handling and implementing its methods which uses the basic concept of solidity like working in remix ethereum and writing a code in .sol file which contains the intermediate knowledge like error handlng and its methods . This program show the use of error handling method and also its implementation.

## Getting Started


### Executing program

To run this program , i am using Remix , an Solidity IDE.
->To start go to Remix IDE and start coding 
->add a solidity file i named it as incentive.sol
->include the licence (SPDX) 
->use the latest solidity compiler by including the pragma which will compiler the code using that solidity compiler
->make a contract named incentivereceived 
->under that contract create a function named incentivecal which take two parameters of unsigned interger (uint256) type _basesalary and _salaryreceived.
->write require method with some condition  which ensures that _basesalary should always be equal to 5000. if not then an error message will revert. 
->write revert method with some condition which ensures that _incentive should always be greayer tha salary . if it is not than error messsage will revert.
->write assert methhod which will only consist only one statement which ensure _salaryreceived should be greater than or equal to _basesalary , if not then transaction is revert.
->click on compile (compilemultiplication.sol)
->go to deploy and deploy it.

code blocks for commands
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Incentivereceived {
   
    function incentivecal(uint256 _basesalary, uint256 _salaryreceived) external pure returns (uint256) {

        // require statement
        require(_basesalary == 5000 , "Salary shoould always be 5000");

        // assert statement
        assert(_salaryreceived >= _basesalary);

        // calculating incentive
        uint256 _incentive = _salaryreceived - _basesalary;
       

        // revert statement
        if (_incentive < 5000) {
             

            revert(" Incentive received but less than salary");
        }

        return _incentive;
    }
}

## Help

Change the compiler solidity version if error occur , then change by going to compiler solidity menu present on left side of the compiler and change the compiler version.

## Authors

->Amrita Kumari
->https://www.linkedin.com/in/amrita-kumari-753319232/

## License

This project is licensed under the MIT License - see the licence file for details.
