<template>
  <div class="Categories">
    <div class="Categories-head">
      <h3><a href="#">Shortcuts</a></h3>
      <a href="#">See all</a>
    </div>
    <div class="Categories-wrapp">
      <a v-for="item in items" :key="item.id" href="#" class="Categories-wrapp-card">
        <div class="Categories-wrapp-card-img">
          <img src="../assets/image/user.jpeg" alt="img">
          <a href="#" class="btn-play">
            <PlayIcon />
          </a>
        </div>
        <div class="Categories-wrapp-card-name">
          <h6>{{ item.name }}</h6>
        </div>
        <div class="Categories-wrapp-card-desc">
          <p>Some description of music</p>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
import PlayIcon from '../assets/icons/PlayIcon.vue'
export default {
  name: 'Categories',
  components: {
    PlayIcon
  },
  data() {
    return {
      items: [
        {
          id: 1,
          name: 'Daily Mix 1'
        },
        {
          id: 2,
          name: 'Daily Mix 2'
        },
        {
          id: 3,
          name: 'Daily Mix 3'
        },
        {
          id: 4,
          name: 'Daily Mix 4'
        },
        {
          id: 5,
          name: 'Daily Mix 5'
        },
        {
          id: 6,
          name: 'Daily Mix 6'
        },
        {
          id: 7,
          name: 'Daily Mix 1'
        },
        {
          id: 8,
          name: 'Daily Mix 2'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.Categories {

  &-head {
    display: flex;
    justify-content: space-between;
    align-items: center;

    a {
      color: #B3B3B3;
      font-weight: 600;
      font-size: 14px;
      text-decoration: none;

      &:hover {
        text-decoration: underline;
      }
    }
    
    h3 {

      &:hover a {
        text-decoration: underline;
      }

      a {
        color: #fff;
        text-decoration: none;
        font-weight: 700;
        font-size: 22px;
      }
    }
  }

  &-wrapp {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    padding-top: 20px;
    padding-bottom: 20px;

    &-card {
      padding: 18px;
      background-color: #171717;
      border-radius: 4px;
      max-width: 11.5%;
      transition: all .3s;
      text-decoration: none;

      &:hover {
        background-color: #282828;
      }

      &:hover .btn-play {
        bottom: 10px;
        opacity: 1;
      }

      &-img{
        position: relative;

        img {
          width: 100%;
          height: 100%;
          display: block;
          object-fit: cover;
          border-radius: 2px;
        }

        .btn-play {
          cursor: default;
          position: absolute;
          width: 40px;
          height: 40px;
          background-color: #1DB954;
          border-radius: 20px;
          display: flex;
          align-items: center;
          justify-content: center;
          transition: .3s;

          bottom: 0px;
          right: 10px;
          opacity: 0;

          svg {
            width: 40%;
            height: 40%;
            margin-left: 3px;
          }
        }
      }

      &-name {
        padding: 15px 0 7px;
        h6 {
          color: #fff;
          font-size: 14px;
          font-weight: 600;
        }
      }

      &-desc {
        p {
          color: #A8A8A8;
          font-weight: 500;
          font-size: 13px;
        }
      }
    }
  }
}
</style>
