# Addition

Scenario: Add two numbers
  
  Given I have a calculator that's turned on.

  When I enter "number1"
  And I press "+" button
  And I enter "number2"
  And I press "=" button
  
  Then I see the "added sum" as the result

Scenario: Add more numbers

  Given I have a working calculator and have more than two numbers to add

  When I enter "number1"
  And I press "+" button And I enter "number2" And I press "+" button
  And I enter third number
  And I press "=" button
  
  Then I see the "final Added sum" as result

Scenario: Result is too large to display (or overrunning the limits)

  Given I have a calculator that's turned on.

  When I enter "number1"
  And I press "+" button
  And I enter "number2"
  And I press "=" button
  And if sum exceeds the limit
  
  Then I see the "sum in exponential form" as the result

Scenario: Numbers can be negative

  Given I have a Working calculator

  When I enter "number1"
  And I press "+" button
  And I enter "number2"
  And I press "=" button
  
  Then I see the "appropriate sum" as the result

Scenario: Numbers can be fraction

  Given I have a Working calculator

  When I enter "number1"
  And I press "+" button
  And I enter "number2"
  And I press "=" button
  
  Then I see the "sum in fractional form" as the result

Scenario: Number can be irrational

  Given I have a Working calculator

  When I enter "number1"
  And I press "+" button
  And I enter "number2"
  And I press "=" button
  
  Then I see the "sum in decimal form" as the result

Scenario: Length of each number

  Given I have a Working calculator

  When I enter either "number1" or "number2" and it's length exceeds predefined limit
  And I perform addition
  And I press "=" button
  
  Then I see the "sum in exponential form" as the result

Scenario: If number1 or number2 is not entered

  Given I have a Working calculator

  When I enter either "number1" or "number2"
  And I press "+" button
  And I press "=" button
  
  Then I see the "entered number" as the result

Scenario: If the number is real/complex

  Given I have a Working calculator and supports complex number addition

  When I enter "number1"
  And I press "+" button
  And I enter "number2"
  And I enter "number2"
  And I enter "=" button
  
  Then I see "real parts and complex parts added" as result

Scenario: If we are inbetween some operation

  Given I have a Working calculator

  When I enter "number1"
  And I press "+" button
  And I press "-" button
  And I enter "number2"
  And I enter "=" button
  
  Then I see the "difference between number1 and number2" as the result.
