# TFL_UIAutomation

#Introduction

This project tests Plan a journey, edit a journey on results page and recently planned journeys functionality

#Decisions made during the creation on the Framework

1. To keep the project simple, all BDD scenarios are written in same feature file i.e. PlanAJourney.feature
2. Page object model is used to list all the locators based on the page they belong to 
3. Due to lack of time, high level scenarios written otherwise more scenarios can be writtena and implemented to test the each field thoroughly. 
For example below scenarios can be included to test From and To fileds thoroughly

Scenario: Verify that Plan a journey widget is unable to return results with invalid From location but valid To location
	Given I navigate to tfl.gov.uk
	And I enter invalid location in From field
	And I enter valid location in To field 
	When I click Plan my journey button
	Then I don't see the results

Scenario: Verify that Plan a journey widget is unable to return results with valid From location but invalid To location
	Given I navigate to tfl.gov.uk
	And I enter valid location in From field
	And I enter invalid location in To field 
	When I click Plan my journey button
	Then I don't see the results
	
Note: Due to lack of time, the implementation is not completed. I was not given enough notice about this challenge (The email arrived on Friday evening and I have limited access to emails until Sunday). If I had given enough notice then I would have completed it. Currently facing issues with the test runs. This implementation shows my thinking towards automating the UI features. 
