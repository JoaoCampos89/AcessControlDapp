# AcessControlDapp [WIP]


This app intends to store a profile of images of persons which can be identified by computer vision in blockchain as a smart contract, then is possible for everyone send allow requests to devices. These devices are connected to locks and they open  when the person in the contract is allowed to enter in the lock. All entrances are registered in the blockchain to assure an inviolate environment.

The workflow is shown next:

The person creates a profile and identification using acessControlToken (ac). These token stores all the data necessary to identify the person.

The owner of the lock sends a transaction where allow predetermined persons to enter.

When person is identified the lock is open

The structure of the token

pragma solidity ^0.4.16;

contract acessControl{
    struct owner{
      address person;
    }

    struct allowedPerson {
        uint fingerprint; // fingerprint data
        address person; // person address
        uint imageFingerprint;   // image dataset
    }
    
    mapping(address => allowedPerson) public allowedPersons;
}








