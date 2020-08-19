<template>
  <div>
    <b-sidebar id="sidebar-1" toggleable="lg" title="Sidebar" text-variant="dark" shadow backdrop>
      <div class="px-3">
        <nav class="py-2">
          <b-nav vertical>
            <b-nav-item active class="my-link" href="#link-0">Active</b-nav-item>
            <b-nav-item class="my-link" href="#link-1">Link</b-nav-item>
            <b-nav-item class="my-link" href="#link-2">Another Link</b-nav-item>
          </b-nav>
        </nav>

        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
          </b-nav-form>
        </b-navbar-nav>
      </div>
    </b-sidebar>
  </div>
</template>
