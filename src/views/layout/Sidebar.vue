<template>
  <!--
    <div class="sidebar">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>Sidebar Header Part</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deserunt doloremque doloribus, explicabo impedit iure maiores maxime, praesentium quae quaerat quasi qui repellat reprehenderit tempore tenetur voluptatum? Assumenda doloribus quam vitae?</p>
          <div class="list">
            <h3>Sidebar List</h3>
            <ul>
              <li><a href="#">Home</a></li>
              <li><a href="#">About</a></li>
              <li><a href="#">Contact Out Time</a></li>
              <li><a href="#">Blog</a></li>
              <li><a href="#">Our Gallary</a></li>
              <li><a href="#">About Comapany</a></li>
              <li><a href="#"><i class="fas fa-ad"></i></a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
  -->

<div class="main_side_bar_part">
<div class="sider_bar displa_flax">
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="siderbar">
          <div class="title">
            Simple Title
          </div>
          <div class="menu-item">
            <router-link to="/"  :class="{'active' : activeMenu === index}" tag="button" class="menu_bt" v-for="(menu, index) in menus" :key="index" >
              <div  @click="activeMenu = index" class="link-contaciner">
                {{menu}}
              </div>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

</div>



</template>

<script>
export default {
  name: "Sidebar",
  data(){
    return{
      activeMenu: 0,
      menus: ['home', 'about','contact', 'blog', 'gallary', 'footer', 'Slider']
    }
  }
}
</script>
