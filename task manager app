<html>
<head>
    <title>Task Manager</title>
    <script>
        function fetchTasks() {
            fetch('tasks.php')
                .then(response => response.json())
                .then(data => {
                    let list = document.getElementById('taskList');
                    list.innerHTML = '';
                    data.forEach(task => {
                        list.innerHTML += `<li>${task.title} - ${task.description} - ${task.status}</li>`;
                    });
                });
        }

        function addTask() {
            let title = document.getElementById('title').value;
            let description = document.getElementById('description').value;
            let status = document.getElementById('status').value;

            fetch('tasks.php', {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ title, description, status })
            }).then(() => fetchTasks());
        }
    </script>
</head>
<body onload="fetchTasks()">
    <h2>Task Manager</h2>
    <input type="text" id="title" placeholder="Task Title" required>
    <input type="text" id="description" placeholder="Description" required>
    <input type="text" id="status" placeholder="Status" required>
    <button onclick="addTask()">Add Task</button>
    <ul id="taskList"></ul>
</body>
</html>
