# Developer Interview Exercise

Read through the entire exercise carefully.

## Instructions

Your task is to create an application that can be used to store user details, which will be accepted via an API, and stored in a database. You do not need to have a fully functioning application, but functional aspects are beneficial. The focus of this exercise is to see how you would build an application like this, so please try and include pseudocode or comments for areas that you do not have time to make fully functional.

## Application requirements

1) POST API endpoint that takes in the user model [below](#user-model) and stores it in a DB (SQL preferable but not required)
2) GET API endpoint to retrieve a user by `id`
3) Validation for the user model, with the appropriate API responses
4) Storage of the user in the DB (preferably SQL)

It is also helpful to consider how you will deploy this application.

## User Model

Feel free to add on to this model where you see fit. This model is to give an indication for the `User` payload for the GET and POST responses.

``` jsonc
{
    "id": "user_id_123456awd", // Required
    "name": "Test User", // Optional
    "phone_number" : "+27845522589", // Required
    "email" : "test@gmail.com", // Optional - valid email required
    "diagnostic_level" : 3, //Required - Integer in the range 0-10 (inclusive)
    "current_level" : 5, //Required - Integer in the range 0-10 (inclusive)
    "first_message_timestamp" : "Make this a datetime in ISO format", //Required
    "last_message_timestamp" : "Make this a datetime in ISO format", //Required
    "message_ids": [
        "msg_1234_awd",
        "msg_1235_awd",
        "msg_2356_dfg",
    ] // Required - All ids should be unique strings
}
```
