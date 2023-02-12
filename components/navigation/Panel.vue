<template>
  <v-navigation-drawer
    v-model="drawer"
    app
    :width="width"
    :mobile-breakpoint="1041"
  >
    <div class="navPanel">
      <div>
        <div class="logo">
          <nuxt-link to="/"
            ><img src="/images/png/logo.png" alt=""
          /></nuxt-link>
        </div>
        <!-- nav  -->
        <!-- nav header  -->
        <v-list nav class="navList">
          <!-- dashboard  -->
          <nuxt-link to="/" class="topNav">
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="17"
                  height="14"
                  viewBox="0 0 17 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M2.5 11.5C2.5 11.7812 2.71875 12 3 12H15.5C16.0312 12 16.5 12.4688 16.5 13C16.5 13.5625 16.0312 14 15.5 14H3C1.59375 14 0.5 12.9062 0.5 11.5V1C0.5 0.46875 0.9375 0 1.5 0C2.03125 0 2.5 0.46875 2.5 1V11.5ZM11.1875 7.71875C10.8125 8.125 10.1562 8.125 9.78125 7.71875L8 5.9375L5.1875 8.71875C4.8125 9.125 4.15625 9.125 3.78125 8.71875C3.375 8.34375 3.375 7.6875 3.78125 7.3125L7.28125 3.8125C7.65625 3.40625 8.3125 3.40625 8.6875 3.8125L10.5 5.59375L13.7812 2.3125C14.1562 1.90625 14.8125 1.90625 15.1875 2.3125C15.5938 2.6875 15.5938 3.34375 15.1875 3.71875L11.1875 7.71875Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title"
                >Dashboard</v-list-item-title
              >
            </v-list-item>
          </nuxt-link>
          <!-- Schools  -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/school') }"
            to="/school"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="21"
                  height="17"
                  viewBox="0 0 21 17"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M11.0312 1.1875C10.7188 0.96875 10.2812 0.96875 9.9375 1.1875L5.6875 4H2C1.15625 4 0.5 4.6875 0.5 5.5V15.5C0.5 16.3438 1.15625 17 2 17H19C19.8125 17 20.5 16.3438 20.5 15.5V5.5C20.5 4.6875 19.8125 4 19 4H15.2812L11.0312 1.1875ZM8.5 14C8.5 12.9062 9.375 12 10.5 12C11.5938 12 12.5 12.9062 12.5 14V17H8.5V14ZM3.5 7H4.5C4.75 7 5 7.25 5 7.5V9.5C5 9.78125 4.75 10 4.5 10H3.5C3.21875 10 3 9.78125 3 9.5V7.5C3 7.25 3.21875 7 3.5 7ZM16 7.5C16 7.25 16.2188 7 16.5 7H17.5C17.75 7 18 7.25 18 7.5V9.5C18 9.78125 17.75 10 17.5 10H16.5C16.2188 10 16 9.78125 16 9.5V7.5ZM3.5 11H4.5C4.75 11 5 11.25 5 11.5V13.5C5 13.7812 4.75 14 4.5 14H3.5C3.21875 14 3 13.7812 3 13.5V11.5C3 11.25 3.21875 11 3.5 11ZM16 11.5C16 11.25 16.2188 11 16.5 11H17.5C17.75 11 18 11.25 18 11.5V13.5C18 13.7812 17.75 14 17.5 14H16.5C16.2188 14 16 13.7812 16 13.5V11.5ZM7.75 6.5C7.75 4.40625 10.0312 3.0625 11.875 4.125C12.7188 4.625 13.25 5.53125 13.25 6.5C13.25 8.625 10.9375 9.96875 9.125 8.90625C8.25 8.40625 7.75 7.5 7.75 6.5ZM10.5 5C10.2188 5 10 5.25 10 5.5V6.5C10 6.78125 10.2188 7 10.5 7H11.5C11.75 7 12 6.78125 12 6.5C12 6.25 11.75 6 11.5 6H11V5.5C11 5.25 10.75 5 10.5 5Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Schools</v-list-item-title>
            </v-list-item>
          </nuxt-link>
          <!-- student  -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/student') }"
            to="/student"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="15"
                  height="16"
                  viewBox="0 0 15 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M0.90625 2.5L1.125 2.5625V4.375C0.90625 4.5 0.75 4.75 0.75 5C0.75 5.28125 0.875 5.5 1.09375 5.625L0.59375 7.5625C0.53125 7.78125 0.65625 8 0.84375 8H2.125C2.3125 8 2.4375 7.78125 2.375 7.59375L1.875 5.625C2.09375 5.5 2.25 5.28125 2.25 5C2.25 4.75 2.09375 4.5 1.875 4.375V2.75L3.5 3.125V5C3.5 7.21875 5.28125 9 7.5 9C9.6875 9 11.4688 7.21875 11.4688 5L11.5 3.125L14.0625 2.5C14.625 2.375 14.625 1.65625 14.0625 1.53125L8.09375 0.09375C7.6875 0 7.28125 0 6.875 0.09375L0.90625 1.53125C0.34375 1.65625 0.34375 2.375 0.90625 2.5ZM10.7188 9.78125L7.5 13L4.25 9.78125C2.0625 10.5 0.5 12.5 0.5 14.9375C0.5 15.5312 0.96875 16 1.5625 16H13.4062C14 16 14.5 15.5312 14.5 14.9375C14.5 12.5 12.9062 10.5 10.7188 9.78125Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Students</v-list-item-title>
            </v-list-item>
          </nuxt-link>
          <!-- parents -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/parent') }"
            to="/parent"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="21"
                  height="16"
                  viewBox="0 0 21 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M10.4688 10C12.2812 10 13.7188 8.5625 13.7188 6.75C13.7188 4.96875 12.25 3.5 10.4688 3.5C8.6875 3.5 7.25 4.96875 7.25 6.75C7.21875 8.5625 8.6875 10 10.4688 10ZM12.0312 11H8.9375C6.46875 11 4.5 12.875 4.5 15.1875C4.5 15.6562 4.875 16 5.375 16H15.5938C16.0938 16 16.5 15.6562 16.5 15.1875C16.5 12.875 14.5 11 12.0312 11ZM16.5 5C17.875 5 19 3.90625 19 2.5C19 1.125 17.875 0 16.5 0C15.0938 0 14 1.125 14 2.5C14 3.90625 15.0938 5 16.5 5ZM6.21875 6.75C6.21875 6.59375 6.25 6.4375 6.28125 6.28125C5.9375 6.09375 5.5625 6 5.15625 6H3.25C1.71875 6 0.5 7.3125 0.5 8.9375C0.5 9.25 0.71875 9.5 1.03125 9.5H7.28125C6.625 8.78125 6.21875 7.8125 6.21875 6.75ZM4.5 5C5.875 5 7 3.90625 7 2.5C7 1.125 5.875 0 4.5 0C3.09375 0 2 1.125 2 2.5C2 3.90625 3.09375 5 4.5 5ZM17.7188 6H15.8125C15.4062 6 15.0312 6.125 14.6875 6.28125C14.6875 6.4375 14.7188 6.59375 14.7188 6.75C14.7188 7.8125 14.3438 8.78125 13.6875 9.5H19.9375C20.25 9.5 20.5 9.25 20.5 8.9375C20.5 7.3125 19.25 6 17.7188 6Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Parents</v-list-item-title>
            </v-list-item>
          </nuxt-link>
          <!-- teachers -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/teacher') }"
            to="/teacher"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="21"
                  height="16"
                  viewBox="0 0 21 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M19 0H7C6.15625 0 5.5 0.71875 5.5 1.5625V3C6.21875 3 6.90625 3.21875 7.46875 3.5625V2H18.4688V11H16.4688V9.5C16.4688 9.25 16.2188 9 15.9688 9H12.9688C12.6875 9 12.4688 9.25 12.4688 9.5V11H9.46875C10.1562 11.5312 10.6875 12.2188 11.0625 13H18.9688C19.8125 13 20.5 12.3125 20.5 11.4688V1.5625C20.5 0.71875 19.8125 0 19 0ZM5.5 10C7.15625 10 8.5 8.6875 8.5 7C8.5 5.34375 7.15625 4 5.5 4C3.8125 4 2.5 5.34375 2.5 7C2.5 8.65625 3.8125 10 5.5 10ZM6.5 11H4.5C2.28125 11 0.5 12.8125 0.5 15C0.5 15.5625 0.9375 16 1.5 16H9.5C10.0312 16 10.5 15.5625 10.5 15C10.5 12.8125 8.6875 11 6.5 11Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Teachers</v-list-item-title>
            </v-list-item>
          </nuxt-link>
          <!-- content -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/content') }"
            to="/content"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="13"
                  height="18"
                  viewBox="0 0 13 18"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M0.9375 1.09375C1.1875 0.96875 1.5 1 1.71875 1.1875L3 2.28125L4.25 1.1875C4.53125 0.96875 4.9375 0.96875 5.21875 1.1875L6.5 2.28125L7.75 1.1875C8.03125 0.96875 8.4375 0.96875 8.71875 1.1875L10 2.28125L11.25 1.1875C11.4688 1 11.7812 0.96875 12.0625 1.09375C12.3125 1.21875 12.5 1.46875 12.5 1.75V16.25C12.5 16.5625 12.3125 16.8125 12.0625 16.9375C11.7812 17.0625 11.4688 17.0312 11.25 16.8438L10 15.75L8.71875 16.8438C8.4375 17.0625 8.03125 17.0625 7.75 16.8438L6.5 15.75L5.21875 16.8438C4.9375 17.0625 4.53125 17.0625 4.25 16.8438L3 15.75L1.71875 16.8438C1.5 17.0312 1.1875 17.0625 0.9375 16.9375C0.65625 16.8125 0.5 16.5625 0.5 16.25V1.75C0.5 1.46875 0.65625 1.21875 0.9375 1.09375ZM3.5 5.5C3.21875 5.5 3 5.75 3 6C3 6.28125 3.21875 6.5 3.5 6.5H9.5C9.75 6.5 10 6.28125 10 6C10 5.75 9.75 5.5 9.5 5.5H3.5ZM3 12C3 12.2812 3.21875 12.5 3.5 12.5H9.5C9.75 12.5 10 12.2812 10 12C10 11.75 9.75 11.5 9.5 11.5H3.5C3.21875 11.5 3 11.75 3 12ZM3.5 8.5C3.21875 8.5 3 8.75 3 9C3 9.28125 3.21875 9.5 3.5 9.5H9.5C9.75 9.5 10 9.28125 10 9C10 8.75 9.75 8.5 9.5 8.5H3.5Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Content</v-list-item-title>
            </v-list-item>
          </nuxt-link>
          <!-- reports -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/reports') }"
            to="/reports"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="13"
                  height="16"
                  viewBox="0 0 13 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M8.5 0V4H12.5L8.5 0ZM7.5 4V0H2C1.15625 0 0.5 0.6875 0.5 1.5V14.5C0.5 15.3438 1.15625 16 2 16H11C11.8125 16 12.5 15.3438 12.5 14.5V5H8.5C7.9375 5 7.5 4.5625 7.5 4ZM2.5 2.25C2.5 2.125 2.59375 2 2.75 2H5.25C5.375 2 5.5 2.125 5.5 2.25V2.75C5.5 2.90625 5.375 3 5.25 3H2.75C2.59375 3 2.5 2.90625 2.5 2.75V2.25ZM2.5 4.25C2.5 4.125 2.59375 4 2.75 4H5.25C5.375 4 5.5 4.125 5.5 4.25V4.75C5.5 4.90625 5.375 5 5.25 5H2.75C2.59375 5 2.5 4.90625 2.5 4.75V4.25ZM10 12C10.25 12 10.5 12.25 10.5 12.5C10.5 12.7812 10.25 13 10 13H8.5C8 13 7.53125 12.7188 7.3125 12.2812C7.21875 12.0938 7.0625 12.0625 7 12.0625C6.90625 12.0625 6.75 12.0938 6.6875 12.25L6.4375 12.75C6.34375 12.9062 6.15625 13 6 13H5.9375C5.75 13 5.5625 12.875 5.5 12.6562L5 11.0938L4.65625 12.0938C4.46875 12.6562 3.96875 13 3.375 13H3C2.71875 13 2.5 12.7812 2.5 12.5C2.5 12.25 2.71875 12 3 12H3.375C3.53125 12 3.65625 11.9062 3.71875 11.7812L4.28125 10.0625C4.375 9.75 4.65625 9.5625 5 9.5625C5.3125 9.5625 5.59375 9.75 5.6875 10.0625L6.125 11.375C6.75 10.875 7.8125 11.0625 8.1875 11.8125C8.25 11.9375 8.375 12.0312 8.5 12.0312H10V12Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Reports</v-list-item-title>
            </v-list-item>
          </nuxt-link>
          <!-- subscriptions -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/subscription') }"
            to="/subscription"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="19"
                  height="16"
                  viewBox="0 0 19 16"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M0.59375 0.71875C0.8125 0.28125 1.25 0 1.75 0H15.25C15.7188 0 16.1562 0.28125 16.375 0.71875C16.5625 1.15625 16.5 1.6875 16.1875 2.0625L12.875 6.125C10.375 6.65625 8.46875 8.84375 8.46875 11.5C8.46875 12.375 8.6875 13.1875 9.03125 13.9062C8.96875 13.875 8.9375 13.8438 8.875 13.8125L6.875 12.3125C6.625 12.125 6.5 11.8438 6.5 11.5V9.03125L0.78125 2.0625C0.46875 1.6875 0.40625 1.15625 0.59375 0.71875ZM18.5 11.5C18.5 14 16.4688 16 14 16C11.5 16 9.46875 14 9.46875 11.5C9.46875 9.03125 11.5 7 14 7C16.4688 7 18.5 9.03125 18.5 11.5ZM13.4062 10.375C13.5625 10.3125 13.7812 10.25 13.9688 10.25C14.2188 10.2812 14.5 10.3125 14.8125 10.4062C15.0625 10.4688 15.3438 10.2812 15.4062 10.0312C15.4688 9.75 15.3125 9.5 15.0312 9.40625C14.875 9.375 14.6875 9.34375 14.5 9.3125V9C14.5 8.75 14.25 8.5 14 8.5C13.7188 8.5 13.5 8.75 13.5 9V9.3125C13.2812 9.34375 13.0938 9.40625 12.9062 9.5C12.5625 9.71875 12.1875 10.0938 12.25 10.6562C12.2812 11.1562 12.5938 11.4688 12.9062 11.625C13.1875 11.7812 13.5312 11.875 13.8125 11.9375L13.875 11.9688C14.1875 12.0625 14.4062 12.125 14.5938 12.2188C14.7188 12.3125 14.7188 12.375 14.7188 12.4062C14.75 12.4688 14.7188 12.5312 14.6875 12.5312C14.6875 12.5625 14.6562 12.625 14.5625 12.6562C14.4375 12.7188 14.2188 12.7812 14 12.75C13.6875 12.75 13.4375 12.6562 13.0625 12.5625C13 12.5312 12.9375 12.5 12.875 12.5C12.625 12.4062 12.3438 12.5625 12.25 12.8125C12.1875 13.0938 12.3125 13.375 12.5938 13.4375C12.625 13.4688 12.6875 13.4688 12.75 13.5C12.9688 13.5625 13.2188 13.6562 13.5 13.7188V14.0625C13.5 14.3438 13.7188 14.5625 14 14.5625C14.25 14.5625 14.5 14.3438 14.5 14.0625V13.7188C14.6875 13.6875 14.875 13.625 15.0625 13.5312C15.4375 13.3125 15.75 12.9375 15.7188 12.375C15.7188 11.875 15.4062 11.5625 15.0938 11.375C14.8125 11.1875 14.4375 11.0938 14.125 11C13.8125 10.9062 13.5625 10.8438 13.375 10.75C13.25 10.6562 13.25 10.625 13.25 10.625V10.5938C13.2188 10.5312 13.25 10.5312 13.25 10.5C13.2812 10.4688 13.3125 10.4375 13.4062 10.375Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title"
                >Subscriptions</v-list-item-title
              >
            </v-list-item>
          </nuxt-link>
          <!-- tickets -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/ticket') }"
            to="/ticket"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="13"
                  height="18"
                  viewBox="0 0 13 18"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M0.90625 1.09375C1.1875 0.96875 1.5 1 1.71875 1.1875L3 2.28125L4.25 1.1875C4.53125 0.96875 4.9375 0.96875 5.21875 1.1875L6.5 2.28125L7.75 1.1875C8.03125 0.96875 8.4375 0.96875 8.71875 1.1875L10 2.28125L11.25 1.1875C11.4688 1 11.7812 0.96875 12.0625 1.09375C12.3125 1.21875 12.5 1.46875 12.5 1.75V16.25C12.5 16.5625 12.3125 16.8125 12.0625 16.9375C11.7812 17.0625 11.4688 17.0312 11.25 16.8438L10 15.75L8.71875 16.8438C8.4375 17.0625 8.03125 17.0625 7.75 16.8438L6.5 15.75L5.21875 16.8438C4.9375 17.0625 4.53125 17.0625 4.25 16.8438L3 15.75L1.71875 16.8438C1.5 17.0312 1.1875 17.0625 0.90625 16.9375C0.65625 16.8125 0.5 16.5625 0.5 16.25V1.75C0.5 1.46875 0.65625 1.21875 0.90625 1.09375ZM3.5 5.5C3.21875 5.5 3 5.75 3 6C3 6.28125 3.21875 6.5 3.5 6.5H9.5C9.75 6.5 10 6.28125 10 6C10 5.75 9.75 5.5 9.5 5.5H3.5ZM3.5 12.5H9.5C9.75 12.5 10 12.2812 10 12C10 11.75 9.75 11.5 9.5 11.5H3.5C3.21875 11.5 3 11.75 3 12C3 12.2812 3.21875 12.5 3.5 12.5ZM3.5 8.5C3.21875 8.5 3 8.75 3 9C3 9.28125 3.21875 9.5 3.5 9.5H9.5C9.75 9.5 10 9.28125 10 9C10 8.75 9.75 8.5 9.5 8.5H3.5Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Tickets</v-list-item-title>
            </v-list-item>
          </nuxt-link>
          <!-- Settings -->
          <nuxt-link
            :class="{ still__active: $route.path.includes('/settings') }"
            to="/settings"
            class="topNav"
          >
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="17"
                  height="14"
                  viewBox="0 0 17 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M3.5 14H5.5C6.03125 14 6.5 13.5625 6.5 13C6.5 12.4688 6.03125 12 5.5 12H3.5C2.9375 12 2.5 11.5625 2.5 11V3C2.5 2.46875 2.9375 2 3.5 2H5.5C6.03125 2 6.5 1.5625 6.5 1C6.5 0.46875 6.03125 0 5.5 0H3.5C1.8125 0 0.5 1.34375 0.5 3V11C0.5 12.6562 1.8125 14 3.5 14ZM16.25 6.46875L11.75 2.21875C11.5312 2 11.2188 1.96875 10.9375 2.0625C10.6562 2.1875 10.5 2.46875 10.5 2.75V5H6.5C5.9375 5 5.5 5.46875 5.5 6V8C5.5 8.5625 5.9375 9 6.5 9H10.5V11.25C10.5 11.5312 10.6562 11.8125 10.9375 11.9375C11.2188 12.0312 11.5312 12 11.75 11.7812L16.25 7.53125C16.5625 7.28125 16.5625 6.75 16.25 6.46875Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Settings</v-list-item-title>
            </v-list-item>
          </nuxt-link>
          <!-- logout -->
          <nuxt-link to="#" class="topNav">
            <v-list-item class="dropdownList">
              <v-list-item-icon>
                <svg
                  width="17"
                  height="14"
                  viewBox="0 0 17 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M3.5 14H5.5C6.03125 14 6.5 13.5625 6.5 13C6.5 12.4688 6.03125 12 5.5 12H3.5C2.9375 12 2.5 11.5625 2.5 11V3C2.5 2.46875 2.9375 2 3.5 2H5.5C6.03125 2 6.5 1.5625 6.5 1C6.5 0.46875 6.03125 0 5.5 0H3.5C1.8125 0 0.5 1.34375 0.5 3V11C0.5 12.6562 1.8125 14 3.5 14ZM16.25 6.46875L11.75 2.21875C11.5312 2 11.2188 1.96875 10.9375 2.0625C10.6562 2.1875 10.5 2.46875 10.5 2.75V5H6.5C5.9375 5 5.5 5.46875 5.5 6V8C5.5 8.5625 5.9375 9 6.5 9H10.5V11.25C10.5 11.5312 10.6562 11.8125 10.9375 11.9375C11.2188 12.0312 11.5312 12 11.75 11.7812L16.25 7.53125C16.5625 7.28125 16.5625 6.75 16.25 6.46875Z"
                    fill="#666666"
                  />
                </svg>
              </v-list-item-icon>
              <v-list-item-title class="item_title">Log Out</v-list-item-title>
            </v-list-item>
          </nuxt-link>
        </v-list>
      </div>
      <div>
        <img
          v-show="
            $route.fullPath == '/' ||
            $route.path.includes('/parent') ||
            $route.path.includes('/ticket')
          "
          src="/images/png/panel/dashboard.png"
          alt=""
          class="panel__img"
        />
        <img
          v-show="$route.path.includes('/content')"
          src="/images/png/panel/content.png"
          alt=""
          class="panel__img"
        />
        <img
          v-show="
            $route.path.includes('/school') || $route.path.includes('/teacher')
          "
          src="/images/png/panel/school.png"
          alt=""
          class="panel__img"
        />
        <img
          v-show="
            $route.path.includes('/student') ||
            $route.path.includes('/subscription')
          "
          src="/images/png/panel/student.png"
          alt=""
          class="panel__img"
        />
        <p class="panel__copy">
          <svg
            width="16"
            height="16"
            viewBox="0 0 16 16"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M8 0C3.5625 0 0 3.59375 0 8C0 12.4375 3.5625 16 8 16C12.4062 16 16 12.4375 16 8C16 3.59375 12.4062 0 8 0ZM8 14.5C4.40625 14.5 1.5 11.5938 1.5 8C1.5 4.4375 4.40625 1.5 8 1.5C11.5625 1.5 14.5 4.4375 14.5 8C14.5 11.5938 11.5625 14.5 8 14.5ZM7.96875 5.5C8.625 5.5 9.25 5.78125 9.6875 6.25C10 6.53125 10.4688 6.53125 10.75 6.25C11.0625 5.96875 11.0625 5.5 10.7812 5.1875C10.0312 4.4375 9.03125 4.03125 7.96875 4.03125C6.90625 4.03125 5.90625 4.4375 5.15625 5.1875C3.59375 6.75 3.59375 9.28125 5.15625 10.8438C5.90625 11.5938 6.90625 12.0312 7.96875 12.0312C9.03125 12.0312 10.0312 11.5938 10.7812 10.8438C11.0625 10.5625 11.0625 10.0625 10.75 9.78125C10.4688 9.5 10 9.5 9.6875 9.78125C9.25 10.25 8.625 10.5312 7.96875 10.5312C7.3125 10.5312 6.6875 10.25 6.21875 9.78125C5.25 8.8125 5.25 7.21875 6.21875 6.25C6.6875 5.78125 7.3125 5.5 7.96875 5.5Z"
              fill="#383B4C"
            />
          </svg>
          <span>Chronicles Software Development Company</span>
        </p>
      </div>
    </div>
    <!-- -->
  </v-navigation-drawer>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      group: null,
      width: 257,
    };
  },
  methods: {
    showPanel() {
      this.drawer = !this.drawer;
    },
  },
};
</script>

<style lang="scss" scoped>
/* nav Panel styles  */

.navPanel {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 100%;
  height: 100%;
  gap: 23px;
  .logo {
    // width: 100%;
    height: 6.4rem;
    text-align: center;
    margin: 0 14px;
    display: flex;
    align-items: center;
    justify-content: center;
    grid-gap: 15px;
    padding-top: 21px;
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  .navList {
    padding: 0;
    margin-top: 37px;
    a {
      text-decoration: none;
      &.nuxt-link-active.nuxt-link-exact-active {
        .dropdownList {
          background-color: var(--nav-active-color);
          transition: all 0.2s ease-in-out;
          .item_title {
            color: var(--primary-color) !important;
            transition: all 0.2s ease-in-out;
          }
          svg {
            rect {
              stroke: var(--primary-color) !important;
              transition: all 0.2s ease-in-out;
            }
            path {
              fill: var(--primary-color) !important;
              transition: all 0.2s ease-in-out;
            }
          }
        }
      }
      &.still__active {
        .dropdownList {
          background-color: var(--nav-active-color);
          transition: all 0.2s ease-in-out;
          .item_title {
            color: var(--primary-color) !important;
            transition: all 0.2s ease-in-out;
          }
          svg {
            rect {
              stroke: var(--primary-color) !important;
              transition: all 0.2s ease-in-out;
            }
            path {
              fill: var(--primary-color) !important;
              transition: all 0.2s ease-in-out;
            }
          }
        }
      }
    }
    .dropdownList {
      cursor: pointer;
      padding-left: 30.5px;
      padding-top: 0;
      transition: all 0.2s ease-in-out;
      height: 3.6rem;
      border-radius: 0;
      margin-top: 7px;
      justify-content: space-between;
      &:hover {
        background-color: var(--nav-active-color);
        transition: all 0.2s ease-in-out;
        .item_title {
          color: var(--primary-color) !important;
          transition: all 0.2s ease-in-out;
        }
        svg {
          transition: all 0.2s ease-in-out;
          rect {
            stroke: var(--primary-color) !important;
            transition: all 0.2s ease-in-out;
          }
          path {
            fill: var(--primary-color) !important;
            transition: all 0.2s ease-in-out;
          }
        }
      }
      .item_title {
        font-size: var(--panel-font-size);
        font-weight: var(--font-medium);
        overflow: visible !important;
        color: var(--faded-color-second);
        transition: all 0.2s ease-in-out;
      }
      svg {
        width: 20px;
        height: 24px;
        transition: all 0.2s ease-in-out;
      }
    }
    .dropdownListWrapper {
      padding-left: 0;
      margin-bottom: 0;
      height: 2rem !important;
      .item_title {
        font-size: 1.2rem;
        font-weight: 700;
        overflow: visible !important;
        color: var(--nav-color);
        transition: all 0.2s ease-in-out;
      }
      svg {
        width: 20px;
        height: 20px;
        fill: var(--secondary-color);
        transition: all 0.2s ease-in-out;
      }
    }
  }

  .panel__copy {
    display: flex;
    align-items: center;
    gap: 4px;
    justify-content: center;
    span {
      font-weight: var(--font-light);
      font-size: var(--smaller-font-size);
      color: var(--nav-h3-color);
    }
  }
}

.panel__img {
  transition: 0.4s;
  animation: zoom-in-zoom-out 1s ease-in-out;
}

@keyframes zoom-in-zoom-out {
  0% {
    transform: scale(1, 1);
  }
  50% {
    transform: scale(1.08, 1.08);
  }
  100% {
    transform: scale(1, 1);
  }
}

.v-application--is-ltr .v-list-item__action:first-child,
.v-application--is-ltr .v-list-item__icon:first-child {
  margin-bottom: 0;
  margin-top: 12px;
  margin-right: 12px !important;
}

/* nav Panel styles end */
</style>