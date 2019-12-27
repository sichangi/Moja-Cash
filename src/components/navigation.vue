<template>
  <nav>
    <div class="nav__inner">
      <div class="row justify-content-between align-items-center relative">
        <div class="col-3 col-sm-2 col-md-1 logo__item">
          <img alt="moja cash logo" src="/mlogo.svg">
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
  export default {
    name: 'navigation',
    data() {
      return {
        isMobile: false,
        mq: null,
        navOpen: false,
        navVisible: false,
        isScrolling: false,
        scrollTop: 0,
        navbarHeight: 200
      };
    },
    beforeMount() {
      window.addEventListener('scroll', () => {
        this.isScrolling = true;
      }, {passive: true});

      setInterval(() => {
        if (this.isScrolling) {
          this.hasScrolled();
          this.isScrolling = false;
        }
      }, 250);
    },
    mounted() {
      this.mq = window.matchMedia('(min-width: 560px)');
      this.checkIfMobile(this.mq);
      this.mq.addListener(this.checkIfMobile);
    },
    methods: {
      toggleNav() {
        this.navOpen = !this.navOpen;
      },
      checkIfMobile(mq) {
        this.isMobile = !mq.matches;
        return !mq.matches;
      },
      hasScrolled() {
        this.scrollTop = window.scrollY;
        this.navVisible = this.scrollTop >= this.navbarHeight;
      }
    },
    destroyed() {
      if (this.mq) {
        this.mq.removeListener(this.checkIfMobile);
      }
    }
  };
</script>

<style lang="scss">
  nav {
    align-items: center;
    background-color: rgba(255, 255, 255, 0);
    display: flex;
    height: 100px;
    transition: background-color .4s ease;
    width: 100%;

    .logo__item {
      height: 100%;
      width: 100%;

      .logo {
        align-items: center;
        display: flex;
        height: 60px;
        width: 100%;

        @media(max-width: 560px) {
          height: 36px;
        }

        img {
          max-height: 100%;
          max-width: 100%;
        }
      }
    }

    &.visible {
      background-color: rgba(255, 255, 255, 1);
      border-bottom: 1px solid #eaedf0;
    }
  }
</style>
