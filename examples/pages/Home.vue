<template>
  <section class="wrapper">
    <div class="slogan">
      <h1>Vue-Pull-To</h1>
      <p>for Vue.js 2.0</p>
      <svg class="icon icon-face" aria-hidden="true">
        <use xlink:href="#icon-face-20"></use>
      </svg>
    </div>
    <pull-to class="scroller-view">
      <ul class="list">
        <li>
          <router-link href="/bounce-scroll">
            Bounce scroll
            <svg class="icon icon-arrow" aria-hidden="true">
              <use xlink:href="#icon-arrow-right"></use>
            </svg>
          </router-link>
        </li>
        <li>
          <router-link href="/simple-pullto-refresh">
            Simple pull to refresh
            <svg class="icon icon-arrow" aria-hidden="true">
              <use xlink:href="#icon-arrow-right"></use>
            </svg>
          </router-link>
        </li>
        <li>
          <router-link href="/simple-pullto-loadmore">
            Simple pull to load more
            <svg class="icon icon-arrow" aria-hidden="true">
              <use xlink:href="#icon-arrow-right"></use>
            </svg>
          </router-link>
        </li>
        <li>
          <router-link href="/infinite-scroll">
            Infinite scroll
            <svg class="icon icon-arrow" aria-hidden="true">
              <use xlink:href="#icon-arrow-right"></use>
            </svg>
          </router-link>
        </li>
        <li>
          <router-link href="/use-position-relative-scroll">
            Use Position Relative Scroll
            <svg class="icon icon-arrow" aria-hidden="true">
              <use xlink:href="#icon-arrow-right"></use>
            </svg>
          </router-link>
        </li>
      </ul>
    </pull-to>
  </section>
</template>

<style scoped rel="stylesheet/less" lang="less">
  .wrapper {
    display: flex;
    flex-direction: column;
    height: 100%;
  }

  .scroller-view {
    flex: 1;
  }

  .slogan {
    margin-top: 50px;

    p {
      margin-top: 8px;
      font-size: 16px;
      text-align: center;
    }

    .icon-face {
      margin-top: 15px;
      width: 100%;
      height: 100px;
    }
  }

  h1 {
    font-family: Candara,Calibri,Segoe,Segoe UI,Optima,Arial,sans-serif;
    text-align: center;
    font-size: 35px;
    font-weight: 500;
  }

  .list {
    margin-top: 30px;
    font-size: 16px;

    li:nth-child(even) {
      background: #eee;
    }

    li {
      padding-left: 15px;
      height: 50px;
      line-height: 50px;
      background: #fff;

      a {
        display: block;
        height: 100%;
      }

      .icon-arrow {
        display: inline-block;
        float: right;
        margin-right: 15px;
        height: 100%;
        width: 20px;
        color: #444;
      }
    }
  }
</style>

<script type="text/babel">
  import PullTo from '@';
  import RouterLink from '../components/RouterLink';

  export default {
    name: 'home',
    components: {
      RouterLink,
      PullTo
    }
  };
</script>
