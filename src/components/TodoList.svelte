<script>
  import Todo from "./Todo.svelte";
  import Button from "./styleComponents/Button.svelte";
  import SectionContainer from "./styleComponents/sectionTemplateComponents/SectionContainer.svelte";

  let newTask = "";
  let tasks = []; // Type declared explicitly

  function addTask() {
    if (newTask.trim() !== "") {
      tasks = [...tasks, newTask.trim()];
      newTask = "";
      // Focus the input field after adding a task
      const inputElement = document.getElementById("taskInput");
      if (inputElement) {
        inputElement.focus();
      }
    }
  }

  function removeTask(index) {
    tasks = tasks.filter((_, i) => i !== index);
  }
</script>

<SectionContainer exampleNo="2" title="Todo List">
  <div
    style="display: flex; flex-direction: row; gap: 10px; width: 100%; justify-content: center"
  >
    <input
      type="text"
      bind:value={newTask}
      placeholder="New Task"
      class="input input-bordered input-secondary w-full max-w-xs"
      id="taskInput"
      on:keydown={(event) => {
        if (event.key === "Enter") addTask();
      }}
    />
    <Button text="add" on:click={addTask} />
  </div>

  <ul class="todo-list">
    {#each tasks as task, index}
      <li><Todo {task} remove={() => removeTask(index)} /></li>
    {/each}
  </ul>
</SectionContainer>

<!--
    Explanation:

    Todo Component: The Todo.svelte component displays a single task and a delete button. 
    It accepts the task's name and a remove function as props.
    TodoList Component:
        Adding Tasks: The addTask function adds a new task to the tasks array if it's not empty. 
        It uses two-way binding to clear the input after adding a task.
        Removing Tasks: The removeTask function removes a task by its index. 
        It creates a new array without the task at the given index.
        Rendering Tasks: The {#each} block renders the Todo component for each task in the tasks array, 
        passing the task name and remove function.


    The string.trim() method is a built-in JavaScript function that removes whitespace characters from 
    both the beginning and the end of a string. Whitespace characters include spaces, tabs, and newlines.


-->

<style global>
  .todo-list {
    list-style: none;
    padding: 20px;
    height: 300px;
    width: 500px;
    overflow-y: scroll;
    background-color: purple;
    color: white;
    border-radius: 10px;
  }

  .todo-list::-webkit-scrollbar {
    width: 10px;
  }

  .todo-list li {
    margin-bottom: 20px;
  }
</style>
