<template>
  <!-- As a heading -->
  <nav
   class="navbar navbar-expand-lg navbar-light bg-light"
  >
    <navbar-brand
      text="MediumClone"
    />

    <navbar-toggler
      data-target="navbar"
      arial-controls="#navbar"
      aria-label="navbar"
      @click="toggleCollapse"
    />
    <navbar-collapse
      id="navbar"
      :active="active"
    >
      <navbar-nav>
        <navbar-item
          :active=" $route.path =='/' "
        >
          <navbar-link
            text="All post"
            label="go to home to view all post"
            to="/"
          />
        </navbar-item>
        <navbar-item
          :active=" $route.path == '/new-post' "
        >
          <navbar-link
            text="New post"
            label="go to new post to creat "
            to="/new-post"
          />
        </navbar-item>
      </navbar-nav>
    </navbar-collapse>
  </nav>
</template>

<script>

import NavbarBrand from './NavbarBrand'
import NavbarToggler from './NavbarToggler'
import NavbarCollapse from './NavbarCollapse'
import NavbarNav from './NavbarNav'
import NavbarItem from './NavbarItem'
import NavbarLink from './NavbarLink'

export default {
  name: 'Navbar',
  components: {
    NavbarBrand,
    NavbarToggler,
    NavbarCollapse,
    NavbarNav,
    NavbarItem,
    NavbarLink
  }
}

</script>

<style scoped>
</style>
