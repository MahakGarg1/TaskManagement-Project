# TaskManagement-Project
## Supported Functionalities
1. Add tasks
2. Get all tasks
3. Get tasks by completion and priority
4. Update individual task
5. Delete individual task

## Dependencies
Express, CORS

## Commands to Start the Project
### Install Dependencies
```
npm install
```
### Start Server
```
npm run start
```

## End Point Documentation
### Create a task
```
curl --location 'http://localhost:3001/tasks' \
--header 'Content-Type: application/json' \
--data '{
    "id": 1,
    "priority": "medium",
    "title": "Sleep at 10PM",
    "description": "Make sure to go to bed at 10PM",
    "completed": true
}'
```

### Get all tasks

```
curl --location ''\''http://localhost:3001/tasks' \
--data ''
```

### Get tasks based on completion status(query param - 'completion=true|false')
```
curl --location 'http://localhost:3001/tasks?completion=true' \
--data ''
```

### Get tasks based on priority level
```
curl --location 'http://localhost:3001/tasks/priority/high'
```

### Get individual task details
```
curl --location 'http://localhost:3001/tasks/3'
```
### Update individual task

```
curl --location --request PUT 'http://localhost:3001/tasks/1' \
--header 'Content-Type: application/json' \
--data ''\''{
    "id": 1,
    "priority": "medium",
    "title": "Sleep at 10PM",
    "description": "Make sure to go to bed at 10PM",
    "completed": true
}'\
```
### Delete individual task
```
curl --location --request DELETE 'http://localhost:3001/tasks/1' \
--data ''
```
