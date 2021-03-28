<script>
    import { fly } from 'svelte/transition';
    let todoItem = "";
    let todoList = [];
    //add items from input feild to array
    function addToList() {
        if (!todoItem) return;
        todoList = [...todoList, {
            text: todoItem,
            status: false
        }];
        todoItem = '';
    }
    //is going to remove items from array
    function removeFromList(index) {
        todoList.splice(index, 1);
        todoList = todoList;
    }
</script>

<form on:submit|preventDefault={addToList}>
    <input bind:value = {todoItem}>

</form>

<ul class="todo-list">
    {#each todoList as item, index}
    <li transition:fly= "{{ y: 20, duration: 200}}">
    <input bind:checked={item.status} type="checkbox" class="checkbox">
    <span class:checked={item.status}>{item.text}</span>
    <button class="delete" type="button" on:click={() => removeFromList(index)}>remove</button>  
    </li>
    {/each}
</ul>

<style>
    .todo-list {
        list-style: none;
    }
    .checked {
        text-decoration: line-through;
    }
    form {
        text-align: left;
        margin-top: 1%;
        margin-bottom: 1.5%;
    }
    ul {
        text-align: left;
    }
</style>