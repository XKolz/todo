### 3. Create single todo item

#### POST REQUEST: `http://localhost:3000/todos/`

#### JSON Request

```
{
  "id": 8,
  "todo": "I love my family",
  "priority": "LOW",
  "status": "TO DO",
  "category": "HOME",
  "dueDate": "2023-02-22"
}
```

#### Response

```
Todo Successfully Added
```

---

### 4. Get a list of todd items(filtered by date created and or todo status)

#### GET REQUEST: `http://localhost:3000/agenda/`

#### Description:

Returns a list of all todos with a specific due date in the query parameter `/agenda/?date=2023-02-22`

#### Response

```
[
  {
    "id": 3,
    "todo": "Clean the house",
    "priority": "LOW",
    "status": "TO DO",
    "category": "HOME",
    "dueDate": "2023-02-22"
  }
]
```

- **Scenario 2**

### GET REQUEST: `http://localhost:3000/todos/?category=WORK&status=DONE`

### Description

Returns a list of all todos whose category is 'WORK' and status is 'DONE' in the query paramters for inputs

- **Response**

  ```
  [
    {
      "id": 4,
      "todo": "Code debugging",
      "priority": "MEDIUM",
      "status": "TO DO",
      "category": "WORK",
      "dueDate": "2023-01-12"
    }
  ]
  ```

### 5. Update a todo item status and or title (Just on one end point)

### PUT REQUEST: `http://localhost:3000/todos/:todoId/`

Updates the details of a specific todo based on the todo ID

- **Scenario 1**

  - **JSON Request**
    ```
    {
      "status": "DONE"
    }
    ```
  - **Response**

    ```
    Status Updated
    ```

- **Scenario 2**

  - **JSON Request**
    ```
    {
      "priority": "HIGH"
    }
    ```
  - **Response**

    ```
    Priority Updated
    ```

- **Scenario 3**

  - **JSON Request**

    ```
    {
      "todo": "Clean the house"
    }
    ```

  - **Response**

    ```
    Todo Updated
    ```

- **Scenario 4**

  - **JSON Request**
    ```
    {
      "category": "LEARNING"
    }
    ```
  - **Response**

    ```
    Category Updated
    ```

- **Scenario 5**

  - **JSON Request**
    ```
    {
      "dueDate": "2023-01-12"
    }
    ```
  - **Response**

    ```
    Due Date Updated
    ```
