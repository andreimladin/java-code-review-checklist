# Java Code Review Checklist
I consider the following points a MUST for any Java developer for when he/she is pushing some changes for review or he/she is reviewing.

## Checklist for developers
- Code Quality
	- Basic Checks (before)
		- The code compiles
		- Old unit tests pass
	- The code was tested
		- The code was developer-tested
		- The new code must be covered by unit tests
		- Any refactoring must be covered by unit tests
	- Clean Code
		- Naming Conventions
		- No hard-coded variables
* Unit Testing
- Performance
	 Release resources (HTTP connections, DB connections, Files, any I/O streams )

# Code Quality
## Clean Code
Ensure that the code is clean as much as possible. Check also that SOLID principles are followed TODO Link to be provided
## Design Patterns
Recommend a design pattern where is the case
## Naming Conventions
# App Structure
Check that the changes are correctly written on layers and it respects the Spring Boot App Structure
Do not mixt up a Rest Service with a Web App
# Model
Understand the meaning of usage of each model and try to find where is the most appropriate to be placed as TODO - link to be provided
# Exception Handling
Ensure that each exception is raised and handled correctly TODO - Link to be provided
# Unit Testing
Coverage of minimum 80%
Ensure that all corner cases are covered and it follows the unit testing standards TODO - Link to be provided
# Rest API
Ensure that the API changes respect the REST maturity levels - TODO - Link to be provided
# Error Codes
Ensure that in case of a program error or exception, the API replies with the standard error codes TODO - Link to be provided
Bad example is Hubject-Adapter
# MVC
Ensure that the Model-View-Controller parts of the Web Application are compliant with the Best Practices TODO - Link to be provided
# Alerts
