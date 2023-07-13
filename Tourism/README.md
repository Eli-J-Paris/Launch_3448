# Launch Mod 3 Week 2 Assessment

## Questions (10 Points)

1. Define MVC and explain the purpose of each of the three parts of this pattern:
MVC or Model View Controller is a way of structuring code by splitting an application into 3 different parts.
    - Model: handles all data logic and interacts with the database
    - View: Dynamicly renders an html file that the controller sends to it. In short its what the user will see
    - Controller: acts as a middle man between model and view as it will handle the flow from requests from the client and responses from the server
    </br>
    </br>
    It should be noted that to have a true MVC the model and view should never directly interact with one another but always go through the controller.
    
2. Explain the difference between the **New** route and the **Create** route: New will make a GET request for a new object to be created and will return a view. While Create will make a POST request that will create that new object inside of the database and be returned as a redirect instead of a view.

3. List all of the RESTful routes for the `employee` entity. Make sure to include the Route Name, Path, and HTTP Method for each of the routes. (2 points)
 - the "employee" entity can have 7 different restful routes
 - 1. Index: /Employee   GET
 - 2. New: /Employee/new GET
 - 3. Create /Employee   POST
 - 4. Show /Employee/id  GET
 - 5. Edit /Employee/id/edit  GET
 - 6. Update /Employee/id  PUT
 - 7. Destroy /Employee/id  DELETE


</br>
For the following three questions, explain both how to fix the error/bug and why the part of the code that was broken is important. (2 points each)

4. inside of the controller you will have pass in the hotels into the return view() action so that the index.cshtml view will know about the hotels
<img width="1213" alt="Screenshot 2023-06-13 102204" src="https://github.com/turingschool/launch-curriculum/assets/11747682/f37c233d-e7aa-483e-9f75-7c9b111811e5">

5.The controller for hotels is "Index" while the view is "Indexes" These need to be the same to know about each other.
<img width="1245" alt="Screenshot 2023-06-13 102555" src="https://github.com/turingschool/launch-curriculum/assets/11747682/87c9fbf7-de63-4580-9b36-8632df27b91b">

6. You have to put the `@` symbol before writing any sort of c# code  so in front hotel.name and hotel.location
<img width="1238" alt="Screenshot 2023-06-13 102856" src="https://github.com/turingschool/launch-curriculum/assets/11747682/a39b525d-ae05-463f-b724-be68aa70148c">

## Exercise (10 Points)

Make sure to first run `update-database` to populate the `Tourism` database used by this application.

This application already has the `Index` route for States.

Your task is to do the following:
1. Add the `Show` RESTful route to display the name and abbreviation for a particular state.
1. Add a test for your new `Show` route in the `StateCRUDTests.cs` file.
