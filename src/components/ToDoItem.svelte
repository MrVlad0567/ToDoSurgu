<script>
    export let id;
    export let text;
    export let isDone;
</script>

<div class="todo-item">
    <input class="todo-item__check" type="checkbox">
    <span class="todo-item__text">{text}</span>
    <button class="todo-item__btn">Delete</button>
</div>

<style>
    .todo-item {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 15px;
        background: rgb(231, 153, 153);
        border-radius: 10px;
    }

    .todo-item__check {
        
    }

    .todo-item__text {
        flex-grow: 1;
    }

    .todo-item__btn {
        border: none;
        border-radius: 10px;
        background-color: chocolate;
        padding: 10px;
        min-width: 100px;
    }
</style>