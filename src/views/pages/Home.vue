<template>
  <div class="home displa_flax">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="input_item">
            <h1>{{ text }}</h1>
            <input type="text" v-model="text" placeholder="Enter Any Thing" >
          </div>
          <!--
          <ul>
            <li v-for="(data,index) in dataList" :key="index">{{ index+1+'.' }} {{ data }}</li>
          </ul>
          -->


          <div class="section mt-4">
            <p>{{ head }}</p>
            <!--
              <p>{{ bangladesh }}</p>
            -->
          </div>

          <!--
            <div class="todoListContainer">
              <h2 id="title">{{ ListHeader }}</h2>

              <div class="add_item">
                <input type="text" v-model="item.name">
                <font-awesome-icon icon="plus-square"
                                   @click="addItem()"
                                   :class="[ item.name ? 'active' : 'inactive','plus']"/>

              </div>
            </div>
              -->

          <!--  This is New Section  Part-->

          <div id="app">
            <div class="body_part">
              <TodoHeaderComponent></TodoHeaderComponent>
              <TodoListComponent></TodoListComponent>
            </div>
          </div>



        </div>
      </div>
    </div>
  </div>

</template>

<script>





import TodoHeaderComponent from "@/views/component/TodoHeaderComponent";
import TodoListComponent from "@/views/component/TodoListComponent";
export default {
  name: 'Home',
  components: {TodoListComponent, TodoHeaderComponent},
  data(){
    return{
      activeMenu: 0,
      showList : true,
      menus: ['home', 'about','contact', 'blog', 'gallary', 'footer', 'Slider'],
      text : "Enter Any Thing",
      dataList : ['aaa','bbb','ccc','ddd'],
      head : "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium architecto et expedita harum magnam nulla repellendus sed temporibus voluptates. Accusantium amet animi at dolore doloribus eaque, eius enim, error excepturi iure nemo nesciunt possimus quidem rerum similique tempora voluptatem. Culpa?",
      bangladesh : "My First Vue Todo List Content",
      ListHeader :"To Do List Header",
      item:{name :""},
      todos: [
        {
          name : "List First",
          active : 0
        } ,
        {
          name : "List Second",
          active : 0
        }
      ],
      todo: '',
      selectedIndex: null,
      isEditing: false,
      props: ['item']
    }
  },
  methods:{
    deleteTodo(index){
      this.todos.splice(index, 1)
    }
  },


}






</script>
