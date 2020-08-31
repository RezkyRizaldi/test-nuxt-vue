<template>
  <div>
    <b-container class="mb-5">
      <b-row>
        <b-col>
          <h2 class="text-center text-light mb-4" style="font-size: 48px;">Test Card On Carousel</h2>
        </b-col>
      </b-row>
      <b-row>
        <b-col>
          <b-carousel v-model="slide" :interval="0" controls @sliding-start="onSlideStart" @sliding-end="onSlideEnd">
            <b-carousel-slide>
              <template v-slot:img>
                <b-card-group deck id="nav-scroller" ref="content">
                  <b-card title="【初配信】ホロライブ5期生の雪花ラミィです！【#ほろふぁいぶ】" border-variant="primary" header="Contoh" header-bg-variant="primary" header-text-variant="white" id="card">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/q0CNvUZe3ys?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="tipData" class="my-link" href="https://www.youtube.com/channel/UCFKOVgVbGmX65RxO3EtH3iw">{{ text }}</b-link>
                      </small>
                    </template>
                  </b-card>

                  <b-card title="【初配信！】ホロライブ5期生、桃鈴ねねある🥟【#ほろふぁいぶ】" border-variant="warning" header="Contoh" header-bg-variant="warning" header-text-variant="white">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/fJ7ueGLuXk8?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="'Nene Ch. 桃鈴ねね'" class="my-link" href="https://www.youtube.com/channel/UCAWSyEs_Io8MtpY3m-zqILA">Nene Ch. 桃鈴ねね</b-link>
                      </small>
                    </template>
                  </b-card>

                  <b-card title="【初配信】ホロライブ5期生、獅白ぼたん！【#ほろふぁいぶ】" border-variant="success" header="Contoh" header-bg-variant="success" header-text-variant="white">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/oDtBQCVGRQM?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="'Botan Ch. 獅白ぼたん'" class="my-link" href="https://www.youtube.com/channel/UCUKD-uaobj9jiqB-VXt71mA">Botan Ch. 獅白ぼたん</b-link>
                      </small>
                    </template>
                  </b-card>
                </b-card-group>
              </template>
            </b-carousel-slide>
            <b-carousel-slide>
              <template v-slot:img>
                <b-card-group deck id="nav-scroller" ref="content">
                  <b-card title="【公式切り抜き】炎上に縁がありすぎるさくらみこまとめ【ホロライブ/さくらみこ】" border-variant="danger" header="Contoh" header-bg-variant="danger" header-text-variant="white" id="card">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/WqWqN10biP8?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="'Miko Ch. さくらみこ'" class="my-link" href="https://www.youtube.com/channel/UC-hM6YJuNYVAmUWxeIr9FeA">Miko Ch. さくらみこ</b-link>
                      </small>
                    </template>
                  </b-card>

                  <b-card title="【２周年記念】ワンルームシュガーライフ／湊あくあ【歌ってみた】" border-variant="info" header="Contoh" header-bg-variant="info" header-text-variant="white">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/UXUn_ZqeM4Q?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="'Aqua Ch. 湊あくあ'" class="my-link" href="https://www.youtube.com/channel/UC1opHUrw8rvnsadT-iGp7Cg">Aqua Ch. 湊あくあ</b-link>
                      </small>
                    </template>
                  </b-card>

                  <b-card title="flos / 猫又おかゆ (Cover)" border-variant="dark" header="Contoh" header-bg-variant="dark" header-text-variant="white">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/4muYzftomAE?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="'Okayu Ch. 猫又おかゆ'" class="my-link" href="https://www.youtube.com/channel/UCvaTdHTWBGv3MKj3KVqJVCw">Okayu Ch. 猫又おかゆ</b-link>
                      </small>
                    </template>
                  </b-card>
                </b-card-group>
              </template>
            </b-carousel-slide>
            <b-carousel-slide>
              <template v-slot:img>
                <b-card-group deck id="nav-scroller" ref="content">
                  <b-card title="太陽が似合うよ / Taiyou ga Niau yo | Airani Iofifteen Cover 「歌ってみた」" border-variant="primary" header="Contoh" header-bg-variant="primary" header-text-variant="white" id="card">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/Q4-h-IdOqLs?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="'Airani Iofifteen Channel hololive-ID'" class="my-link" href="https://www.youtube.com/channel/UCAoy6rzhSf4ydcYjJw3WoVg">Airani Iofifteen Channel hololive-ID</b-link>
                      </small>
                    </template>
                  </b-card>

                  <b-card title="【hololiveID】100k Subs Special : Marshmallow & Fans Submission Time 【Ayunda Risu】" border-variant="primary" header="Contoh" header-bg-variant="primary" header-text-variant="white">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/BIfh8QEtbOs?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="'Ayunda Risu Ch. hololive-ID'" class="my-link" href="https://www.youtube.com/channel/UCOyYb1c43VlX9rc_lT6NKQw">Ayunda Risu Ch. hololive-ID</b-link>
                      </small>
                    </template>
                  </b-card>

                  <b-card title="【Japanese.Ver】Baby Doll-Utopia | Moona Hoshinova Cover" border-variant="primary" header="Contoh" header-bg-variant="primary" header-text-variant="white">
                    <b-embed type="iframe" aspect="16by9" src="https://www.youtube.com/embed/jL8xPsLKCog?rel=0" allowfullscreen></b-embed>
                    <template v-slot:footer>
                      <small class="text-muted">
                        <font-awesome-icon :icon="['fas', 'address-card']" class="icon alt mr-1" style="font-size: 22px';"/>
                        <b-link v-b-tooltip.hover.bottom="'Moona Hoshinova hololive-ID'" class="my-link" href="https://www.youtube.com/channel/UCP0BspO_AMEe3aQqqpo89Dg">Moona Hoshinova hololive-ID</b-link>
                      </small>
                    </template>
                  </b-card>
                </b-card-group>
              </template>
            </b-carousel-slide>
          </b-carousel>
        </b-col>
      </b-row>
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
      },
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
    },
    data() {
      return {
        slide: 0,
        sliding: null,
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
  .my-link {
    color: #000;
  }

  .my-link:hover {
    text-decoration: none;
  }
</style>
