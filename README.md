<!DOCTYPE html>
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
                        list.innerHTML += `<li>
                            ${task.title} - ${task.description} - ${task.status} - Assigned to: ${task.assigned_to} 
                            <button onclick="editTask(${task.id}, '${task.title}', '${task.description}', '${task.status}', '${task.assigned_to}')">Edit</button>
                            <button onclick="deleteTask(${task.id})">Delete</button>
                        </li>`;
                    });
                });
        }

        function addTask() {
            let title = document.getElementById('title').value;
            let description = document.getElementById('description').value;
            let status = document.getElementById('status').value;
            let assigned_to = document.getElementById('assigned_to').value;

            fetch('tasks.php', {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ title, description, status, assigned_to })
            }).then(() => fetchTasks());
        }

        function editTask(id, title, description, status, assigned_to) {
            document.getElementById('title').value = title;
            document.getElementById('description').value = description;
            document.getElementById('status').value = status;
            document.getElementById('assigned_to').value = assigned_to;
            document.getElementById('taskId').value = id;
        }

        function updateTask() {
            let id = document.getElementById('taskId').value;
            let title = document.getElementById('title').value;
            let description = document.getElementById('description').value;
            let status = document.getElementById('status').value;
            let assigned_to = document.getElementById('assigned_to').value;

            fetch('tasks.php', {
                method: 'PUT',
                headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
                body: `id=${id}&title=${title}&description=${description}&status=${status}&assigned_to=${assigned_to}`
            }).then(() => fetchTasks());
        }

        function deleteTask(id) {
            fetch('tasks.php', {
                method: 'DELETE',
                headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
                body: `id=${id}`
            }).then(() => fetchTasks());
        }
    </script>
</head>
<body onload="fetchTasks()">
    <h2>Task Manager</h2>
    <input type="hidden" id="taskId">
    <input type="text" id="title" placeholder="Task Title" required>
    <input type="text" id="description" placeholder="Description" required>
    <input type="text" id="status" placeholder="Status" required>
    <input type="text" id="assigned_to" placeholder="Assigned To" required>
    <button onclick="addTask()">Add Task</button>
    <button onclick="updateTask()">Update Task</button>
    <ul id="taskList"></ul>
</body>
</html>
