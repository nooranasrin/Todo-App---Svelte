<script>
import InputField from './InputField.svelte';
let todos = [];

const addTodoItem = (value) => {
  todos = [...todos, value];
}
</script>

<h1>Todo Lists</h1>
<InputField onSubmitHandler={addTodoItem}/>
<ul>
    {#each todos as todo}
    <li>{todo}</li>
    {/each}
</ul>
