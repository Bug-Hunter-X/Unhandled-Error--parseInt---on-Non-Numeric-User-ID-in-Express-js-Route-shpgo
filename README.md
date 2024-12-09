# Express.js Route Handler Error: parseInt() Failure

This repository demonstrates a common error in Express.js route handlers:  failure to handle non-numeric values when parsing parameters intended to be integers.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides the corrected version.

The bug arises because the code directly uses `parseInt()` on the `req.params.id` without checking if it's actually a number. If a non-numeric value is passed as the user ID, `parseInt()` returns `NaN`, leading to potential errors or application crashes.

The solution adds robust error handling to prevent unexpected behavior.