# ExpirationDatePickerDialog-Swift
A simple UIPickerView displayed within an UIAlertView in Swift that allows you to quickly add a picker for just month and year. This is useful when you want to do something like an expiration date picker for a credit card.

The current version is based on Swift 2 and iOS 9.

## Example Usage
    ExpirationDatePickerView().show("Select Expiration Date", doneButtonTitle: "Done", cancelButtonTitle: "Cancel", defaultMonth: defaultMonth, defaultYear : defaultYear) { (month: Int, year: Int) -> Void in
        let dateString = String(format: "%02d/%d", month, year)
        print(dateString) // 05/2015
    }


## Show parameters

- title: String **(Required)**
- doneButtonTitle: String
- cancelButtonTitle: String
- defaultMonth: Int
- defaultYear: Int
- callback: ((month: Int, year: Int) -> Void) **(Required)**

![ExpirationDatePickerDialog-Swift being used](example.jpg?raw=true)
	
The MonthYearPickerView uses a simple block-based "onDateSelected" method to return the date to you upon selection. By default, it selects the current month and year and shows upto 15 years in the future - this can be adapted easily should you wish you use this for something other than expiry dates.

## ExpirationDatePickerDialog is a combination of the following projects

* [@wSquimer] - DatePickerDialog-iOS-Swift(https://github.com/squimer/DatePickerDialog-iOS-Swift) 
* [@bendodson] - MonthYearPickerView-Swift(https://github.com/bendodson/MonthYearPickerView-Swift) 

## License

This code is distributed under the terms and conditions of the [MIT license](LICENSE). 
