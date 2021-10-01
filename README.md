# Guess the card game | Powered by Ethereum Blockchain 

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

```
@dev/Editor: Pavan Ananth Sharma.
Contributors: Oliver Shmikele, Siddarth Raj, Austin Rudolph.
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

>Introduction

This game is based on the popular guess the card memory exercise game using food cards, this is based on the ERC-20 & ERC-721 standards which are the very standards used for transferring tokens or value from one address to another.
In this game whenever you pic a card a special loop is created and when you pick another card there the loop ends but as soon as you pic 2 similar cards in the same loop (example: burger card and burger card) you win and the burger card gets added into your scorecard and removed from the user grid then a certain amount of MemoryTokens(ERC-20) will be added into your wallet as the reward.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

>Advantages

This game can help in increasing memory power and also rewards the users, so this concept is a win-win for the user and also promotes a particular cryptocurrency.
The gas fee will be cost only when the correct pair is found out and when about to redeem it to your wallet.
There will be constant updates if the game releases which will never make it boring to the users.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

>Dependencies 

* Node js
* Truffle should be installed, if not code : ``` npm install truffle -g --force```
* Ganache local blockchain should be installed, if not link: https://www.trufflesuite.com/ganache
* Knowledge about OpenZiplin.
* Ganache should be connected to metamask.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

> Interfaces / standards used is ERC:

ERC is an acronym that stands for Ethereum Request for Comments. ERCs are application-level standards for Ethereum and can include token standards, name registries, library/package formats, and more. Anyone can create an ERC, but it is the author’s responsibility to clearly explain their standard and foster support for it within the community.Common ERC standards define a required set of functions for a token type, allowing applications and smart contracts to interact with them in a predictable way.

* Here are a few stadards we are and will be using in future:
```
ERC-20:(This is the standard API used for fungible tokens, including transfer and balance tracking functionalities.)
ERC-223:(This standard protects users from accidental contract transfers.)
ERC-721:(This is the most popular non-fungible token (NFT) standard. While fungible tokens can be divided, non-fungible tokens can not. NFTs can be owned and transacted by individuals as well as consigned to third-parties. NFTs can represent ownership over digital or physical assets.)
ERC-777:(Like ERC20, ERC777 is a standard for fungible tokens, and is focused around allowing more complex interactions when trading tokens. More generally, it brings tokens and Ether closer together by providing the equivalent of a msg. value field, but for tokens.)
ERC-1155:(This set of interfaces and contracts are all related to the ERC1155 Multi Token Standard.The EIP consists of three interfaces which fulfill different roles, found here as IERC1155, IERC1155MetadataURI and IERC1155Receiver.
ERC1155 implements the mandatory IERC1155 interface, as well as the optional extension IERC1155MetadataURI, by relying on the substitution mechanism to use the same URI for all token types, dramatically reducing gas costs.)
ERC-2981:(A standardized way to retrieve royalty payment information for non-fungible tokens (NFTs) to enable universal support for royalty payments across all NFT marketplaces and ecosystem participants.)
```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Output (example images):

* Interface:

<img width="753" alt="BlockcahinGame_Image1" src="https://user-images.githubusercontent.com/86551444/135518309-cd2b7083-4b98-47a5-9aac-94c473a987bc.PNG">

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

* When the perfect match is found:

<img width="753" alt="BlockcahinGame_Image2" src="https://user-images.githubusercontent.com/86551444/135518717-7d8dd5db-e68c-4401-8ec6-615a09952cd8.PNG">

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

* Another example of perfect match and paying the fees:

<img width="753" alt="BlockcahinGame_Image5" src="https://user-images.githubusercontent.com/86551444/135518945-589cafee-8d2a-4904-9da6-2f4a280efa84.PNG">

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

* When the user pics a wrong pair / incorrect match:

<img width="753" alt="BlockcahinGame_Image4" src="https://user-images.githubusercontent.com/86551444/135519183-a1badd9a-a6a5-4d24-9b23-8a3f1ff7fa4e.PNG">

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Plans under implementation / progresss:

* We can make this an NFT hunting game, where players and users can compete and hunt for NFT's and then level them up by either buying a Mind-Magic-Elixir token (MMET) a new token for upgrading NFT minted by the user or by constantly winning the NFT hunt.
As the number of people increases the grid size also should increase by the following formula:
```
Formula by: Pavan Ananth Sharma
```

<img width="337" alt="FormulaForGameGridSizeBYPavanAnanthSharma" src="https://user-images.githubusercontent.com/86551444/135525005-3766ce10-6cad-4124-9467-63cc879075a8.PNG">

Where

*  GsZ = Grid Size represented as martix, also can be called as the difficulty. (Example: level 3 = 3X3 or level 13 = 13X13)
*  Nu = Number of users / players who have or are playing.
*  Cst = Cost of tokens
*  Ta = MemoryToken.
*  Tb = Mind-Magic-Elixir token(MMET).
*  Nn = Number of NFT's(ERC-721) collected or minted so far.

```
Note: If the size of the grid is throwing a float data type it should be converted to an integer value then the matrix should be constructed by the code. 

Example: if GsZ = 13.3333443 = 13 ; build [13X13] ;

Example 2: if GsZ = 14.98 = 14 ; build [14X14] ;
```

We also can increase or decrease the reward on basis of GsZ which depends on the above factors as well using this formula:
```
Formula by: Pavan Ananth Sharma
```

<img width="377" alt="BlockcahinGameTokenFormulaByPavanAanthSharma" src="https://user-images.githubusercontent.com/86551444/135581946-48d00181-612c-47e8-8719-7027ab287720.PNG">

This means the cost of Ta & Tb or the MemoryToken and  Mind-Magic-Elixir token function is directly proportional to GsZ or the size/difficulty level of the game; i.e. when the GsZ goes up or the level of difficulty increases even the price of Ta & Tb( MemoryToken & Mind-Magic-Elixir) also increases by the current price's thousandth power or 1 in thousand parts.

Example:

Let's suppose: 

Current level = 3

GsZ = 3X3

Price of Ta = 1000.00$

Price of Tb = 2000.00$


Now let's say:

New upgraded level = 4

GsZ = 4X4

Price of Ta = 1001.00$

Price of Tb = 2001.00$

* And once in 500 times when the game restarts and starts running on new block the matrix will become (m ≠ n)% which means the number of rows ≠ number of column, and every 500th time on the new block m = m + 1 and the next 500th time n = n + 1. (Please note this lasts untill the 500th block is mined which means the chances are low and rewards are high)

* Example:
* 1st 500th block : m = m + 1 & m ≠ n which can give us [14X13] matrix.

* 2nd 500th block : n = n + 1 & m ≠ n which can give us [13X14] matrix.


* Which follows the formula and dynamically increases and decreases the difficulty which means if the difficulty decreases the price of tokens decreases and if the difficulty increases the price of tokens also increases, which makes the competition & reward healthy & super fun to play.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

>Conclusion:

If you enjoyed this code and this amazing sesion make sure you follow me here on GitHub and also my Instagram for more amazong content.

Thankyou!!

```
0x2006f8eB8936943B70B4f4377EceCE2096EebF55
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------














