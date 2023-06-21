# Ruby-on-Rails-Backend-Assessment

Complex Ruby on Rails Backend Assessment:

Question: Implement a Ruby on Rails API endpoint that receives a JSON payload containing an array of user objects and performs advanced data processing tasks. The endpoint should return a modified JSON response based on the following requirements:

- The API endpoint should be a POST request at the path `/process_users`.
- The request payload should contain an array of user objects, where each user object has the following attributes: `id`, `name`, `age`, and `email`.
- The endpoint should perform the following tasks:
   1. Remove any users who are under 18 years old.
   2. Sort the remaining users alphabetically by their names.
   3. Calculate the average age of the remaining users.
   4. Group the users by the first letter of their names and return the count of users in each group.
- The endpoint should return a JSON response with the following structure:
   ```json
   {
     "average_age": 28.5,
     "user_count_by_initial": {
       "A": 2,
       "B": 3,
       "C": 1
     }
   }
   ```
   - The `"average_age"` field should contain the calculated average age.
   - The `"user_count_by_initial"` field should contain a key-value pair for each group, where the key is the first letter of the name and the value is the count of users in that group.
- You should implement separate Ruby methods or actions to handle each task and ensure they are called in the correct order.
- You can assume that the input will always be valid, and the user objects will contain the required attributes.


Example Input:
```json
{
  "users": [
    {"id": 1, "name": "Alice", "age": 28, "email": "alice@example.com"},
    {"id": 2, "name": "Bob", "age": 22, "email": "bob@example.com"},
    {"id": 3, "name": "Charlie", "age": 17, "email": "charlie@example.com"},
    {"id": 4, "name": "Alex", "age": 35, "email": "alex@example.com"},
    {"id

": 5, "name": "Bill", "age": 19, "email": "bill@example.com"},
    {"id": 6, "name": "Cindy", "age": 31, "email": "cindy@example.com"},
    {"id": 7, "name": "Ben", "age": 27, "email": "ben@example.com"}
  ]
}
```

In this example, the solution follows the given requirements by removing users under 18 years old, sorting the remaining users by name, calculating the average age, and grouping users by the first letter of their names to return the count in each group. The implementation handles each task separately within their respective methods and returns the modified JSON response as expected.
