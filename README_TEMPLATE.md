# MyToken

This contract implements a basic ERC20 token with minting and burning functionality. The token has the following features:

## Requirements
1. The contract stores the details about the token, including its name, abbreviation, and total supply.
2. It maintains a mapping of addresses to token balances.
3. The contract provides a `mint` function that increases the total supply by a given value and increases the balance of the sender's address by that amount.
4. The contract provides a `burn` function that decreases the total supply by a given value and decreases the balance of the sender's address by that amount.
5. The `burn` function includes conditionals to ensure that the sender's balance is greater than or equal to the amount being burned.

## Usage

### Public Variables

- `tokenName`: A public variable that represents the name of the token.
- `tokenAbbrv`: A public variable that represents the abbreviation or symbol of the token.
- `totalSupply`: A public variable that represents the total supply of the token.

### Mapping

- `balances`: A mapping that associates addresses with their corresponding token balances.

### Minting

The `mint` function is used to increase the total supply and the balance of a specified address. It takes two parameters:

- `_address`: The address to which the tokens will be minted.
- `_value`: The amount of tokens to be minted.

When called, the function increases the total supply by the specified value and updates the balance of the given address accordingly.

### Burning

The `burn` function is used to decrease the total supply and the balance of a specified address. It takes two parameters:

- `_address`: The address from which the tokens will be burned.
- `_value`: The amount of tokens to be burned.

Before subtracting the value from the total supply and the address's balance, the function checks if the balance of the address is greater than or equal to the specified value. If the condition is met, the tokens are burned.

Note that if the condition is not met, the function will fail silently, and the tokens will not be burned.

## License

This code is licensed under the MIT License.
