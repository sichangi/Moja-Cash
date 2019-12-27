<template>
  <footer>
    <div class="container">
      <div class="row reverse-on-mobile justify-content-between">
        <div class="col-12 col-sm-3">
          <div class="logo">
            <img alt="moja cash logo" src="/mlogo.svg">
          </div>
          <div class="copy">&copy; 2019 Moja.cash, all rights reserved</div>
        </div>
        <div class="col-12 col-sm-2">
          <div class="socials">
            <div class="social">
              <svg>
                <use href="#twitter"/>
              </svg>
            </div>
            <div class="social">
              <svg>
                <use href="#instagram"/>
              </svg>
            </div>
          </div>
          <div class="links">
            <a class="link" href="/">About us</a>
            <a class="link" href="/">Contact us</a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
  export default {
    name: 'foot'
  };
</script>

<style lang="scss">
  footer {
    min-height: 10vh;
    padding: 3rem 0;

    .row {
      @media(min-width: 560px) {
        align-items: flex-end;
      }
    }

    .logo {
      height: 30px;
      margin-bottom: 1em;
      width: 100px;

      img {
        max-height: 100%;
        max-width: 100%;
      }
    }

    .copy {
    }

    .socials {
      align-items: center;
      display: flex;
      justify-content: flex-end;
      margin-bottom: 1em;

      @media(max-width: 560px) {
        justify-content: flex-start;
      }

      .social {
        border-radius: 50%;
        color: white;
        cursor: pointer;
        height: 30px;
        margin-left: 1em;
        margin-right: .6rem;
        padding: .2em;
        width: 30px;

        @media(max-width: 560px) {
          margin-left: 0;
          margin-right: 1em;
        }
      }
    }

    .links {
      text-align: right;

      @media(max-width: 560px) {
        margin-bottom: 3em;
        text-align: left;
      }

      .link {
        margin-left: 1em;

        @media(max-width: 560px) {
          margin-left: 0;
          margin-right: 1em;
        }
      }
    }
  }
</style>
