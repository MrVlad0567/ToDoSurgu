<script>
    import ToDoControls from "./ToDoControls.svelte";
    import ToDoItem from "./ToDoItem.svelte";

    const items = [
        {
            id: 1,
            text: 'Some TODO 1',
            isDone: false
        },
        {
            id: 2,
            text: 'Some TODO 2',
            isDone: false
        }
    ];
</script>

<div class="todo-app">
    <ToDoControls/>
    <div class="todo-app__field">
        {#each items as item}
            <ToDoItem id={item.id} text={item.text} isDone={item.isDone}/>
        {/each}
    </div>
</div>

<style>
    .todo-app {
        width: 700px;
        height: 80%;
        background: rgb(176, 168, 168);
        border-radius: 15px;
        padding: 40px;
        display: flex;
        flex-direction: column;
        gap: 30px;
    }

    .todo-app__field {
        background: white;
        flex-grow: 1;
        border-radius: 15px;
        overflow-y: auto;
        padding: 20px;
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
</style>