# Mocking

- Overriding or changing the behaviour of dependency for the purpose of test
- Let you isolate a specific piece of code

## Advantages
- Avoid relying on external services
- Avoid unitanding consequences 
    - sending emails
    - deleting data 
    - etc..
- Speeds up tests
    - delays and data bases might be mocked

## Tools 
- unittest.mock 
    - `MagicMock` / `Mock` - replace real objects
    - `patch` - override behaviour