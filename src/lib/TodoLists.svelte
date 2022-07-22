<script>
let value = "";
let todos = [];

const addTodoItem = () => {
    todos = [...todos, value];
    value = "";
}
</script>

<h1>Todo Lists</h1>

<form on:submit|preventDefault={addTodoItem}>
    <input type="text" bind:value={value}/>
</form>

<ul>
    {#each todos as todo}
    <li>{todo}</li>
    {/each}
</ul>
