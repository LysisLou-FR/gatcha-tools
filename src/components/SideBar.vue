<template>
  <aside class="sidebar">
      <div class="up">
          <div class="logo-wrapper">
              <img alt="Logo Dislyte" src="../assets/logo-dislyte.svg" class="logo">
          </div>
          <nav class="main-nav">
              <ul class="">
                  <li class="is-active">Dashboard</li>
              </ul>
              <div class="divider" role="separator">
                  <span class="divider-wrapper css-1mjhz9d">
                      <p class="divider-label">Tools</p>
                  </span>
              </div>
              <ul class="">
                  <li>Tool name 01</li>
                  <li>Tool name 02</li>
                  <li>Tool name 03</li>
              </ul>
              <div class="divider" role="separator">
                  <span class="divider-wrapper css-1mjhz9d">
                      <p class="divider-label">Liens utiles</p>
                  </span>
              </div>
              <ul class="">
                  <li>Lien externe 01</li>
                  <li>Lien externe 02</li>
                  <li>Lien externe 03</li>
              </ul>
          </nav>
      </div>
      <div class="down">
            <div class="avatar">
                <p class="avatar-img">
                    <img alt="Avatar Lou" src="../assets/avatar-lou.svg">
                </p>
                <p class="avatar-infos">
                    <span class="name">Glou</span>
                    <span class="role">Dev. Front UI/UX</span>
                </p>
            </div>
      </div>
  </aside>
</template>

<script>
export default {
  name: 'SideBar',
  props: {
    msg: String
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/css/variables.scss';
.sidebar {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 30rem;
    background: linear-gradient(180deg, #191933 70%, #111122 100%);
    .logo-wrapper {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 1rem;
        .logo {
            max-width: 180px;
        }
    }
    .main-nav {
        margin: 2rem 0;
        ul {
            padding: 0;
            margin: 0;
            width: 90%;
            li {
                display: flex;
                align-items: center;
                color: rgba(231, 227, 252, 0.8);
                padding: 1.2rem 1.2rem 1.2rem 10%;
                border-radius: 0 0 14px 0;
                cursor: pointer;
                transition: all 0.2s ease;
                &:hover {
                    background-color: rgba(0,0,0,0.25);
                }
                &.is-active {
                    color: $base-dark;
                    background: $shimmer;
                    font-weight: 700;
                    &::before {
                        background-color: $base-dark;
                    }
                }
                &::before {
                    content: '';
                    opacity: 0.6;
                    width: 6px;
                    height: 6px;
                    background-color: rgba(231, 227, 252, 0.8);
                    border-radius: 100px;
                    margin-right: 1rem;
                }
            }
        }
    }
    .divider {
        flex-shrink: 0;
        display: flex;
        white-space: nowrap;
        text-align: center;
        border: 0;
        margin: 3.2rem 0 1.2rem 0;
        width: 90%;
        line-height: normal;
        text-transform: uppercase;
        &::before,
        &::after {
            position: relative;
            width: 100%;
            border-top: thin solid rgba(231, 227, 252, 0.12);
            top: 50%;
            content: "";
            transform: translateY(50%);
        }
        &::before {
            width: 10%;
        }
        &::after {
            width: 90%;
        }
        .divider-wrapper {
            padding-left: 0.625rem;
            padding-right: 0.625rem;
            font-size: 0.75rem;
            letter-spacing: 0.21px;
            .divider-label {
                margin: 0;
                overflow: hidden;
                text-overflow: ellipsis;
                white-space: nowrap;
                font-size: 1.2rem;
                line-height: normal;
                letter-spacing: 1px;
                text-transform: uppercase;
                color: rgba(231, 227, 252, 0.38);
                font-weight: 400;
            }
        }
    }
    .avatar {
        display: flex;
        align-items: center;
        background-color: rgba(255, 255, 255, 0.05);
        border-radius: 6px;
        padding: 0.4rem;
        margin: 2rem;
        .avatar-img {
            width: 5rem;
            margin: 0 1rem 0 0;
            border-radius: 100px;
            overflow: hidden;
            img {
                transform: scale(1);
            }
        }
        .avatar-infos {
            display: flex;
            flex-direction: column;
            gap: 0.2rem;
            color: #fff;
            letter-spacing: .86px;
            margin: 0;
            .name {
                font-size: 1.4rem;
                font-weight: 600;
            }
            .role {
                opacity: 0.6;
                font-size: 1.2rem;
            }
        }
    }
    .down {
        padding-bottom: 2rem;
    }
}
</style>
