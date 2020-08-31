<template>
  <div>
    <b-container fluid class="mb-5">
      <b-row>
        <b-col>
          <h2 class="text-center text-light mb-4" style="font-size: 48px;">Test Carousel</h2>
        </b-col>
      </b-row>
      <b-row>
        <b-col>
          <b-carousel fade :interval="4000" controls indicators @sliding-start="onSlideStart" img-width="1024" img-height="400" style="text-shadow: 1px 1px 2px #333" @sliding-end="onSlideEnd">
            <b-carousel-slide img-src="../assets/img/bg-miko.png">
              <h1>Hello world!</h1>
            </b-carousel-slide>
            <b-carousel-slide img-src="../assets/img/bg-miko2.png">
              <h1>Hello world! 2</h1>
            </b-carousel-slide>
            <b-carousel-slide img-src="../assets/img/bg-miko.png">
              <h1>Hello world! 3</h1>
            </b-carousel-slide>
            <b-carousel-slide img-src="../assets/img/bg-miko2.png">
              <h1>Hello world! 4</h1>
            </b-carousel-slide>
            <b-carousel-slide img-src="../assets/img/bg-miko.png">
              <h1>Hello world! 5</h1>
            </b-carousel-slide>
          </b-carousel>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
