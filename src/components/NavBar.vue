<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="success">
      <b-container>
        <b-navbar-brand href="#">Blog</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-collapse id="nav-collapse" is-nav>
              <b-navbar-nav>
                <b-nav-item :to="{ name: 'Home' }">Home</b-nav-item>
                <b-nav-item :to="{ name: 'About' }">About</b-nav-item>
                <b-nav-item href="#">Posts</b-nav-item>
              </b-navbar-nav>
            </b-collapse>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
};
</script>
