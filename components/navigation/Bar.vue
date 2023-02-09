<template>
  <v-app-bar
    color="#fff"
    app
    :height="60"
    flat
    elevate-on-scroll
    :elevation="2"
    class="top_nav_bar"
  >
    <div class="topBar">
      <div class="topBar__left-wing">
        <div class="topBar__left-left">
          <div class="hamburger">
            <v-app-bar-nav-icon
              @click="$emit('showNav')"
              color="var( --faded-color-second)"
            ></v-app-bar-nav-icon>
          </div>
          <div class="relative">
            <input type="text" placeholder="Enter a keyword.." />
            <div class="relative__icon absolute">
              <svg
                width="20"
                height="20"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M19.0538 18.0462C19.3321 18.3244 19.3321 18.7756 19.0538 19.0538C18.7756 19.3321 18.3244 19.3321 18.0462 19.0538L14.6262 15.6338C14.3479 15.3556 14.3479 14.9044 14.6262 14.6262C14.9044 14.3479 15.3556 14.3479 15.6338 14.6262L19.0538 18.0462ZM8.28999 15.8425C4.11886 15.8425 0.737488 12.4611 0.737488 8.28999C0.737488 4.11886 4.11886 0.737488 8.28999 0.737488C12.4611 0.737488 15.8425 4.11886 15.8425 8.28999C15.8425 12.4611 12.4611 15.8425 8.28999 15.8425ZM8.28999 14.4175C11.6741 14.4175 14.4175 11.6741 14.4175 8.28999C14.4175 4.90586 11.6741 2.16249 8.28999 2.16249C4.90586 2.16249 2.16249 4.90586 2.16249 8.28999C2.16249 11.6741 4.90586 14.4175 8.28999 14.4175ZM4.77499 7.71999C4.77499 7.98232 4.56232 8.19499 4.29999 8.19499C4.03765 8.19499 3.82499 7.98232 3.82499 7.71999C3.82499 5.56884 5.56884 3.82499 7.71999 3.82499C7.98232 3.82499 8.19499 4.03765 8.19499 4.29999C8.19499 4.56232 7.98232 4.77499 7.71999 4.77499C6.09351 4.77499 4.77499 6.09351 4.77499 7.71999Z"
                  fill="#D0C9D6"
                />
              </svg>
            </div>
          </div>
        </div>
        <div class="topBar__left-right">
          <div>
            <svg
              width="24"
              height="18"
              viewBox="0 0 24 18"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M23.5312 5.95312C22.4531 6.79688 21.0938 7.82812 16.3125 11.2969C15.375 12 13.6406 13.5469 12 13.5469C10.3125 13.5469 8.625 12 7.64062 11.2969C2.85938 7.82812 1.5 6.79688 0.421875 5.95312C0.234375 5.8125 0 5.95312 0 6.1875V15.75C0 17.0156 0.984375 18 2.25 18H21.75C22.9688 18 24 17.0156 24 15.75V6.1875C24 5.95312 23.7188 5.8125 23.5312 5.95312ZM12 12C13.0781 12.0469 14.625 10.6406 15.4219 10.0781C21.6562 5.57812 22.125 5.15625 23.5312 4.03125C23.8125 3.84375 24 3.51562 24 3.14062V2.25C24 1.03125 22.9688 0 21.75 0H2.25C0.984375 0 0 1.03125 0 2.25V3.14062C0 3.51562 0.140625 3.84375 0.421875 4.03125C1.82812 5.15625 2.29688 5.57812 8.53125 10.0781C9.32812 10.6406 10.875 12.0469 12 12Z"
                fill="#A1A1A1"
              />
            </svg>
          </div>
          <div>
            <svg
              width="22"
              height="25"
              viewBox="0 0 22 25"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10.5089 25C12.1495 25 13.462 23.6875 13.462 22H7.50888C7.50888 23.6875 8.82138 25 10.5089 25ZM20.587 18.0156C19.6964 17.0312 17.962 15.5781 17.962 10.75C17.962 7.14062 15.4308 4.23438 11.962 3.48438V2.5C11.962 1.70312 11.3058 1 10.5089 1C9.66513 1 9.00888 1.70312 9.00888 2.5V3.48438C5.54013 4.23438 3.00888 7.14062 3.00888 10.75C3.00888 15.5781 1.27451 17.0312 0.383883 18.0156C0.102633 18.2969 -0.0379922 18.6719 0.00888283 19C0.00888283 19.7969 0.571383 20.5 1.50888 20.5H19.462C20.3995 20.5 20.962 19.7969 21.0089 19C21.0089 18.6719 20.8683 18.2969 20.587 18.0156Z"
                fill="#A1A1A1"
              />
              <circle
                cx="16.5088"
                cy="4.5"
                r="4"
                fill="#DA3B3B"
                stroke="white"
              />
            </svg>
          </div>
        </div>
      </div>
    </div>

    <!-- user picture  -->

    <div class="control_area">
      <div class="userImage relative">
        <div class="absolute userImage__user-status">
          <svg
            width="17"
            height="17"
            viewBox="0 0 17 17"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <circle cx="8.5" cy="8.5" r="8.5" fill="#20C5A9" />
            <circle
              cx="8.5"
              cy="8.5"
              r="7.5"
              stroke="white"
              stroke-opacity="0.8"
              stroke-width="2"
            />
          </svg>
        </div>
      </div>
      <v-menu bottom nudge-bottom="32" v-model="userMenu" offset-y>
        <template v-slot:activator="{ on, attrs }">
          <div v-bind="attrs" v-on="on" class="control_area-menu">
            <div>
              <span class="control-area-menu-light">Hi, </span>
              <span>Oluwatosin K</span>
            </div>
            <svg
              :class="{ activeSvg: userMenu }"
              width="12"
              height="7"
              viewBox="0 0 12 7"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M1.08984 0C0.457031 0 0.140625 0.773438 0.597656 1.23047L5.09766 5.73047C5.37891 6.01172 5.83594 6.01172 6.11719 5.73047L10.6172 1.23047C11.0742 0.773438 10.7578 0 10.125 0H1.08984Z"
                fill="#666666"
              />
            </svg>
          </div>
        </template>
        <v-list>
          <v-list-item>
            <v-list-item-title>{{ 33 }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </div>
    <!-- -->
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      userMenu: false,
    };
  },
  mounted() {},
};
</script>

<style lang="scss" scoped>
.top_nav_bar {
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  padding-top: 0;
  padding-bottom: 0;
  .topBar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 100%;
    width: 100%;
    padding: 0 16px;

    .topBar__left-wing {
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-right: 1px solid var(--border-color);
      height: 100%;
      flex-grow: 1;
      .topBar__left-left {
        display: flex;
        align-items: center;
        gap: 31px;
        .relative {
          input {
            background-color: #fff;
            box-shadow: var(--box-shadow-input);
            border-radius: 6px;
            height: 4rem;
            min-width: 43.2rem;
            padding-left: 44px;
            font-size: var(--panel-font-size);
            &::placeholder {
              font-size: var(--panel-font-size);
              color: var(--placeholder-color);
              font-weight: var(--font-light);
            }
          }
          .relative__icon {
            left: 14px;
            top: 50%;
            transform: translateY(-40%);
          }
        }
      }
      .topBar__left-right {
        display: flex;
        align-items: center;
        gap: 38px;
        padding-right: 19px;
        padding-top: 5px;
        svg {
          cursor: pointer;
          width: 18px;
          height: 18px;
        }
      }
    }
  }
  .control_area {
    display: flex;
    align-items: center;
    gap: 15px;
    padding: 0 20px;
    .userImage {
      width: 4rem;
      height: 4rem;
      background-color: var(--secondary-color);
      background: url("/images/png/user.png");
      background-size: cover;
      background-repeat: no-repeat;
      background-position: top center;
      border-radius: 50%;
      border: 1px solid var(--border-color-second);
      // filter: drop-shadow(var(--box-shadow-user));
      // box-shadow: var(--box-shadow-user);
      .userImage__user-status {
        bottom: -7px;
        left: -4px;
        svg {
          width: 14px;
          height: 14px;
        }
      }
    }
    .control_area-menu {
      display: flex;
      align-items: center;
      min-width: 170px;
      grid-gap: 13px;
      justify-content: space-between;
      span {
        font-weight: var(--font-bold);
        color: var(--faded-color-second);
        font-size: var(--panel-font-size);
        text-transform: capitalize;
        &.control-area-menu-light {
          color: var(--faded-color-third);
        }
      }
      svg {
        transition: 0.4s;
        width: 15px;
        height: 15px;
        &.activeSvg {
          // transform: rotate(-180deg) translateY(-2px);
          // transition: 0.4s;
        }
      }
    }
  }
}
</style>