<template>
<div class="todo_header_component">
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="todoListContainer">
          <h2 id="title">{{ $parent.ListHeader }}</h2>

          <div class="input_part">
            <div v-if="!$parent.isEditing" class="input_part">
              <input type="text" v-model="todo" placeholder="Add To Do Any Thing">
              <input type="submit" value="add" @click="storeTodo">
            </div>


            <div v-else>
              <input type="text" v-model="$parent.todo">
              <input type="submit" value="update" @click="updateTodo">
            </div>
            <div id="app" @click="$parent.showList = !$parent.showList" class="hide_show">
              <button class="hide" :class="$parent.showList ? 'btn-danger' : 'btn-primary'" :style="{'fontSize' : padding+'px'}">{{ $parent.showList ? 'Hide' : 'Show' }} List</button>
            </div>
            <div @click="padding--" class="btn btn-primary btn-sm">-</div>
            <div @click="padding++" class="btn btn-success btn-sm ms-2">+</div>
          </div>
          <!--            &lt;!&ndash; Binding Section&ndash;&gt;-->
          <!--            <div class="binding_chack">-->
          <!--              <input class="input_binding"-->
          <!--                  type="checkbox"-->
          <!--                  @change="updateCheck()"-->
          <!--                  v-model="item.completed"/>-->
          <!--              <span :class="[item.completed ? 'completed' : '', 'itemText' ]"> {{ item.name }} </span>-->
          <!--              <button @click="removeItem()" class="trashcan">-->
          <!--                <font-awesome-icon icon="trash"/>-->
          <!--              </button>-->
          <!--            </div>-->




          <!--            <ol>-->
          <!--              <li v-for="(todo, index) in todos">-->
          <!--                {{ todo }}-->

          <!--                <button @click="editTodo(index, todo)">Edit</button>-->

          <!--                <button @click="deleteTodo(index)">Delete</button>-->

          <!--              </li>-->
          <!--            </ol>-->

        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>






export default {
  name: "TodoHeaderComponent",
  data() {
    return {
      todo : "",
      padding : 15,

    }
  },
  methods:{
    storeTodo(){
      if(this.todo){
        let data =  {
          name :this.todo,
          active : 0
        }
        this.$parent.todos.push(data)
      }
      this.todo =''
    },
    updateTodo(){
      this.$parent.todos[this.$parent.selectedIndex].name = this.$parent.todo
      this.$parent.isEditing = false
    }
  }
}


</script>

<style scoped>

</style>