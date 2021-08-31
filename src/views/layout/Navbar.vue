<template>
  <div class="nav">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container">
        <a href="#" class="navbar-brand">
          Navigation
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarMarkep"
                aria-controls="navbarMarkes" aria-expanded="false" aria-lable="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse justify-content-end navbar-collapse" id="navbarMarkep">
          <div class="navbar-nav">
            <a href="../pages/Home.vue" class="nav-link active">Home</a>
            <a href="../pages/About.vue" class="nav-link">product</a>
            <a href="#" class="nav-link">services</a>
            <a href="#" class="nav-link">price</a>
            <a href="#" class="nav-link">business</a>
            <a href="#" class="nav-link">contact</a>
          </div>
          <form class="ms-5">
            <button class="btn btn-outline-success" type="login">sign in</button>
          </form>
        </div>
      </div>
    </nav>
  </div>

</template>

<script>
export default {
  name: "Navbar"
}
</script>

<style scoped>

</style>