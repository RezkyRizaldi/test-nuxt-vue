<template>
  <div id="myNav">
    <b-navbar class="bg-navbar" toggleable="lg" type="dark" variant="transparent" v-b-scrollspy:nav-scroller fixed="top">
      <b-navbar-toggle class="nav-toggle" target="sidebar-1"></b-navbar-toggle>
      <b-button v-b-toggle.sidebar-1 class="mr-2 sidenav-toogle" variant="success">Toggle Sidebar</b-button>
      <b-navbar-brand href="#" class="ml-2">NavBar</b-navbar-brand>

      <b-navbar-toggle class="nav-toggle" target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item active href="#card" @click="scrollIntoView">Card</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#">Link</b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Cari" autofocus></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit" variant="success">
              <font-awesome-icon :icon="['fas', 'search']" class="icon alt" style="font-size: 22px';"/>
            </b-button>
          </b-nav-form>

          <b-dropdown right variant="outline-transparent" class="ml-2" no-caret>

            <!-- Using 'button-content' slot -->
            <template slot="button-content">
              <span class="mr-2 text-dark">Username</span>
              <b-avatar badge badge-variant="success" src="../assets/img/miko.jpg" alt="ProfilPic User" class="m1" size="2.5rem"></b-avatar>
            </template>
            <b-dropdown-item href="#">
              <b-button v-b-modal.modal-center-profile variant="transparent">
                <font-awesome-icon :icon="['fas', 'user']" class="icon alt mr-2" style="font-size: 22px';"/>Profile
              </b-button>
            </b-dropdown-item>
            <b-dropdown-item href="#">
              <b-button v-b-modal.modal-center-logout variant="transparent">
                <font-awesome-icon :icon="['fas', 'power-off']" class="icon alt mr-2" style="font-size: 22px';"/>Logout
              </b-button>
            </b-dropdown-item>
          </b-dropdown>
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
