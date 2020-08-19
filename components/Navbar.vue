<template>
  <div>
    <b-navbar class="bg-navbar" toggleable="lg" type="dark" variant="transparent">
      <b-navbar-toggle class="nav-toggle" target="sidebar-1"></b-navbar-toggle>
      <b-button v-b-toggle.sidebar-1 class="mr-2 sidenav-toogle" variant="success">Toggle Sidebar</b-button>
      <b-navbar-brand href="#">NavBar</b-navbar-brand>

      <b-navbar-toggle class="nav-toggle" target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item active href="#">Link</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit" variant="success">Search</b-button>
          </b-nav-form>

          <b-nav-item-dropdown text="Dropdown" right>

            <!-- Using 'button-content' slot -->
            <b-dropdown-item href="#">Profile</b-dropdown-item>
            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<style>
  .bg-navbar {
    background: linear-gradient(90deg, #30A4FB, #44E4C5);
  }

  @media screen and (max-width: 992px) {
    .sidenav-toogle {
      display: none;
    }
  }
</style>
