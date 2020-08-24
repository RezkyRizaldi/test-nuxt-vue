<template>
  <div>
    <b-container fluid class="mb-5">
      <b-card-group class="my-card-group" deck id="nav-scroller" ref="content">
        <b-card title="【初配信】ホロライブ5期生の雪花ラミィです！【#ほろふぁいぶ】" border-variant="primary" header="Contoh" header-bg-variant="primary" header-text-variant="white" id="card">
          <div class="embed-responsive embed-responsive-16by9">
            <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/q0CNvUZe3ys?rel=0" allowfullscreen></iframe>
          </div>
          <template v-slot:footer>
            <small class="text-muted">
              <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
              <b-link v-b-tooltip.hover.bottom="tipData" class="my-link" href="https://www.youtube.com/channel/UCFKOVgVbGmX65RxO3EtH3iw">{{ text }}</b-link>
            </small>
          </template>
        </b-card>

        <b-card title="【初配信！】ホロライブ5期生、桃鈴ねねある🥟【#ほろふぁいぶ】" border-variant="primary" header="Contoh" header-bg-variant="primary" header-text-variant="white">
          <div class="embed-responsive embed-responsive-16by9">
            <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/fJ7ueGLuXk8?rel=0" allowfullscreen></iframe>
          </div>
          <template v-slot:footer>
            <small class="text-muted">
              <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
              <b-link v-b-tooltip.hover.bottom="'Nene Ch. 桃鈴ねね'" class="my-link" href="https://www.youtube.com/channel/UCAWSyEs_Io8MtpY3m-zqILA">Nene Ch. 桃鈴ねね</b-link>
            </small>
          </template>
        </b-card>

        <b-card title="【初配信】ホロライブ5期生、獅白ぼたん！【#ほろふぁいぶ】" border-variant="primary" header="Contoh" header-bg-variant="primary" header-text-variant="white">
          <div class="embed-responsive embed-responsive-16by9">
            <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/oDtBQCVGRQM?rel=0" allowfullscreen></iframe>
          </div>
          <template v-slot:footer>
            <small class="text-muted">
              <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
              <b-link v-b-tooltip.hover.bottom="'Botan Ch. 獅白ぼたん'" class="my-link" href="https://www.youtube.com/channel/UCUKD-uaobj9jiqB-VXt71mA">Botan Ch. 獅白ぼたん</b-link>
            </small>
          </template>
        </b-card>
      </b-card-group>
    </b-container>
  </div>
</template>

<script>
  export default {
    methods: {
      // Convenience method to scroll a heading into view.
      // Not required for scrollspy to work
      scrollIntoView(evt) {
        evt.preventDefault()
        const href = evt.target.getAttribute('href')
        const el = href ? document.querySelector(href) : null
        if (el) {
          this.$refs.content.scrollTop = el.offsetTop
        }
      }
    },
    data() {
      return {
        text: `
          Lamy Ch. 雪花ラミィ
        `,
        tipData: `
          Lamy Ch. 雪花ラミィ
        `
      }
    }
  }
</script>

<style>
  .my-card-group {
    /* position: relative;
    height: 300px;
    overflow-y: scroll; */
  }

  .my-link {
    color: #000;
  }

  .my-link:hover {
    text-decoration: none;
  }
</style>
