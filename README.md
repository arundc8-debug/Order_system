# Requisition System
## Overview
This is a Python code that runs requisition management system of staff purchases.
It allows staff to:
- Fill personal and requisition information.
- Adding items and  total costs.
- Decision on approval according to the cost limits.
- Answer remaining requisitions.
- See requisition statistics.
The program is an object-oriented program and it puts into practice some of the software design principles.

Principles of software design that were applied.
### 1. SRP.
This Principle ensures that every object is directed at a particular tasks.
•	staff_info() – gathers  staff information.
•	requisitions_total() – Adds   total cost.
•	requisition approval () - Determines whether it is approved or not.
•	respond_requisition() - Responds to requests.
•	display_requisition() – displays requisition.
•	requisition-statistic() -Shows requisition statistics.
 
### 2.  Encapsulation
It stores data of an object and the operations which operate with that data in one place and regulates the access so that it cannot be modulated by some unknown circumstances.
All the data of requisition form are stored as attributes within the RequisitionSystem class.
• Methods make direct use of this data.


### 3. DRY (Don’t Repeat Yourself)
The DRY principle is that one should not repeat the same code and instead, one should reuse methods or functions meaning that the changes will be made in a single location.
• The program does not repeat itself in certain areas.
• Still, there is repeated input validation (e.g. verification of empty strings).

###  4. Open/Closed Principle
  The code must be open to new features but closed to changing old code so,you can add new functionality without disrupting the functionality of the existing one.
• New approval levels or rules may also be added in requisition approval without affecting the structure of the method.
This ensures that the system is more adaptable and simple to maintain.

 
### 5. Separation of Concerns
Separation of Concerns separates a program into diffferent sections, with each section addressing a specific kind of work. 
Separate display methods such as display requisition and requisition statistic do not go hand in hand with processing methods such as requisitions total and requisition approval.It improves maintainability and makes it readable.

### 6. Information Expert
Information Expert refers to assigning a job to the component of the program that already possesses the data to perform it in an action, such that it does not have to rely on others.
RequisitionSystem Class- This is where all the requisition-related statistics (totals, approval, and status) are stored.
This internal data is required by the method requisition statistic, which is used to display statistics without additional input.
• This allows related data and behavior to be grouped together and hence the code can be easily comprehended and maintained.
###7. Polymorphism
Polymorphism refers to an interface taking on different data or behavior types of data.
Although a single class is used in this program, it may be extended through the application of polymorphism.

