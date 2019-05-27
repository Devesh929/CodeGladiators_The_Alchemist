This File Constains basic idea of project, for testing instructions refer-(testing instructions.txt)
For Team Details and Project Link Details refer "UiPath_-_Submission.docx"
For proper architecture refer ppt.

Our idea is to develop a project for Unit Testing  that works as a plug and play component. We are developing a framework which will run all the unit tests in a folder and generates a log report stating results of all tests (pass/fail) also stating the errors if a particular unit test case is failed.

-->Unit Tests are the cases designed to test any algorithm, logic, workflow.
 
Our project includes-

 Framework : used for automated running of unit tests and logging.
 Custom activity package: that plays essential part in running of Framework and Unit Tests both.
 Unit Test Template :used to easily make unit tests.

Resulting product is a Framework that:

-->Can be integrated into any UiPath project or framework (can be placed inside any folder or sub-folder and it will still work out of the box).
-->Can run any .xaml file found in Test_Repository folder and also make a distinction if .xaml file is a Unit Test or not (user is notified via log).
-->Logs test runs and gives extensive information about failed tests (both inside UiPath console and in textual log files).

*****Unit tests*******
Framework has no use if there are no tests to be run. As such, biggest effort required from the developers themselves is in writing of Unit Tests. Luckily, by using unit test template, custom activity and Assert methods, this is much less of a chore.

Basic idea of Unit Testing is to arrange a set of data that will be used to test the code.

After running of code that is being tested, output is compared with the expected value.

Comparison should give information if test have passed or not.

Unit testing comprises of three stages:

-->Arrange
-->Act
-->Assert.

Arrange Stage
Purpose of the arrange stage is to define input parameters for the test:
Manually define parameters and data
(If needed) Define expected result
(If needed) Read configuration file

Act Stage
Purpose of act stage is to run the code that is being tested (by invoking the code and supplying it previously arranged data).

Output of this stage should be actual value that code produces assigned to the actual variable.

Assert Stage
Purpose of the assert stage is to evaluate test outputs (usually this is done by comparing actual value gotten by running the code with the expected value that was defined in the arrange stage, but is not the only type of test that can be done).


Assert methods make writing of Unit Tests much easier and exceptions thrown by these methods serve a big role in Framework logging.
Quick guide:

Assert Unit Test activity is used as a container for writing Assert methods (imported from CustomActivities.VariableComparer namespace) which are used to evaluate unit test outputs.
