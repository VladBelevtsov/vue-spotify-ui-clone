<template>
  <div class="Navbar">
    <!-- Logo -->
    <div class="Navbar-logo">
      <img src="@/assets/image/logo.png"/>
    </div>
    <!-- Nav -->
    <nav class="Navbar-nav">
      <ul>
        <li class="active"><a href="#"><HomeIcon />Home</a></li>
        <li><a href="#"><SearchIcon />Search</a></li>
        <li><a href="#"><LibraryIcon />Your Library</a></li>
      </ul>
    </nav>
    <!-- Playlists -->
    <div class="Navbar-playlists">
      <h3>Playlists</h3>
      <ul class="mainList">
        <li><a href="#"><span><PlusIcon /></span> Create Playlist</a></li>
        <li class="liked"><a href="#"><span><HeartIcon /></span> Liked Songs</a></li>
      </ul>
      <ul class="followlist">
        <a href="#">1. Playlist</a>
        <a href="#">2. Playlist</a>
        <a href="#">3. Playlist</a>
        <a href="#">4. Playlist</a>
        <a href="#">5. Playlist</a>
        <a href="#">6. Playlist</a>
      </ul>
    </div>
    <!-- Install -->
    <div class="Navbar-install">
      <a href="#"><Download />Install App</a>
    </div>
  </div>
</template>

<script>
// Icons
import HomeIcon from '../assets/icons/HomeIcon'
import SearchIcon from '../assets/icons/SearchIcon'
import LibraryIcon from '../assets/icons/LibraryIcon'

import PlusIcon from '../assets/icons/PlusIcon'
import HeartIcon from '../assets/icons/HeartIcon'

import Download from '../assets/icons/Download'

export default {
  name: 'Navbar',
  components: {
    HomeIcon,
    SearchIcon,
    LibraryIcon,
    PlusIcon,
    HeartIcon,
    Download
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.Navbar {
  position: fixed !important;
  left: 0px;
  top: 0px;
  width: 230px;
  height: calc(100vh - 90px);
  background-color: #040404;
  position: relative;

  // Logo

  &-logo {
    padding: 25px;
    img {
      width: 130px;
      display: block;
    }
  }

  //Nav

  &-nav {
    ul {
      padding: 0 7px;

      .active {
        a {
          background-color: #282828;
          color: #fff;

          svg path {
            fill: #fff !important;
          }
        }
      }
      li {
        a {
          padding: 10px 15px;
          width: 100%;
          display: block;
          border-radius: 5px;
          display: flex;
          align-items: center;
          color: #B3B3B3;
          text-decoration: none;
          font-size: 13px;
          font-weight: 600;
          transition: .2s;

          &:hover {
            color: #fff;

            svg path {
              fill: #fff !important;
            }
          }

          svg {
            width: 20px;
            height: 20px;
            display: block;
            margin-right: 15px;

            path {
              fill: #B3B3B3 !important;
              transition: .2s;
            }
          }
        }
      }
    }
  }

  //Playlists

  &-playlists {
    padding: 0 20px;

    h3 {
      color: #B3B3B3;
      text-transform: uppercase;
      font-size: 13px;
      font-weight: 600;
      padding-top: 20px;
      padding-bottom: 15px;
    }
    .mainList {
      border-bottom: 1px solid #282828;
      padding-bottom: 5px;

      li {
        margin-bottom: 10px;

        &:hover {
          a {
            color: #fff;
            span {
              background: #fff;
            }
          }
        }

        a {
          display: flex;
          align-items: center;

          color: #B3B3B3;
          text-decoration: none;
          font-size: 13px;
          font-weight: 600;

          span {
            width: 34px;
            height: 34px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #B3B3B3;

            margin-right: 15px;

            svg {
              width: 15px;
              height: 15px;
              display: block;
              path {
                fill: #000 !important;
              }
            }
          }
        }
      }

      .liked {
        a {
          span {
            background: linear-gradient(130deg, rgba(51,10,171,1) 0%, rgba(136,165,152,1) 100%);
          }
        }

        &:hover {
          a {
            span {
              background: linear-gradient(130deg, rgba(71,13,244,1) 0%, rgba(192,233,217,1) 100%);
            }
          }
        }

        svg path {
          fill: #fff !important;
        }
      }
    }

    .followlist {
      display: flex;
      flex-direction: column;
      padding-top: 20px;

      a {
        color: #B3B3B3;
        font-size: 14px;
        font-weight: 400;
        text-decoration: none;
        cursor: default;
        margin-bottom: 10px;
      }
    }
  }

  // Download

  &-install {
    position: absolute;
    bottom: 0px;
    left: 0px;
    a {
      padding: 20px;
      display: flex;
      align-items: center;
      color: #B3B3B3;
      font-weight: 600;
      font-size: 14px;
      text-decoration: none;

      svg {
        width: 18px;
        height: 18px;
        margin-right: 5px;
        path {
          fill: #B3B3B3;
        }
      }
    }
  }
}
</style>
