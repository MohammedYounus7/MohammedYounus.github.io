<!DOCTYPE html>
<html lang="en">
<head>
    <meta cha
    function addTask() {
        const taskInput = document.getElementById("task-input").value;
        if (taskInput) {
            toDoList.push(taskInput);
            displayTasks();
        }
    }
    function displayTasks() {
        const output = document.getElementById("to-do-list-output");
        if (toDoList.length === 0) {
            output.innerHTML = "No tasks available.";
        } else {
            output.innerHTML = toDoList.map((task, index) => `${index + 1}. ${task}`).join("<br>");
        }
    }
</script>

</body>
</html>
