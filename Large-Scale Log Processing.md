# Large-Scale Log Processing

Background:
Imagine you're working at a company that receives billions of log entries each day. Each log entry is a string in the following 

```
timestamp, user_id, action_type
```

For example:
```
2023-10-11 10:15:45,12345,LOGIN
2023-10-11 10:15:46,12346,LOGOUT
```

Your task is to design and implement a system that can efficiently store, retrieve, and process these logs.

Requirements:
- Storage: Design a data structure that can efficiently store these logs.
- Retrieval: Implement a method to retrieve all logs for a specific user_id.
- Analysis: Implement a method to find the count of each action type (e.g., LOGIN, LOGOUT) for a given day.
- Constraints: You can assume the log entries are received in chronological order.The storage solution should be scalable to handle the large influx of logs.The retrieval and analysis operations should be efficient.

Code:

Please provide a high-level implementation for the above requirements.

Sample Solution
```
class LogSystem:
    def __init__(self):
        # Using a dictionary to store logs for each user_id.
        # This helps in efficient retrieval.
        self.user_logs = {}
        
        # Using a dictionary to store count of each action type for each day.
        self.daily_actions = {}

    def store_log(self, log):
        timestamp, user_id, action_type = log.split(',')
        
        # Storing log for the user.
        if user_id not in self.user_logs:
            self.user_logs[user_id] = []
        self.user_logs[user_id].append(log)
        
        # Updating daily action counts.
        date =
```
