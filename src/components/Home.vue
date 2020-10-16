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

      <div class="Home-header-wrapp-categories">
        <div class="Home-header-wrapp-categories-head">
          <h3><a href="#">Shortcuts</a></h3>
          <a href="#">See all</a>
        </div>
        <div class="Home-header-wrapp-categories-wrapp">
          <a v-for="shortcut in shortcuts" :key="shortcut.name" href="#" class="Home-header-wrapp-categories-wrapp-card">
            <div class="Home-header-wrapp-categories-wrapp-card-img">
              <img :src="shortcut.img" alt="img">
              <a href="#" class="btn-play">
                <PlayIcon />
              </a>
            </div>
            <div class="Home-header-wrapp-categories-wrapp-card-name">
              <h6>{{ shortcut.name }}</h6>
            </div>
            <div class="Home-header-wrapp-categories-wrapp-card-desc">
              <p>Some description of music</p>
            </div>
          </a>
        </div>
      </div>
      
      <div class="Home-header-wrapp-categories">
        <div class="Home-header-wrapp-categories-head">
          <h3><a href="#">Made for Vlad Bielievtsov</a>
            <span>Get better recommendations the more you listen.</span>
          </h3>
          <a href="#">See all</a>
        </div>
        <div class="Home-header-wrapp-categories-wrapp">
          <a v-for="recommendations in MadeFor" :key="recommendations.name" href="#" class="Home-header-wrapp-categories-wrapp-card">
            <div class="Home-header-wrapp-categories-wrapp-card-img">
              <img :src="recommendations.img" alt="img">
              <a href="#" class="btn-play">
                <PlayIcon />
              </a>
            </div>
            <div class="Home-header-wrapp-categories-wrapp-card-name">
              <h6>{{ recommendations.name }}</h6>
            </div>
            <div class="Home-header-wrapp-categories-wrapp-card-desc">
              <p>Some description of music</p>
            </div>
          </a>
        </div>
      </div>

      <div class="Home-header-wrapp-categories">
        <div class="Home-header-wrapp-categories-head">
          <h3><a href="#">Shows to try</a>
            <span>Podcasts we think you'll get hooked on.</span>
          </h3>
          <a href="#">See all</a>
        </div>
        <div class="Home-header-wrapp-categories-wrapp">
          <a v-for="trying in Try" :key="trying.name" href="#" class="Home-header-wrapp-categories-wrapp-card">
            <div class="Home-header-wrapp-categories-wrapp-card-img">
              <img :src="trying.img" alt="img">
              <a href="#" class="btn-play">
                <PlayIcon />
              </a>
            </div>
            <div class="Home-header-wrapp-categories-wrapp-card-name">
              <h6>{{ trying.name }}</h6>
            </div>
            <div class="Home-header-wrapp-categories-wrapp-card-desc">
              <p>Some description of music</p>
            </div>
          </a>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
// Icons
import ArrowLeftIcon from '../assets/icons/ArrowLeftIcon.vue'
import ArrowDownIcon from '../assets/icons/ArrowDownIcon.vue'
import PlayIcon from '../assets/icons/PlayIcon.vue'

export default {
  name: 'Home',
  props: ['item'],
  components: {
    ArrowLeftIcon,
    ArrowDownIcon,
    PlayIcon
  },
  data() {
    return {
      shortcuts: [
        {name: 'Daily shorts 1', img: 'https://images.unsplash.com/photo-1513829596324-4bb2800c5efb?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily shorts 2', img: 'https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily shorts 3', img: 'https://images.unsplash.com/photo-1494232410401-ad00d5433cfa?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily shorts 4', img: 'https://images.unsplash.com/photo-1487180144351-b8472da7d491?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1352&q=80'},
        {name: 'Daily shorts 5', img: 'https://images.unsplash.com/photo-1514320291840-2e0a9bf2a9ae?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily shorts 6', img: 'https://images.unsplash.com/photo-1508700115892-45ecd05ae2ad?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily shorts 7', img: 'https://images.unsplash.com/photo-1470225620780-dba8ba36b745?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily shorts 8', img: 'https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'}
      ],
      MadeFor: [
        {name: 'Daily Mix 1', img: 'https://images.unsplash.com/photo-1511367734837-f2956f0d8020?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1294&q=80'},
        {name: 'Daily Mix 2', img: 'https://images.unsplash.com/photo-1483412033650-1015ddeb83d1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1353&q=80'},
        {name: 'Daily Mix 3', img: 'https://images.unsplash.com/photo-1477233534935-f5e6fe7c1159?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily Mix 4', img: 'https://images.unsplash.com/photo-1508186736123-44a5fcb36f9f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'},
        {name: 'Daily Mix 5', img: 'https://images.unsplash.com/photo-1504898770365-14faca6a7320?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=702&q=80'},
        {name: 'Daily Mix 6', img: 'https://images.unsplash.com/photo-1502773860571-211a597d6e4b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily Mix 7', img: 'https://images.unsplash.com/photo-1468817814611-b7edf94b5d60?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'},
        {name: 'Daily Mix 8', img: 'https://images.unsplash.com/photo-1538819137474-ffa0ee381af6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=676&q=80'}
      ],
      Try: [
        {name: 'Daily Try 1', img: 'https://images.unsplash.com/photo-1511735111819-9a3f7709049c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1267&q=80'},
        {name: 'Daily Try 2', img: 'https://images.unsplash.com/photo-1466428996289-fb355538da1b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily Try 3', img: 'https://images.unsplash.com/photo-1489641493513-ba4ee84ccea9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjF9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily Try 4', img: 'https://images.unsplash.com/photo-1483032469466-b937c425697b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily Try 5', img: 'https://images.unsplash.com/photo-1471478331149-c72f17e33c73?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1349&q=80'},
        {name: 'Daily Try 6', img: 'https://images.unsplash.com/photo-1433622070098-754fdf81c929?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'},
        {name: 'Daily Try 7', img: 'https://images.unsplash.com/photo-1466232373731-46205f0b668e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'},
        {name: 'Daily Try 8', img: 'https://images.unsplash.com/photo-1464676015774-81a71be95929?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80'}
      ]
    }
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

    &-wrapp {
      &-categories {
        padding-top: 20px;
        &-head {
          display: flex;
          justify-content: space-between;
          align-items: center;

          a {
            color: #B3B3B3;
            font-weight: 600;
            font-size: 12px;
            text-decoration: none;
            text-transform: uppercase;

            &:hover {
              text-decoration: underline;
            }
          }
          
          h3 {
            display: flex;
            flex-direction: column;

            span {
              color: #A7A7A7;
              font-weight: 500;
              font-size: 12px;
            }

            &:hover a {
              text-decoration: underline;
            }

            a {
              color: #fff;
              text-decoration: none;
              font-weight: 700;
              font-size: 22px;
              text-transform: none;
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
                min-height: 150px;
                max-height: 150px;
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
    }
  }
}
</style>
