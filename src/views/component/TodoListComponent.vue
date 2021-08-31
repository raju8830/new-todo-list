<template>
<div v-if="$parent.showList" class="todo_list_component">
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <ul class="order_list_part">
          <li v-for="(todo, index) in $parent.todos" :key="index">
            {{ index+1 }}.
            <input v-model="todo.active" class="input_binding"
                   type="checkbox"/>
            <span :class="todo.active ? 'active' : '' || index == 0 ? 'first_child': '' || index == $parent.todos.length -1 ? 'last_child': ''" class="active_part">{{ todo.name }}</span>

            <button @click="editTodo(index, todo)" style="background: #2c3e50;border: none;margin: 0px 5px 5px 0px;border-radius: 5px;color: #ffffff;padding: 5px 10px">Edit</button>

            <button @click="deleteTodo(index)" style="background: #F24C00;border: none;margin: 0px 0px 5px 0px;border-radius: 5px;color: #ffffff;padding: 5px 10px">Delete</button>

          </li>
        </ul>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "TodoListComponent",
  methods:{
    editTodo(index, todo){
      this.$parent.todo = todo.name
      this.$parent.selectedIndex = index
      this.$parent.isEditing = true
    },
    deleteTodo(index){
      this.$parent.todos.splice(index, 1)
    }
  }
}
</script>

<style scoped>

</style>