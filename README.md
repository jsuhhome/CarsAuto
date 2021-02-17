CarsAuto

Requirements
==============================================================

* Visual Studio 2019 - Version 16.8.5
* .net core sdk 3.1. But I used version 5

StepsSteps to Run the Tests
=============================================================
1. Start Visual Studio 2019 (I used the community edition)

2. "Open a Project or Solution" (not "Open a local folder"), and in the "CarsAuto" folder, select "CarsAuto.sln" and open

2.1 Build the solution. It should download the nuget package dependencies.

3. In the "Test" menu, click on "Test Explorer". This will open the test explorer window. In the "test explorer window", drill down in TestCars until you see "CarTest1"

4. Right click "CarTest1" and click "Run". It should start running that test. 

5. the browser should start up automatically and run. Your Chrome version should match with the chrome driver that is in the \Browsers directory.



Project info
==============================================================
If you look in the right side of visual studio, you will see a "solutions explorer" window that has all the code.
You will notice 2 projects, AppDriver and TestCars. These compile to their own specific DLLs.

TestCars project is where the unit tests are. Open up Tests\CarsTests.cs to see the Xunit test that will run.

AppDriver project is the automation interface that the xunit tests will speak with.
The general idea is all tests should lie in the TestCars project should be written in a high level english like instructions. The code for these unit tests aren't the best examples since this is just a demo project. The details of how to carry our those high  level instructions are handled by the automation interface which acts as an abstraction layer between the actual unit tests and the application under test(cars.com).


This way changes in cars.com website only need to be handled in the AppDriver project. The actual tests in TestCars can remain the same.












