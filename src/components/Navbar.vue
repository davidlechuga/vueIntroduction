<template>
<!-- As a heading -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <navbar-brand
            text= "MediumClone"
        />
        <navbar-toggler
        data-target="navbar"
        arial-controls="#navbar"
        aria-label="navbar"
        />
        <navbar-collapse id="navbar">
          <navbar-nav>
            <navbar-item>
              <navbar-link
                text="hola"
                label="que onda"
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
