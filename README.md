# aa-errors

Welcome to the error documentation repository for our SDK. This repository serves as a centralized hub for documenting, understanding, and resolving errors across our software stack. Our goal is to streamline the troubleshooting process and enhance the development experience by providing immediate access to error solutions and advice.

### How It Works

Our SDK queries this repository in real-time to fetch solutions and advice for any errors that occur. This integration facilitates a direct and efficient way to address issues, providing developers with the necessary information to solve problems as they arise.

## Contributing

Your contributions are vital to keeping this repository valuable and up-to-date. Whether you're fixing a typo, adding a new error, or refining the solution for an existing issue, your input helps improve our collective troubleshooting efforts.

### How to Contribute

1. **Submit a Pull Request (PR)**: Submit a PR to the main repository for review. Or...
2. **Edit the JSON directly** [here](https://github.com/bcnmy/aa-errors/edit/main/docs/errors.json) (be careful!).

**NB: The 'regex' field is used to match a thrown error from the SDK to your KnownError, so please make sure it is a string unique to your error**

#### Error Documentation Structure

```typescript
export type KnownError = {
  name: string;
  regex: string;
  description: string;
  causes: string[];
  solutions: string[];
};
```

#### Example:

```
{
    "name": "SmartAccountInsufficientFundsError",
    "regex": "aa21",
    "description": "You are not using a paymaster, and the sender address did not have enough native tokens to cover the gas costs associated with the user operation.",
    "causes": ["Your smart wallet does not have funds to send transaction."],
    "solutions": [
      "If you are not using a paymaster, verify that the sender address has enough native tokens to cover the required prefund.",
      "Send some native tokens in your smart wallet to be able to resolve the error.",
      "If you are looking to use a paymaster to cover the gas fees, verify that the paymasterAndData field is set."
    ]
}
```

### [Hosted errors](https://bcnmy.github.io/aa-errors/errors.json)
