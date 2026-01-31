# Singlish to Sinhala Translation Test Suite

## Project Overview
This project contains a comprehensive Playwright-based test suite for testing Singlish (Roman script Sinhala) to Sinhala (Sinhala script) conversion functionality.

## Test Coverage
- **Total Test Cases**: 34
  - Positive Test Cases: 23
  - Negative Test Cases: 11

### Test Categories

#### Positive Test Cases (Pos_Fun_0001-0023)
Tests that verify correct Singlish to Sinhala conversions including:
- Daily status messages
- Polite requests and greetings
- Office-related conversations
- Time and currency handling
- Conditional and negative questions
- Slang expressions
- Instructions with English terms

#### Negative Test Cases (Neg_Fun_0001-0011)
Tests that verify the system properly handles:
- Misspelled input
- Excessive spacing
- Joined words
- English abbreviations
- Mixed English conjunctions
- Complex conditional sentences
- Edge cases and error scenarios

## Prerequisites
- Node.js 18.x or higher
- npm (comes with Node.js)

## Installation

1. **Clone or extract the repository**
   ```bash
   cd IT23679894
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

   This will install:
   - `@playwright/test` - Playwright testing framework
   - `@types/node` - TypeScript type definitions

## Running the Tests

### Run all tests
```bash
npx playwright test
```

### Run tests with detailed output
```bash
npx playwright test --reporter=list
```

### Run tests in watch mode
```bash
npx playwright test --watch
```

### Run a specific test
```bash
npx playwright test --grep "Pos_Fun_0001"
```

### View HTML test report
```bash
npx playwright show-report
```

## Project Structure
```
IT23679894/
├── tests/
│   └── IT23679894_singlish_to_sinhala.spec.ts    # Main test file
├── playwright-report/                              # Test reports
├── test-results/                                   # Test result artifacts
├── playwright.config.ts                            # Playwright configuration
├── package.json                                    # Project dependencies
└── README.md                                       # This file
```

## Test File Details

### IT23679894_singlish_to_sinhala.spec.ts
Contains:
- Test data array with 34 test cases
- Each test case includes:
  - `id`: Unique test identifier
  - `name`: Descriptive test name
  - `input`: Singlish input text
  - `expected`: Expected Sinhala output
  - `type`: Test type (S for short, M for medium)

### Test Implementation
- **Positive Tests**: Verify that conversion produces expected Sinhala output
- **Negative Tests**: Verify that incorrect inputs produce different (wrong) output

## Configuration

### playwright.config.ts
- **Test Directory**: `./tests`
- **Browser**: Chromium (optimized for performance)
- **Reporters**: HTML report
- **Trace**: On first retry for debugging failed tests

## Expected Test Results
All 34 tests should pass:
- ✓ 23 Positive tests verify correct conversions
- ✓ 11 Negative tests verify proper error handling

## Troubleshooting

### Port already in use error
If you see "EADDRINUSE" when viewing reports:
```bash
# Kill existing node processes
Get-Process | Where-Object {$_.Name -like "*node*"} | Stop-Process -Force
```

### Tests not found
Ensure the test file is in the `tests/` directory:
```bash
npx playwright test tests/IT23679894_singlish_to_sinhala.spec.ts
```

### Dependencies not installed
```bash
rm -r node_modules
npm install
```

## Test Execution Time
- Average execution time: ~2-3 seconds for all 34 tests
- Parallel execution: Tests run across 6 workers by default

## Notes
- The test suite uses mock conversion functions for testing purposes
- In production, replace the mock function with actual Singlish-to-Sinhala API
- Test cases cover various linguistic patterns and edge cases

## Support
For issues or questions about the test suite, review the test file comments and playwright documentation at https://playwright.dev

## Author
Registration Number: IT23679894
Date: January 31, 2026
