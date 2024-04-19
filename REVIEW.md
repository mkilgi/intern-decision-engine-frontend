# Code Review

## Overview
The web application is clean and simple. API request is functional. There is everything needed for this type of site but I would make a few changes.

## Changes
- fixed dart warnings
- Fixed bug where valid amount did not update correctly if requested value and response value were exactly equal.
```dart
// If not approved
if (tempAmount < _loanAmount || tempPeriod > _loanPeriod) // used to be tempAmount <= _loanAmount
```
- Removed onChange submitting and replaced it with a button.
    - onChange requests made the site extremely laggy
    - there is no need for so many updates
    - this could potentially hinder our server performance
```dart
//Button for submitting form
  SizedBox(
    width: 130,
    height: 40,
    child: ElevatedButton(
        onPressed: _submitForm,
        child: const Text(
          "Apply",
          style: TextStyle(fontWeight: FontWeight.w600, fontSize: 16),
        )),
  ),
```
- Added color feedback to the requested loan sliders so it would be easier to understand if the loan approved or not.

## Conclusion
I really liked this web application. Different components were correctly separated and made it more readable. It was real easy to make a couple changes. Good job :D
