<template>
  <div class="slider__slide">
    <img class="album"
         :src="require(`@/assets/albums/${data.album}.webp`)"
         alt="album">
  </div>
</template>

<script>
export default {
  props: {
    data: Object
  },
  name: 'v-slider'
}
</script>

<style scoped lang="stylus">
.slider__slide {
  position relative
  border-radius 18px
  width 200px
  height 200px
  overflow hidden

  @media only screen and (max-width 376px) {
    & {
      width 170px
      height 170px
    }
  }

  .album {
    position absolute
    top 0
    left 0
    width 100%
    height 100%
  }
}

</style>
