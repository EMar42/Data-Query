# Boolean Query Tree

Boolean Query Tree is a tool for flexible filtering of flat JSON data using boolean operations. It allows you to apply various conditions to filter data, providing more flexibility compared to limited filter options. The tool is suitable for applications like web apps, where users want to filter products based on custom conditions, or for data analysts who need to filter large datasets using specific conditions.

## Features

- Filter flat JSON data using flexible boolean conditions.
- Supports operators like "AND," "EQUAL," "LARGER THAN," and more.
- Allows nesting of filter operators within each other.
- Can be used with CSV data by converting it into a JavaScript object.

## Usage

1. Install the required dependencies:

2. Import the `BooleanQuery` class and use its methods to perform boolean queries on your data.

```javascript
const BooleanQuery = require('./boolean-query/BooleanQuery');

// Example usage for a single object
const objectToFilter = { /* Your object data here */ };
const operation = "AND(EQUAL(property1, value1), OR(EQUAL(property2, value2), LOWER_THAN(property3, value3)))";
const result = BooleanQuery.check(objectToFilter, operation);

// Example usage for a list of objects
const objectsToFilter = [ /* Your array of objects here */ ];
const operation = "AND(EQUAL(property1, value1), OR(EQUAL(property2, value2), LOWER_THAN(property3, value3)))";
const filteredObjects = BooleanQuery.checkMany(objectsToFilter, operation).findAll();
```
// Additional examples and methods are available in the code files.


## File Structure
The file structure of this project is as follows:

boolean-query/BooleanQuery.js: Contains the implementation of the BooleanQuery class, which provides the core filtering functionality.
index.js: Includes sample usages of the BooleanQuery tool with hardcoded data.
test.js: Contains test cases to validate the functionality of the BooleanQuery tool.
sampleData.js: Provides sample data that can be used for testing and experimentation.

Testing
This project includes unit tests to ensure the correctness of the BooleanQuery tool. To run the tests, execute the following command:

```bash
npm test
```

## Contributions
Contributions to this project are welcome! If you have any suggestions, improvements, or bug fixes, feel free to open an issue or submit a pull request.

```Feel free to modify and expand upon this README template according to your project's specific needs.```

