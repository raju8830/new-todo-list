<template>
<div class="main_footer">
  <div class="container">
    <div class="row">
      <div class="col-md-3">
        <div class="footer_part">
          <h3>Company logo</h3>
          <img src="https://png.pngtree.com/png-clipart/20190613/original/pngtree-facebook-icon-png-image_3584912.jpg" alt="">
        </div>
      </div>
      <div class="col-md-3">
        <div class="footer_part">
          <h3>Company Link option</h3>
          <div class="menu-item">
            <router-link to="/"  :class="{'active' : activeMenu === index}" tag="button" class="menu_bt" v-for="(menu, index) in menus" :key="index" >
              <div  @click="activeMenu = index" class="link-contaciner">
                {{menu}}
              </div>
            </router-link>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="footer_part">
          <h3>Company Link</h3>
          <div class="menu-item">
            <router-link to="/"  :class="{'active' : activeMenus === index}" tag="button" class="menu_bt" v-for="(menu, index) in menuss" :key="index" >
              <div  @click="activeMenus = index" class="link-contaciner">
                {{menu}}
              </div>
            </router-link>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="footer_part">
          <h3>Company Address</h3>
          <div class="addres">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium aliquam aliquid commodi harum soluta vel!</p>
            <span>Dhaka, Mohammadpur <br>1200 Dhaka</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "Foote",
  data(){
    return{
      activeMenu: 0,
      menus: ['This is the Footer Part', 'Single Footer', 'Custion Footer Part', 'sider Footer part'],

      activeMenus: 0,
      menuss: ['This is the Footer Part', 'gallary', 'Custion Footer Part', 'sider Footer part'],
    }
  }
}
</script>

<style scoped>

</style>