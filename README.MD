# Solidity fundamental #

in this prject we're using basic solidity features like datatypes, visibility, Default Initializations, Comments, Functions, Scope, View & Pure Functions

1. datatypes
    
    * bool: The possible values are constants true and false.

    * uint unsignNumberVariable (uint8, uint16, uint32, uint64, uint128, uint256) when you write uint means uint256. for example __uint favNumber = 7;__

    * int signNumberVariable (int8, int16, int32, int64, int128, int256) when you write int means int256. for example __int favNumber = -7;__

    * string stringVariable for example __string name = IronMan;__

    * array

    * Structs 

    * Mapping

2. visibility 
 
   * external : function can be called from other contracts and transactions 

   * public : as name suggest, anyone call method with public visibility

   * internal : this is the default visibility. contract itself and child contranct can access.

   * private : contract itself can call not it's child or anyone on blockchain.

3. Default Initializations values for different datatypes if value is not provided at the time on initalise a variable

    * boolean: false

    * string: ""

    * int: 0

    * uint: 0

    * fixed: 0.0 (presumably; this type is not fully supported)

    * enum: the first element of the enum

    * address: 0x0000000000000000000000000000000000000000 (or address(0))

    * function

        1. internal: empty function, returning
        2. initial values (if return is needed)
    external: function that throws when called

    * mapping: empty mapping

    * struct: a struct where all members are set to initial values

    * dynamically-sized: []
    * fixed-sized: an array of the fixed size where all elements are set to initial values

4. scope

    * State variables : State variables are permanently stored in the contract’s storage. They are defined outside of any function’s scope at the top level of contract.

    * Local variables : Local variables in Solidity are declared inside a function. They are only accessible within the function.

    * Global variables : Global variables in Solidity are some predefined special variables, that can be used in any scope in a Solidity program. Global variables provide information about the transactions and blockchain properties. __For example block.difficulty, block.gaslimit, msg.sender, msg.data, now etc.__

5. View function

> view indicates that the function will not alter the storage state in any way. But it allows you to "view" it

6. pure function

> pure is even more strict, indicating that it will not even read the storage state.

7. storage vs memory vs calldata

    * All the variables and arrays declared outside of the function are state variables and stored in Storage by default

    * The second storage type is a memory which is temporary storage. You can declare memory type variables only inside the function or to receive the function parameters.

    * The third storage type is calldata which is also a temporary storage just like memory. You might be wondering memory storage is already there then why do we need another temporary storage.Calldata is indeed temporary storage but it is a little different from memory. The main difference is calldata storage is non-modifiable storage which means once function parameters are passed you cannot modify them inside the function.




 

