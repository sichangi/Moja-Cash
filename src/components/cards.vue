<template>
  <div id="card-story" ref="bg">
  </div>
</template>

<script>
  export default {
    name: 'card-story',
    mounted() {
      const container = this.$refs.bg;
      const controller = new ScrollMagic.Controller();
      const Tween = new TimelineLite()
        .add(TweenLite.to(container, 1, {backgroundPositionX: '-480px', backgroundPositionY: '-240px'}));
      // .add(TweenLite.to(container, 1, {backgroundPositionX: '-480px', backgroundPositionY: '-240px'}))
      // .add(TweenLite.to(container, 1, {backgroundPositionX: '-480px', backgroundPositionY: '-240px'}))

      new ScrollMagic.Scene({triggerElement: '#card-story', triggerHook: 0.98, duration: 2000})
        .setTween(Tween).addTo(controller);
    }
  };
</script>

<style lang="scss">
  #card-story {
    background-image: url("/img/phone_card.svg");
    background-position: -150px -100px;
    background-repeat: no-repeat;
    height: 100%;
    overflow: hidden;
    position: relative;
    width: 100%;

    @media(max-width: 560px) {
      background-position: -150px -80px;
    }

    &:before {
      background-color: rgba(0, 0, 0, 0.4);
      content: "";
      height: 100%;
      left: 0;
      position: absolute;
      top: 0;
      width: 100%;
    }

  }
</style>
