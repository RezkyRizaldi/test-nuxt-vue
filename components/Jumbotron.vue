<template>
  <div>
    <b-jumbotron class="bg-jumbotron text-center d-flex d-flex-r justify-content-center align-items-center" header="Test Jumbotron" lead="Belajar Nuxt.js dengan BootstrapVue2" text-variant="light">
      <b-button v-b-toggle.collapse-2 v-b-popover.hover.blur.left="popover" title="Latihan" variant="primary" @click="makeToast('primary')" href="#" class="mb-3">{{ text }}
        <font-awesome-icon :icon="['fas', 'eye']" class="icon alt ml-1" style="font-size: 22px';"/>
      </b-button>

      <!-- Element to collapse -->
      <b-collapse id="collapse-2">
        <b-card text-variant="dark">Hello, World!</b-card>
      </b-collapse>
    </b-jumbotron>
  </div>
</template>

<script>
  export default {
    // computed: {
    // tooltipText: function() {
    //     put your logic here to change the tooltip text
    //     return `
    //       View More
    //     `
    //   }
    // },
    data() {
      return {
        text: `
          View More
        `,
        popover: `
          Ini adalah file latihan Nuxt.js menggunakan BootstrapVue 2
        `
      }
    },
    methods: {
      makeToast(variant = null) {
        this.$bvToast.toast('Toast body content', {
          title: `Variant ${variant || 'default'}`,
          variant: variant,
          solid: true
        })
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
