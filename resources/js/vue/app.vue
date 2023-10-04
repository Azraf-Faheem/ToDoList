<template>
    <div class="todoListContainer">
        <div class="heading">
            <h2 id="title"> Welcome to TODOLIST</h2>
        </div>
    </div>
</template>

<script>
import addItemForm from "./addItemForm"
import listView from "./listView"

export default {
    components: {
        addItemForm
    }
}
</script>

<style scoped>
/* Scoped styles specific to this component */
.todoListContainer {
    /* Add your container styles here */
    margin: 20px;
    padding: 10px;
    border: 1px solid #ccc;
    background-color: #f5f5f5;
}

.heading {
    /* Add your heading styles here */
    font-size: 24px;
    color: #333;
    text-align: center;
}

#title {
    /* Add styles for the title here */
    font-weight: bold;
    text-decoration: underline;
}
</style>
