<template>
  <div>
    <b-jumbotron class="bg-jumbotron text-center d-flex d-flex-r justify-content-center align-items-center" header="Test Jumbotron" lead="Belajar BootstrapVue" text-variant="light">
    <b-button v-b-tooltip.hover.top="tooltipText" variant="primary" href="#">{{ text }}
      <font-awesome-icon :icon="['fas', 'eye']" class="icon alt ml-1" style="font-size: 22px';"/>
    </b-button>
    </b-jumbotron>
  </div>
</template>

<script>
  export default {
    name: 'App',
    computed: {
    tooltipText: function() {
      // put your logic here to change the tooltip text
        return `
          View More
        `
      }
    },
    data() {
      return {
        text: `
          View More
        `
      }
    }
  }
</script>

<style>
  .bg-jumbotron {
  background-image: url("https://mdbootstrap.com/img/Photos/Others/gradient1.jpg");
  background-size: cover;
  min-height: 600px;
}

.d-flex-r {
  flex-direction: column;
}
</style>
