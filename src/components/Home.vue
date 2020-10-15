<template>
  <div class="Home">
    <div class="Home-header">
      <div class="Home-header-nav">
        <button class="prev"><ArrowLeftIcon /></button>
        <button class="next"><ArrowLeftIcon /></button>
      </div>
      <div class="Home-header-right">
        <div class="Home-header-right-upgrade">
          <a href="#">Upgrade</a>
        </div>
        <div class="Home-header-right-user">
          <div class="Home-header-right-user-img">
            <img src="../assets/image/user.jpeg" alt="user name">
          </div>
          <div class="Home-header-right-user-name">
            User name
          </div>
          <div class="Home-header-right-user-more">
            <ArrowDownIcon />
          </div>
        </div>
      </div>
    </div>
    <div class="Home-header-wrapp">

      <Categories />
      <Categories />
      <Categories />
    </div>
  </div>
</template>

<script>
// Icons
import ArrowLeftIcon from '../assets/icons/ArrowLeftIcon.vue'
import ArrowDownIcon from '../assets/icons/ArrowDownIcon.vue'

import Categories from '../components/Categories'

export default {
  name: 'Home',
  components: {
    ArrowLeftIcon,
    ArrowDownIcon,
    Categories
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.Home {
  background-color: #121212;
  min-height: calc(100vh - 90px);
  padding: 20px 35px 35px 35px;

  &-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 20px;

    &-nav {
      display: flex;

      button {
        background-color: #0A0A0A;
        border: 0;
        outline: 0;
        border-radius: 50px;
        display: block;
        padding: 8px;
        cursor: not-allowed;
        margin-right: 15px;

        svg {
          display: block;
          width: 14px;
          height: 14px;
        }
      }

      .next {
        svg {
          transform: rotate(180deg);
        }
      }
    }

    &-right {
      display: flex;
      align-items: center;

      &-upgrade {
        a {
          width: 140px;
          height: 35px;
          display: block;
          background-color: #050505;
          border-radius: 50px;
          display: flex;
          align-items: center;
          justify-content: center;
          border: 1px solid #F8F8F8;
          color: #F8F8F8;
          text-decoration: none;
          text-transform: uppercase;
          font-weight: 600;
          font-size: 12px;
          transition: .1s;

          &:hover {
            transform: scale(1.05);
          }
        }
      }

      &-user {
        display: flex;
        align-items: center;
        background-color: #050505;
        border-radius: 50px;
        padding: 3px;
        cursor: pointer;
        margin-left: 15px;

        &:hover {
          background-color: #282828;
        }

        &-img {
          img {
            width: 29px;
            height: 29px;
            object-fit: cover;
            display: block;
            border-radius: 50px;
          }
        }

        &-name {
          color: #F8F8F8;
          font-size: 13px;
          font-weight: 600;
          padding: 0 10px;
        }

        &-more {
          padding-right: 10px;

          svg {
            width: 11px;
            height: 11px;
          }
        }
      }
    }
  }
}
</style>
