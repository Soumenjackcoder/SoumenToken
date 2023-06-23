# MyToken

This contract implements a basic token system with minting and burning capabilities.

## Requirements

1. The contract has public variables that store the details about the coin: token name, token abbreviation, and total supply.
2. The contract uses a mapping to track the token balances of addresses (`address => uint`).
3. The contract has a `mint` function that increases the total supply by a given value and increases the balance of a specified address.
4. The contract has a `burn` function that decreases the total supply by a given value and decreases the balance of a specified address.
5. The `burn` function includes conditionals to ensure that the balance of the sender is greater than or equal to the amount being burned.

## Usage

1. Deploy the `MyToken` contract on the Ethereum blockchain.
2. Access the public variables to get information about the token:
   - `tokenName`: The name of the token (e.g., "META").
   - `tokenAbbrv`: The abbreviation of the token (e.g., "MAT").
   - `totalSupply`: The total supply of the token.
3. Use the `mint` function to create new tokens:
   - Parameters: `_address` (address) - The address to receive the minted tokens.
                `_value` (uint) - The amount of tokens to mint.
   - Example:
     ```solidity
     MyToken myToken = MyToken(address);
     myToken.mint(receiverAddress, amount);
     ```
4. Use the `burn` function to destroy tokens:
   - Parameters: `_address` (address) - The address from which the tokens will be burned.
                `_value` (uint) - The amount of tokens to burn.
   - Example:
     ```solidity
     MyToken myToken = MyToken(address);
     myToken.burn(senderAddress, amount);
     ```

## Contributing

Contributions to this project are welcome. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and test thoroughly.
4. Commit your changes and push the branch to your forked repository.
5. Submit a pull request, providing a clear description of your changes.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
