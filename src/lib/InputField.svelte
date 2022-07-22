<script>
export let onSubmitHandler;
let value = "";

const onSubmit = () => {
    onSubmitHandler(value);
    value = "";
}
</script>

<form on:submit|preventDefault={onSubmit}>
    <input type="text" bind:value={value}/>
</form>
