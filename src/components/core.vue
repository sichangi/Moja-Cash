<template>
  <div id="core">
    <header>
      <div class="container">
        <div class="row reverse-on-mobile justify-content-center">
          <div class="col-12 col-sm-8 col-md-4 col-lg-5 justify-content-center flex dir-column ">
            <h1>Spend together <br>with one wallet</h1>
            <!--<h1>A unified wallet <br>under your control</h1>-->
            <div class="cta">
              <span>
                <svg><use xlink:href="#arrow-forward"/></svg>
              </span> Sign up for early access
            </div>
          </div>
          <div class="col-12 col-sm-4 col-md-8 col-lg-7">
            <div class="img">
              <svg>
                <use xlink:href="#header-img"/>
              </svg>
            </div>
          </div>
        </div>
        <div class="row description">
          <div class="col-12 col-sm-7 col-md-4">
            <p>A multi-user payment solution that offers an easy and intuitive way for everyone to manage, send and
              control family or group spending from one wallet.</p>
          </div>
        </div>
      </div>
    </header>
    <section id="story-mode">
      <div class="container alt">
        <div class="row row-reverse-on-desktop">
          <div class="col-12 col-md-offset-1 col-md-7 mobile-sticky">
            <div class="anim">
              <story/>
            </div>
          </div>
          <div class="meta-mobile"></div>
          <div class="col-12 col-md-4">
            <div class="story">
              <div class="wrapper">
                <div class="inner-container" ref="story_wrapper">
                  <div class="page-1">
                    <h3>Easily top up and send funds to individual wallets from your mobile platform of choice.</h3>
                    <div class="detail">Moja.Cash provides support for MPESA, Airtel Money or Equitel with more
                      integrations on the way
                    </div>
                    <div class="cta"><span><svg><use xlink:href="#arrow-forward"/></svg></span> Sign up for early
                      access
                    </div>
                  </div>
                  <div class="page-2">
                    <h3>Securely & conveniently withdraw funds from your mobile or moja cash card</h3>
                    <div class="detail">Easily create limits on amounts used by specific wallet holders and the goods
                      purchased.
                    </div>
                    <div class="cta"><span><svg><use xlink:href="#arrow-forward"/></svg></span> Sign up for early
                      access
                    </div>
                  </div>
                  <div class="page-3">
                    <h3>Receive real time notifications and monitor spending from the comfort of your phone</h3>
                    <div class="detail">Get real time insight and stats on spending activities across your wallets
                      users.
                    </div>
                    <div class="cta"><span><svg><use xlink:href="#arrow-forward"/></svg></span> Sign up for early
                      access
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="post">
      <div class="container">
        <div class="row">
          <div class="col-12 col-md-5">
            <div class="insight-bar">
              <img alt="app" src="/img/phone.png">
            </div>
          </div>
          <div class="col-12 col-md-5 col-md-offset-1">
            <div class="minor-title">OUR INSIGHT</div>
            <h3 class="title">Inspired by the need for a better means to handling personal finances, we built Moja cash
              knowing; What you measure, you can improve.</h3>
            <p class="description">Sed id dignissim neque, non placerat elit. Pellentesque rutrum, nunc vel elementum
              imperdiet, nibh massa viverra ante, sed commodo mi libero vel metus.</p>
          </div>
        </div>
      </div>
    </section>
    <section id="app-card">
      <div class="bg">
        <cards/>
      </div>
      <div class="container">
        <div class="row">
          <div class="col-12 col-sm-8 col-md-4">
            <h3>Conveniently make payments by card or mobile from anywhere, anytime.</h3>
            <p>Pay via the Moja.cash app or with our secure, NFC enabled credit cards, powered by MasterCard.</p>
            <div class="cta"><span><svg><use xlink:href="#arrow-forward"/></svg></span> Sign up for early access
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="know-cta">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-12 col-sm-8 col-md-6">
            <h3>Stay in the know</h3>
            <p>Get a notification & monetary offer as soon as we launch our beta version of the service as well as the
              initial release in the coming future.</p>
            <button class="cta-btn">Request access</button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
  import Story from './story';
  import Cards from './cards';

  export default {
    name: 'core',
    components: {Cards, Story}
  };
</script>

<style lang="scss">
  #core {
    svg {
      max-height: 100%;
      max-width: 100%;
    }

    .cta {
      align-items: center;
      cursor: pointer;
      display: flex;
      padding: 2em 0;

      span {
        background-color: #4DAEC2;
        border-radius: 50%;
        cursor: pointer;
        display: block;
        height: 40px;
        margin-right: 1em;
        padding: .8em;
        position: relative;
        width: 40px;

        &:before {
          background-color: rgba(0, 0, 0, 0.2);
          border-radius: 50%;
          bottom: 0;
          content: "";
          height: 0;
          left: 0;
          margin: auto;
          position: absolute;
          right: 0;
          top: 0;
          transition: all .2s ease;
          width: 0;
        }

        svg {
          position: relative;

          use {
            height: 100%;
            width: 100%;
          }
        }
      }

      &:hover span:before {
        height: 82%;
        width: 82%;
      }
    }

    header {
      align-items: center;
      display: flex;
      height: 100vh;
      min-height: 800px;
      position: relative;

      @media(max-width: 560px) {
        min-height: 680px;
      }

      .img {
        height: 50vh;
        width: 100%;

        @media(max-width: 560px) {
          height: 36vh;
          margin-bottom: 1rem;
        }

        svg {
          height: 100%;
          width: 100%;
        }
      }

      .description {
        bottom: 3rem;
        font-size: 1vw;
        font-weight: 400;
        max-width: var(--container-max);
        position: absolute;
        width: var(--container-width);

        @media(max-width: 1440px) {
          font-size: 1.2vw;
        }

        @media(max-width: 770px) {
          font-size: 2.2vw;
        }

        @media(max-width: 560px) {
          font-size: 4vw;

          /*line-height: 1.2em;*/
        }
      }
    }

    section {
      background-color: #343434;
      /*min-height: 800px;*/
      min-height: 100vh;
    }

    section#story-mode {
      .story {
        position: relative;
        @media(max-width: 770px) {
          flex-direction: row;
        }

        .wrapper {
          min-height: 280vh;
          min-width: 100%;

          @media(max-width: 770px) {
            min-height: unset;
            /*overflow-x: auto;*/
            /*display: inline-flex;*/
          }

          .inner-container {
            @media screen and (max-width: 560px) {
              display: inherit;
              width: auto;
            }
          }

        }

        [class*="page-"] {
          display: flex;
          flex-direction: column;
          flex-grow: 1;
          height: 90vh;
          justify-content: center;

          @media(max-width: 770px) {
            display: inline-flex;
            float: left;
            height: 45vh;
            min-width: 100%;
            padding-right: .5em;

            .cta {
              display: none;
            }
          }

          h3 {
            font-size: 1.8vw;
            font-weight: 500;
            line-height: 1.4em;

            @media (max-width: 1440px) {
              font-size: 1.8vw;
            }

            @media (max-width: 770px) {
              font-size: 4vw;
            }

            @media (max-width: 560px) {
              font-size: 6.2vw;
            }
          }

          .detail {
            font-size: .8vw;
            line-height: 1.6em;
            padding: 1em 0;

            @media (max-width: 1440px) {
              font-size: 1vw;
            }

            @media (max-width: 770px) {
              font-size: 2.4vw;
            }

            @media (max-width: 560px) {
              font-size: 3.6vw;
            }
          }
        }

        .page-1 {
        }

        .page-2 {
          span {
            background-color: #e45f4d;
          }
        }

        .page-3 {
          span {
            background-color: #20c997;
          }
        }

        .mobile-nav {
          align-items: center;
          bottom: 2em;
          display: flex;
          height: 24px;
          justify-content: space-between;
          position: absolute;
          right: 0;
          width: 80px;

          @media(min-width: 770px) {
            display: none;
          }

          [class*="-nav"] {
            border: 1px solid #929292;
            border-radius: 50%;
            cursor: pointer;
            height: 30px;
            padding: .5em;
            width: 30px;
          }
        }
      }

      @media(max-width: 760px) {
        .mobile-sticky {
          position: -webkit-sticky;
          position: sticky;
          top: 0;
          z-index: 19;
        }
      }

      .anim {
        backface-visibility: hidden;
        height: 100vh;
        position: -webkit-sticky;
        position: sticky;
        /*background-color: aliceblue;*/
        top: 0;
        transition: width .3s ease-in-out;

        @media screen and (min-width: 560px) {
          width: 0;
        }

        &.in {
          @media screen and (min-width: 560px) {
            width: 100%;
          }
        }

        @media(max-width: 770px) {
          height: 55vh;
          /*max-width: 100vw;*/
          margin-left: calc(-1 * (100vw - var(--container-width)) / 2);
          margin-right: calc(-1 * (100vw - var(--container-width)) / 2);
        }

        @media (max-width: 560px) {
          margin: 0 -0.8rem;
        }
      }
    }

    section#post {
      align-items: center;
      background-color: white;
      color: #393838;
      display: flex;
      font-weight: bold;
      min-height: 90vh;
      padding: 3rem 0;

      .insight-bar {
        align-items: flex-end;
        background-color: #393838;
        display: flex;
        height: 100%;
        margin-top: 2.8rem;
        position: relative;

        img {
          bottom: 2rem;
          height: 150%;
          position: absolute;
          right: 12vw;
        }

        @media(max-width: 1590px) {
          margin-left: calc((15vw / 2) * -1);
        }

        @media(min-width: 1591px) {
          margin-left: calc((100vw - 1366px) / 2 * -1);
        }

        @media(max-width: 560px) {
          height: 180px;
          margin-bottom: 2rem;
          margin-top: 22vh;

          img {
            right: 44vw;
          }
        }
      }

      .minor-title {
        font-weight: bold;
        margin-bottom: 1em;

        @media (max-width: 560px) {
          font-size: 3.4vw;
        }
      }

      h3.title {
        font-weight: bold;

        @media (min-width: 770px) {
          font-size: 1.8vw;
        }

        @media (max-width: 560px) {
          font-size: 5.2vw;
        }
      }

      .description {
        font-weight: 600;

        @media (min-width: 770px) {
          font-size: 1vw;
        }
      }
    }

    section#app-card {
      align-items: center;
      display: flex;
      min-height: 75vh;
      position: relative;

      .bg {
        height: 100%;
        left: 0;
        position: absolute;
        top: 0;
        width: 100%;
      }

      .container {
        position: relative;

        p {
          font-size: 1.1em;
        }

        .cta {
          padding: 1em 0;
        }
      }
    }

    section#know-cta {
      background-color: black;
      min-height: 32vh;
      padding: 4rem 0;
      text-align: center;

      p {
        font-size: 1.1em;
      }

      .cta-btn {
        margin: 1em 0;

        @media(min-width: 560px) {
          max-width: 180px;
        }
      }
    }
  }
</style>
