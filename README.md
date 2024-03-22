# aa-errors

Welcome to the error documentation repository for our SDK. This repository serves as a centralized hub for documenting, understanding, and resolving errors across our software stack. Our goal is to streamline the troubleshooting process and enhance the development experience by providing immediate access to error solutions and advice.

### How It Works

Our SDK queries this repository in real-time to fetch solutions and advice for any errors that occur. This integration facilitates a direct and efficient way to address issues, providing developers with the necessary information to solve problems as they arise.

## Contributing

Your contributions are vital to keeping this repository valuable and up-to-date. Whether you're fixing a typo, adding a new error, or refining the solution for an existing issue, your input helps improve our collective troubleshooting efforts.

### How to Contribute

1. **Submit a Pull Request (PR)**: Submit a PR to the main repository for review.
2. **Edit the JSON directly** [here](https://github.com/bcnmy/aa-errors/edit/main/docs/errors.json) (be careful!).

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

### [Hosted errors](https://bcnmy.github.io/aa-errors/errors.json)
