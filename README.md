# Java Code Review Checklist
I consider the following points a MUST for any Java developer for when he/she is reviewing some Java code changes.

## Checklist for developers
### Code Quality
- Basic Checks (before)
	- The code compiles
	- Old unit tests pass
- The code was tested
	- The code was developer-tested
	- The new code must be covered by unit tests
	- Any refactoring must be covered by unit tests
	- At least 80% coverage for the code changes
	- [EMP] Unit tests should be compliant to the standards posted here
- Clean Code
	- Naming Conventions (classes, constants, variables, methods (void vs return), etc)
	- No hard-coded variables
	- Indentation
	- No spelling mistakes
	- The code does what it says it does
	- The code is easy to read (**Readability**)
	- Avoid duplicate code
	- Check if the code could be replaced by calling functions in other libraries/components
- Best Practices
	- OOP Principles are correctly used
	- The code follows the SOLID PRINCIPLES
	- Design Patterns
		- Recommend a design pattern when you fill that a pattern could fit there
- Exception Handling
	- Ensure that each exception is raised and handled correctly
	- Ensure that you have a well-defined exception hierarchy
	- Split the exceptions in two types: technical and business

### Application Structure
- Ensure that your changes are correctly written on layers and it respects the Spring Boo App Structure
- Do not mixt up a Rest Service with a Web App (like Spring Rest with Spring MVC )

### Model
- Understand the meaning of each model you defined and treat it like the most appropiate terminology for it: DTO (form for MVC), entity, Value Object, Java Bean
- Place it in the correct package
- For more details check this page [TODO link to be provided]

### Rest API
- Ensure your Rest API respects the REST maturity levels
- Error Codes
	- Ensure that in case of any error or exception the API replies with the standard error codes (defined at the system level)
	- Do not write Rest API which have different directions for receiving requestions from
		- Example: having a service which facilitates communication with an external 3rd party, do not expose the same service for the 3rd party to request back, for this use a different service (e.g. a notification service)
		- You can get into a confusion when you have to handle differently the same exception in the service, but it comes from different directions, you have 2 clients and cannot reply with the same error codes (one should be internally and the other one specific to the 3rd party)
- DTO
	- Use DTO pattern for passing data between controller and service layer (at least when using **sensitive** or **aggregated** data)

### MVC
- Ensure that your Model-View-Controller parts of the Web Application are compliant to the Best Practices
	- JSP don't have business logic (no Java code, only JSTL, Spring or Thymeleaf tags)
	- Model doesn't have business logic
	- Controller delegates the requests to the business (service) layer, it doesn't have logic
	- Use DTO (classes ending with Form in case of MVC) pattern for passing data between controller and service layer (at least when using **sensitive** or **aggregated** data)

### Performance
- Release resources (HTTP connections, DB connections, Files, any I/O streams )

### Security

### Thead-safety
- Ensure your code is not a candidate for race conditions and deadlocks

### Logging

### Alerting

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
