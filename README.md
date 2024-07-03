# Passchecker: Password Strength Evaluation Tool

## Overview

This application is designed to evaluate the strength of passwords using various password strength algorithms. It provides users with a score for each entered password, helping them understand how secure their chosen passwords are in different security contexts.

## Supported Algorithms

The application currently supports the following password evaluation algorithms:

- **zxcvbn**: Developed by Dropbox, this algorithm estimates the number of attempts required to guess a password by considering common passwords, keyboard patterns, demographic data, and attack scenarios.

## Getting Started

### Prerequisites

- Node.js
- npm (Node Package Manager)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/librelynx/passchecker.git
   ```
2. Navigate to the project directory:
   ```bash
   cd passchecker
   ```
3. Install the dependencies:
   ```bash
   npm install
   ```

### Running the Application

To run the application on your local machine:

```bash
npm run dev
```

This will launch the application on `localhost:5173` (or another port if configured differently).

## Usage

Simply enter a password into the input field provided on the application's homepage. The results from each algorithm will be displayed, giving you a score or an estimation of how strong the password is according to each algorithm.

## Contributing

Contributions to this project are welcome! Here are a few ways you can help:

- Add new algorithms for password evaluation.
- Improve the existing algorithm implementations.
- Enhance the user interface for better usability.

To contribute, please fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the GNU AFFERO GENERAL PUBLIC LICENSE - see the [LICENSE.md](LICENSE) file for details.