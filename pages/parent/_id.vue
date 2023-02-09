<template>
  <div>
    <section id="pageBody">
      <v-row class="content_row">
        <!-- title  -->
        <div style="padding-right: 24px" class="col-12 header_wrapper">
          <div style="display: flex; align-items: center; grid-gap: 35px">
            <div onclick="history.back()" class="header_wrapper-back">
              <svg
                width="25"
                height="16"
                viewBox="0 0 25 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M1.42188 6.96875L7.42188 0.96875C7.98438 0.359375 8.96875 0.359375 9.53125 0.96875C10.1406 1.53125 10.1406 2.51562 9.53125 3.07812L6.10938 6.5H23.5C24.2969 6.5 25 7.20312 25 8C25 8.84375 24.2969 9.5 23.5 9.5H6.10938L9.53125 12.9688C10.1406 13.5312 10.1406 14.5156 9.53125 15.0781C8.96875 15.6875 7.98438 15.6875 7.42188 15.0781L1.42188 9.07812C0.8125 8.51562 0.8125 7.53125 1.42188 6.96875Z"
                  fill="#F88B2A"
                />
              </svg>

              <span>back</span>
            </div>
            <header>Kolawole Benjamin</header>
          </div>
          <div class="header_wrapper-buttons">
            <v-btn
              outlined
              color="var(--primary-color)"
              class="button button--header button--outlined"
            >
              <svg
                width="13"
                height="15"
                viewBox="0 0 13 15"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M6.5 14.75C7.45703 14.75 8.22266 13.9844 8.22266 13H4.75C4.75 13.9844 5.51562 14.75 6.5 14.75ZM12.3789 10.6758C11.8594 10.1016 10.8477 9.25391 10.8477 6.4375C10.8477 4.33203 9.37109 2.63672 7.34766 2.19922V1.625C7.34766 1.16016 6.96484 0.75 6.5 0.75C6.00781 0.75 5.625 1.16016 5.625 1.625V2.19922C3.60156 2.63672 2.125 4.33203 2.125 6.4375C2.125 9.25391 1.11328 10.1016 0.59375 10.6758C0.429688 10.8398 0.347656 11.0586 0.375 11.25C0.375 11.7148 0.703125 12.125 1.25 12.125H11.7227C12.2695 12.125 12.5977 11.7148 12.625 11.25C12.625 11.0586 12.543 10.8398 12.3789 10.6758Z"
                  fill="#F88B2A"
                />
              </svg>

              <span>NOTIFY payment </span>
            </v-btn>
            <v-btn color="var(--primary-color)" class="button button--header">
              <svg
                width="17"
                height="15"
                viewBox="0 0 17 15"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M11.6172 3.04688C11.5078 2.9375 11.3438 2.9375 11.2344 3.04688L5.27344 9.00781L5 11.5508C4.94531 11.8789 5.24609 12.1797 5.57422 12.125L8.11719 11.8516L14.0781 5.89062C14.1875 5.78125 14.1875 5.61719 14.0781 5.50781L11.6172 3.04688ZM16.0469 2.41797L14.707 1.07812C14.2969 0.667969 13.6133 0.667969 13.2031 1.07812L12.2461 2.03516C12.1367 2.14453 12.1367 2.30859 12.2461 2.41797L14.707 4.87891C14.8164 4.98828 14.9805 4.98828 15.0898 4.87891L16.0469 3.92188C16.457 3.51172 16.457 2.82812 16.0469 2.41797ZM11.125 10.2383V13H2.375V4.25H8.63672C8.74609 4.25 8.82812 4.22266 8.88281 4.16797L9.97656 3.07422C10.168 2.85547 10.0312 2.5 9.73047 2.5H1.9375C1.19922 2.5 0.625 3.10156 0.625 3.8125V13.4375C0.625 14.1758 1.19922 14.75 1.9375 14.75H11.5625C12.2734 14.75 12.875 14.1758 12.875 13.4375V9.14453C12.875 8.84375 12.5195 8.70703 12.3008 8.89844L11.207 9.99219C11.1523 10.0469 11.125 10.1289 11.125 10.2383Z"
                  fill="white"
                />
              </svg>

              <span>edit SCHOOL</span>
            </v-btn>
          </div>
        </div>

        <v-row style="height: max-content" class="col-12">
          <div style="height: max-content" class="school__info col-3">
            <v-card class="school__card">
              <img src="/images/png/parent/logo.png" alt="" />

              <div class="school__content">
                <div>
                  <h2 class="school__content-title">Kolawole Benjamin</h2>
                  <span class="school__content-subtitle">Full Name</span>
                </div>
                <div class="school__content-status-area">
                  <div>
                    <h4 class="school__content-text">6289178298</h4>
                    <span class="school__content-subtitle">ID</span>
                  </div>
                  <div>
                    <h4 class="school__content-text status">Active</h4>
                    <span class="school__content-subtitle">Status</span>
                  </div>
                </div>
                <div>
                  <div>
                    <h4 class="school__content-text">07023456789</h4>
                    <span class="school__content-subtitle">Phone Number</span>
                  </div>
                </div>
                <div>
                  <div>
                    <h4 class="school__content-text">k.benjamin@gmail.com</h4>
                    <span class="school__content-subtitle">Email Address</span>
                  </div>
                </div>
                <div>
                  <div>
                    <h4 class="school__content-text">
                      Grange International School +2more
                    </h4>
                    <span class="school__content-subtitle"
                      >School Affiliation</span
                    >
                  </div>
                </div>
                <div class="school__content-status-area">
                  <div>
                    <h4 class="school__content-text">942317905</h4>
                    <span class="school__content-subtitle">School ID</span>
                  </div>
                  <div>
                    <h4 class="school__content-text text-right">3</h4>
                    <span class="school__content-subtitle">No of Wards</span>
                  </div>
                </div>

                <div class="school__content-status-area">
                  <div>
                    <h4 class="school__content-text button">NOTIFY PAYMENT</h4>
                  </div>
                  <div>
                    <h4 class="school__content-text button">ARCHIVE</h4>
                  </div>
                </div>
              </div>
            </v-card>
            <div style="padding-top: 24px" class="chart">
              <v-card class="chart__container mini">
                <div class="chart__header">
                  <div>
                    <h3 class="chart__title">Recent History</h3>
                  </div>
                </div>
                <div class="chart__list">
                  <div v-for="n in 3" :key="n" class="chart__list-info">
                    <div class="chart__list-title">
                      <svg
                        width="30"
                        height="30"
                        viewBox="0 0 30 30"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <circle
                          cx="15"
                          cy="15"
                          r="15"
                          fill="#F88B2A"
                          fill-opacity="0.1"
                        />
                        <path
                          d="M9.94205 6.6655C10.2233 6.5405 10.5358 6.57175 10.7545 6.75925L12.0358 7.853L13.2858 6.75925C13.567 6.5405 13.9733 6.5405 14.2545 6.75925L15.5358 7.853L16.7858 6.75925C17.067 6.5405 17.4733 6.5405 17.7545 6.75925L19.0358 7.853L20.2858 6.75925C20.5045 6.57175 20.817 6.5405 21.0983 6.6655C21.3483 6.7905 21.5358 7.0405 21.5358 7.32175V21.8217C21.5358 22.1342 21.3483 22.3842 21.0983 22.5092C20.817 22.6342 20.5045 22.603 20.2858 22.4155L19.0358 21.3217L17.7545 22.4155C17.4733 22.6342 17.067 22.6342 16.7858 22.4155L15.5358 21.3217L14.2545 22.4155C13.9733 22.6342 13.567 22.6342 13.2858 22.4155L12.0358 21.3217L10.7545 22.4155C10.5358 22.603 10.2233 22.6342 9.94205 22.5092C9.69205 22.3842 9.5358 22.1342 9.5358 21.8217V7.32175C9.5358 7.0405 9.69205 6.7905 9.94205 6.6655ZM12.5358 11.0717C12.2545 11.0717 12.0358 11.3217 12.0358 11.5717C12.0358 11.853 12.2545 12.0717 12.5358 12.0717H18.5358C18.7858 12.0717 19.0358 11.853 19.0358 11.5717C19.0358 11.3217 18.7858 11.0717 18.5358 11.0717H12.5358ZM12.5358 18.0717H18.5358C18.7858 18.0717 19.0358 17.853 19.0358 17.5717C19.0358 17.3217 18.7858 17.0717 18.5358 17.0717H12.5358C12.2545 17.0717 12.0358 17.3217 12.0358 17.5717C12.0358 17.853 12.2545 18.0717 12.5358 18.0717ZM12.5358 14.0717C12.2545 14.0717 12.0358 14.3217 12.0358 14.5717C12.0358 14.853 12.2545 15.0717 12.5358 15.0717H18.5358C18.7858 15.0717 19.0358 14.853 19.0358 14.5717C19.0358 14.3217 18.7858 14.0717 18.5358 14.0717H12.5358Z"
                          fill="#F88B2A"
                        />
                      </svg>

                      <span
                        >You have a new ticket from Atlantic Hall College</span
                      >
                    </div>
                    <p class="chart__list-timer">1 min ago</p>
                  </div>
                </div>
              </v-card>
            </div>
          </div>
          <!-- analytics  -->
          <div
            style="height: max-content; margin: 0; padding-top: 0"
            class="col-9 row"
          >
            <!-- header  -->
            <div
              style="height: max-content; padding-bottom: 0"
              class="col-12 chart"
            >
              <v-card class="chart__container only_header">
                <div class="chart__header">
                  <div>
                    <h3 class="chart__title">Wards Account Summary</h3>
                  </div>
                  <v-menu nudge-bottom="5" bottom offset-y>
                    <template v-slot:activator="{ on, attrs }">
                      <v-btn
                        :ripple="false"
                        color="var(--faded-color))"
                        outlined
                        dark
                        v-bind="attrs"
                        v-on="on"
                        class="button button--outlined"
                      >
                        <span>Last 6 months</span>
                        <svg
                          width="10"
                          height="6"
                          viewBox="0 0 10 6"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M9.47656 1.50391L6.00391 5.00391C5.8125 5.16797 5.59375 5.25 5.375 5.25C5.12891 5.25 4.91016 5.16797 4.74609 5.00391L1.27344 1.50391C1 1.25781 0.917969 0.875 1.05469 0.546875C1.19141 0.21875 1.51953 0 1.875 0H8.84766C9.20312 0 9.50391 0.21875 9.64062 0.546875C9.77734 0.875 9.72266 1.25781 9.47656 1.50391Z"
                            fill="black"
                            fill-opacity="0.6"
                          />
                        </svg>
                      </v-btn>
                    </template>
                    <v-list>
                      <v-list-item>
                        <v-list-item-title>Days</v-list-item-title>
                      </v-list-item>
                    </v-list>
                  </v-menu>
                </div>
              </v-card>
            </div>
            <!-- school people info  -->
            <div class="col-12">
              <v-card class="school__offical ward__card">
                <img src="/images/png/parent/user1.png" alt="" />
                <div class="school__offical-content">
                  <div class="content__class">
                    <h3 class="school__offical-name">
                      Kolawole Esther Jesutofunmi
                    </h3>
                    <span class="school__offical-subtitle">Name</span>
                    <div
                      style="
                        display: flex;
                        align-items: center;
                        justify-content: space-between;
                        width: 100%;
                      "
                    >
                      <div>
                        <h3 class="school__offical-text">0865454758</h3>
                        <span class="school__offical-subtitle">ID</span>
                      </div>
                      <div>
                        <h3 class="school__offical-text status">Active</h3>
                        <span class="school__offical-subtitle">Status</span>
                      </div>
                    </div>
                    <h3 class="school__offical-text">k.esther@gmail.com</h3>
                    <span class="school__offical-subtitle">Email Address</span>
                    <h3 class="report">VIEW FULL REPORT</h3>
                  </div>
                </div>
                <!-- stats  -->
                <div class="content__stat">
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Overall Growth</h3>
                      <h3 class="school__offical-name percent">19%</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 10L14.2415 8.09167L10.1748 4.025L6.8415 7.35833L0.666504 1.175L1.8415 0L6.8415 5L10.1748 1.66667L15.4248 6.90833L17.3332 5V10H12.3332Z"
                            fill="#B00020"
                          />
                        </svg>
                        <span>-11%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 3.5L7.7621 12L10.3629 9L12.4435 17L14.5242 15H17.125L21.2863 6L23.8871 8L28.0484 3.5L30.6492 10L32.7298 6L35.3306 10.5L36.8911 4.5H39.4919L41.5726 7.5L43.6532 6L50.4153 6.5L53.0161 2L56.1371 8H57.6976L60.8186 4.5L66.5403 8H68.621L71.2218 16H73.3024L75.3831 9L77.9839 7L80.0645 19.5L84.2258 6.5L88.9073 8.5L90.9879 12L95.6694 15L100.351 12L105.032 15.5H107.113L109.194 17.5L111.274 10L113.875 16.5L115.956 9.5L118.036 14L120.637 15.5L122.718 8.5L126.879 16"
                            stroke="#B00020"
                            stroke-width="1.5"
                          />
                          <circle cx="128" cy="18" r="3" fill="#B00020" />
                        </svg>
                      </div>
                    </div>
                  </div>
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Average Performance</h3>
                      <h3 class="school__offical-name percent">75%</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 0L14.2415 1.90833L10.1748 5.975L6.8415 2.64167L0.666504 8.825L1.8415 10L6.8415 5L10.1748 8.33333L15.4248 3.09167L17.3332 5V0H12.3332Z"
                            fill="#43A047"
                          />
                        </svg>

                        <span>+8%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 17.5L7.7621 9L10.3629 12L12.4435 4L14.5242 6H17.125L21.2863 15L23.8871 13L28.0484 17.5L30.6492 11L32.7298 15L35.3306 10.5L36.8911 16.5H39.4919L41.5726 13.5L43.6532 15L50.4153 14.5L53.0161 19L56.1371 13H57.6976L60.8186 16.5L66.5403 13H68.621L71.2218 5H73.3024L75.3831 12L77.9839 14L80.0645 1.5L84.2258 14.5L88.9073 12.5L90.9879 9L95.6694 6L100.351 9L105.032 5.5H107.113L109.194 3.5L111.274 11L113.875 4.5L115.956 11.5L118.036 7L120.637 5.5L122.718 12.5L126.879 5"
                            stroke="#43A047"
                            stroke-width="1.5"
                          />
                          <circle
                            cx="3"
                            cy="3"
                            r="3"
                            transform="matrix(1 0 0 -1 125 6)"
                            fill="#43A047"
                          />
                        </svg>
                      </div>
                    </div>
                  </div>
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Overall Time Spent</h3>
                      <h3 class="school__offical-name percent">12hrs/wk</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 10L14.2415 8.09167L10.1748 4.025L6.8415 7.35833L0.666504 1.175L1.8415 0L6.8415 5L10.1748 1.66667L15.4248 6.90833L17.3332 5V10H12.3332Z"
                            fill="#B00020"
                          />
                        </svg>
                        <span>-5%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 3.5L7.7621 12L10.3629 9L12.4435 17L14.5242 15H17.125L21.2863 6L23.8871 8L28.0484 3.5L30.6492 10L32.7298 6L35.3306 10.5L36.8911 4.5H39.4919L41.5726 7.5L43.6532 6L50.4153 6.5L53.0161 2L56.1371 8H57.6976L60.8186 4.5L66.5403 8H68.621L71.2218 16H73.3024L75.3831 9L77.9839 7L80.0645 19.5L84.2258 6.5L88.9073 8.5L90.9879 12L95.6694 15L100.351 12L105.032 15.5H107.113L109.194 17.5L111.274 10L113.875 16.5L115.956 9.5L118.036 14L120.637 15.5L122.718 8.5L126.879 16"
                            stroke="#B00020"
                            stroke-width="1.5"
                          />
                          <circle cx="128" cy="18" r="3" fill="#B00020" />
                        </svg>
                      </div>
                    </div>
                  </div>
                </div>
              </v-card>
            </div>
            <div class="col-12">
              <v-card class="school__offical ward__card">
                <img src="/images/png/parent/user2.png" alt="" />
                <div class="school__offical-content">
                  <div class="content__class">
                    <h3 class="school__offical-name">
                      Kolawole Esther Jesutofunmi
                    </h3>
                    <span class="school__offical-subtitle">Name</span>
                    <div
                      style="
                        display: flex;
                        align-items: center;
                        justify-content: space-between;
                        width: 100%;
                      "
                    >
                      <div>
                        <h3 class="school__offical-text">0865454758</h3>
                        <span class="school__offical-subtitle">ID</span>
                      </div>
                      <div>
                        <h3 class="school__offical-text status">Active</h3>
                        <span class="school__offical-subtitle">Status</span>
                      </div>
                    </div>
                    <h3 class="school__offical-text">k.esther@gmail.com</h3>
                    <span class="school__offical-subtitle">Email Address</span>
                    <h3 class="report">VIEW FULL REPORT</h3>
                  </div>
                </div>
                <!-- stats  -->
                <div class="content__stat">
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Overall Growth</h3>
                      <h3 class="school__offical-name percent">3%</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 0L14.2415 1.90833L10.1748 5.975L6.8415 2.64167L0.666504 8.825L1.8415 10L6.8415 5L10.1748 8.33333L15.4248 3.09167L17.3332 5V0H12.3332Z"
                            fill="#43A047"
                          />
                        </svg>

                        <span>8%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 17.5L7.7621 9L10.3629 12L12.4435 4L14.5242 6H17.125L21.2863 15L23.8871 13L28.0484 17.5L30.6492 11L32.7298 15L35.3306 10.5L36.8911 16.5H39.4919L41.5726 13.5L43.6532 15L50.4153 14.5L53.0161 19L56.1371 13H57.6976L60.8186 16.5L66.5403 13H68.621L71.2218 5H73.3024L75.3831 12L77.9839 14L80.0645 1.5L84.2258 14.5L88.9073 12.5L90.9879 9L95.6694 6L100.351 9L105.032 5.5H107.113L109.194 3.5L111.274 11L113.875 4.5L115.956 11.5L118.036 7L120.637 5.5L122.718 12.5L126.879 5"
                            stroke="#43A047"
                            stroke-width="1.5"
                          />
                          <circle
                            cx="3"
                            cy="3"
                            r="3"
                            transform="matrix(1 0 0 -1 125 6)"
                            fill="#43A047"
                          />
                        </svg>
                      </div>
                    </div>
                  </div>
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Average Performance</h3>
                      <h3 class="school__offical-name percent">62.5%</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 10L14.2415 8.09167L10.1748 4.025L6.8415 7.35833L0.666504 1.175L1.8415 0L6.8415 5L10.1748 1.66667L15.4248 6.90833L17.3332 5V10H12.3332Z"
                            fill="#B00020"
                          />
                        </svg>
                        <span>-23%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 3.5L7.7621 12L10.3629 9L12.4435 17L14.5242 15H17.125L21.2863 6L23.8871 8L28.0484 3.5L30.6492 10L32.7298 6L35.3306 10.5L36.8911 4.5H39.4919L41.5726 7.5L43.6532 6L50.4153 6.5L53.0161 2L56.1371 8H57.6976L60.8186 4.5L66.5403 8H68.621L71.2218 16H73.3024L75.3831 9L77.9839 7L80.0645 19.5L84.2258 6.5L88.9073 8.5L90.9879 12L95.6694 15L100.351 12L105.032 15.5H107.113L109.194 17.5L111.274 10L113.875 16.5L115.956 9.5L118.036 14L120.637 15.5L122.718 8.5L126.879 16"
                            stroke="#B00020"
                            stroke-width="1.5"
                          />
                          <circle cx="128" cy="18" r="3" fill="#B00020" />
                        </svg>
                      </div>
                    </div>
                  </div>
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Overall Time Spent</h3>
                      <h3 class="school__offical-name percent">4hrs/wk</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 10L14.2415 8.09167L10.1748 4.025L6.8415 7.35833L0.666504 1.175L1.8415 0L6.8415 5L10.1748 1.66667L15.4248 6.90833L17.3332 5V10H12.3332Z"
                            fill="#B00020"
                          />
                        </svg>
                        <span>-25%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 3.5L7.7621 12L10.3629 9L12.4435 17L14.5242 15H17.125L21.2863 6L23.8871 8L28.0484 3.5L30.6492 10L32.7298 6L35.3306 10.5L36.8911 4.5H39.4919L41.5726 7.5L43.6532 6L50.4153 6.5L53.0161 2L56.1371 8H57.6976L60.8186 4.5L66.5403 8H68.621L71.2218 16H73.3024L75.3831 9L77.9839 7L80.0645 19.5L84.2258 6.5L88.9073 8.5L90.9879 12L95.6694 15L100.351 12L105.032 15.5H107.113L109.194 17.5L111.274 10L113.875 16.5L115.956 9.5L118.036 14L120.637 15.5L122.718 8.5L126.879 16"
                            stroke="#B00020"
                            stroke-width="1.5"
                          />
                          <circle cx="128" cy="18" r="3" fill="#B00020" />
                        </svg>
                      </div>
                    </div>
                  </div>
                </div>
              </v-card>
            </div>
            <div class="col-12">
              <v-card class="school__offical ward__card">
                <img src="/images/png/parent/user3.png" alt="" />
                <div class="school__offical-content">
                  <div class="content__class">
                    <h3 class="school__offical-name">
                      Kolawole Esther Jesutofunmi
                    </h3>
                    <span class="school__offical-subtitle">Name</span>
                    <div
                      style="
                        display: flex;
                        align-items: center;
                        justify-content: space-between;
                        width: 100%;
                      "
                    >
                      <div>
                        <h3 class="school__offical-text">0865454758</h3>
                        <span class="school__offical-subtitle">ID</span>
                      </div>
                      <div>
                        <h3 class="school__offical-text status">Active</h3>
                        <span class="school__offical-subtitle">Status</span>
                      </div>
                    </div>
                    <h3 class="school__offical-text">k.esther@gmail.com</h3>
                    <span class="school__offical-subtitle">Email Address</span>
                    <h3 class="report">VIEW FULL REPORT</h3>
                  </div>
                </div>
                <!-- stats  -->
                <div class="content__stat">
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Overall Growth</h3>
                      <h3 class="school__offical-name percent">19%</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 10L14.2415 8.09167L10.1748 4.025L6.8415 7.35833L0.666504 1.175L1.8415 0L6.8415 5L10.1748 1.66667L15.4248 6.90833L17.3332 5V10H12.3332Z"
                            fill="#B00020"
                          />
                        </svg>
                        <span>-11%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 3.5L7.7621 12L10.3629 9L12.4435 17L14.5242 15H17.125L21.2863 6L23.8871 8L28.0484 3.5L30.6492 10L32.7298 6L35.3306 10.5L36.8911 4.5H39.4919L41.5726 7.5L43.6532 6L50.4153 6.5L53.0161 2L56.1371 8H57.6976L60.8186 4.5L66.5403 8H68.621L71.2218 16H73.3024L75.3831 9L77.9839 7L80.0645 19.5L84.2258 6.5L88.9073 8.5L90.9879 12L95.6694 15L100.351 12L105.032 15.5H107.113L109.194 17.5L111.274 10L113.875 16.5L115.956 9.5L118.036 14L120.637 15.5L122.718 8.5L126.879 16"
                            stroke="#B00020"
                            stroke-width="1.5"
                          />
                          <circle cx="128" cy="18" r="3" fill="#B00020" />
                        </svg>
                      </div>
                    </div>
                  </div>
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Average Performance</h3>
                      <h3 class="school__offical-name percent">75%</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 10L14.2415 8.09167L10.1748 4.025L6.8415 7.35833L0.666504 1.175L1.8415 0L6.8415 5L10.1748 1.66667L15.4248 6.90833L17.3332 5V10H12.3332Z"
                            fill="#B00020"
                          />
                        </svg>
                        <span>+8%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 17.5L7.7621 9L10.3629 12L12.4435 4L14.5242 6H17.125L21.2863 15L23.8871 13L28.0484 17.5L30.6492 11L32.7298 15L35.3306 10.5L36.8911 16.5H39.4919L41.5726 13.5L43.6532 15L50.4153 14.5L53.0161 19L56.1371 13H57.6976L60.8186 16.5L66.5403 13H68.621L71.2218 5H73.3024L75.3831 12L77.9839 14L80.0645 1.5L84.2258 14.5L88.9073 12.5L90.9879 9L95.6694 6L100.351 9L105.032 5.5H107.113L109.194 3.5L111.274 11L113.875 4.5L115.956 11.5L118.036 7L120.637 5.5L122.718 12.5L126.879 5"
                            stroke="#43A047"
                            stroke-width="1.5"
                          />
                          <circle
                            cx="3"
                            cy="3"
                            r="3"
                            transform="matrix(1 0 0 -1 125 6)"
                            fill="#43A047"
                          />
                        </svg>
                      </div>
                    </div>
                  </div>
                  <div class="school__offical-content averages">
                    <div>
                      <h3 class="school__offical-text">Overall Time Spent</h3>
                      <h3 class="school__offical-name percent">12hrs/wk</h3>
                      <div class="school__offical-subtitle average">
                        <svg
                          width="18"
                          height="10"
                          viewBox="0 0 18 10"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M12.3332 10L14.2415 8.09167L10.1748 4.025L6.8415 7.35833L0.666504 1.175L1.8415 0L6.8415 5L10.1748 1.66667L15.4248 6.90833L17.3332 5V10H12.3332Z"
                            fill="#B00020"
                          />
                        </svg>
                        <span>-5%</span>
                      </div>
                      <div>
                        <svg
                          width="131"
                          height="21"
                          viewBox="0 0 131 21"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M1 3.5L7.7621 12L10.3629 9L12.4435 17L14.5242 15H17.125L21.2863 6L23.8871 8L28.0484 3.5L30.6492 10L32.7298 6L35.3306 10.5L36.8911 4.5H39.4919L41.5726 7.5L43.6532 6L50.4153 6.5L53.0161 2L56.1371 8H57.6976L60.8186 4.5L66.5403 8H68.621L71.2218 16H73.3024L75.3831 9L77.9839 7L80.0645 19.5L84.2258 6.5L88.9073 8.5L90.9879 12L95.6694 15L100.351 12L105.032 15.5H107.113L109.194 17.5L111.274 10L113.875 16.5L115.956 9.5L118.036 14L120.637 15.5L122.718 8.5L126.879 16"
                            stroke="#B00020"
                            stroke-width="1.5"
                          />
                          <circle cx="128" cy="18" r="3" fill="#B00020" />
                        </svg>
                      </div>
                    </div>
                  </div>
                </div>
              </v-card>
            </div>
          </div>
        </v-row>
      </v-row>
    </section>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  data() {
    return {
      pieChartData: {
        labels: ["Resolved", "Open", "New", "Pending"],
        datasets: [
          {
            label: "Visualization",
            data: [45, 15, 15, 25],
            backgroundColor: ["#26A69A", "#6200EE", "#EE6002", "#FFBA07"],
            borderColor: "rgba(255, 255, 255, 1)",
            borderWidth: 2,
            radius: 80,
            hoverBackgroundColor: "#F88B2A",
            hoverOffset: 10,
          },
        ],
      },
      barChartOptions: {
        responsive: true,
        maintainAspectRatio: true,
        pointStyle: "star",
        barThickness: 41,
        hoverOffset: 4,
        scales: {
          xAxes: {
            grid: {
              display: false,
            },
          },
          yAxes: {
            position: "right",
            stacked: true,
            // grace: "5%",
            grid: {
              borderColor: ["rgba(0, 0, 0, 0.12)"],
              color: ["rgba(0, 0, 0, 0.12)"],
              drawBorder: false,
            },
            min: 0,
            max: 20,
            suggestedMax: 100,
            suggestedMin: 50,
          },
        },
        plugins: {
          legend: {
            title: {
              display: false,
              padding: 0,
              font: {
                weight: "600",
                size: 14,
              },
            },
            // rtl: true,
            position: "bottom",
            display: false,
            labels: {
              pointStyle: "circle",
              display: false,
              usePointStyle: false,
              align: "start",
              padding: 24,
              color: "#000",
              boxWidth: 9,
              boxHeight: 9,
              font: {
                size: 12,
              },
            },
          },
          title: {
            align: "start",
            display: false,
          },
          tooltip: {
            backgroundColor: "#7769f5",
            // titleColor: "red",
            // bodyColor: "#eb3d34",
            bodyFont: {
              weight: "bold",
              size: 14,
            },
            padding: 13,
            displayColors: false,
          },
        },
      },
      pieChartOptions: {
        responsive: true,
        maintainAspectRatio: true,
        rotation: 0,
        cutout: 0,
        hoverBorderWidth: 1,
        plugins: {
          legend: {
            title: {
              display: true,
              padding: 0,
              font: {
                weight: "600",
                size: 14,
              },
            },
            // rtl: true,
            position: "right",
            labels: {
              pointStyle: "circle",
              usePointStyle: true,
              align: "start",
              padding: 24,
              color: "#000",
              boxWidth: 9,
              boxHeight: 9,
              font: {
                size: 12,
              },
            },
          },
          title: {
            align: "start",
          },
          tooltip: {
            backgroundColor: "#7769f5",
            // titleColor: "red",
            // bodyColor: "#eb3d34",
            bodyFont: {
              weight: "bold",
              size: 14,
            },
            padding: 13,
            displayColors: false,
          },
        },
        animation: {
          animateScale: true,
          animateRotate: true,
        },
      },
      lineChartOPtions: {
        responsive: true,
        maintainAspectRatio: true,
        pointStyle: "rectRounded",
        // pointBackgroundColor: "#F88B2A",
        barThickness: 3,
        hoverOffset: 4,
        tension: 0.1,
        elements: {
          point: {
            radius: 0,
            hoverRadius: 6,
          },
        },
        plugins: {
          legend: {
            title: {
              display: true,
              padding: 0,
              font: {
                weight: "600",
                size: 14,
              },
            },
            // rtl: true,
            position: "bottom",
            labels: {
              // pointStyle: "circle",
              usePointStyle: true,
              align: "start",
              padding: 24,
              color: "#000",
              boxWidth: 9,
              boxHeight: 9,
              font: {
                size: 12,
              },
            },
          },
          title: {
            align: "start",
          },
          tooltip: {
            backgroundColor: "#7769f5",
            // titleColor: "red",
            // bodyColor: "#eb3d34",
            bodyFont: {
              weight: "bold",
              size: 14,
            },
            padding: 13,
            displayColors: false,
          },
        },
        scales: {
          xAxes: {
            grid: {
              display: false,
            },
          },
          yAxes: {
            position: "right",
            grid: {
              borderColor: ["rgba(0, 0, 0, 0.12)"],
              color: ["rgba(0, 0, 0, 0.12)"],
              drawBorder: false,
            },
            min: 0,
            max: 40,
          },
        },
      },
      barChannelData: null,
      barChannelOptions: null,
      lineDataViews: null,
      lineDataSales: null,
      barDataProjects: null,
    };
  },
  methods: {
    showModal(type) {
      switch (type) {
        case "edit":
          this.$refs.editUser.showDialogue();
          break;
        case "viewUser":
          this.$refs.viewUser.showDialogue();
          break;

        default:
          break;
      }
    },
  },
  async mounted() {
    await this.$store.dispatch("mock/actionGetChannels");
    await this.$store.dispatch("mock/actionGetUsers");
    await this.$store.dispatch("mock/actionGetSummary");
    await this.$store.dispatch("mock/actionGetProjects");

    this.barChannelData = {
      labels: [...(this.channels && this.channels.map((item) => item.name))],
      datasets: [
        {
          label: "Visual",
          data: [
            ...(this.channels && this.channels.map((item) => item.summary)),
          ],
          backgroundColor: [
            ...(this.channels && this.channels.map((item) => item.color)),
          ],
          borderColor: "rgba(100, 155, 0, 1)",
          borderWidth: 0,
          hoverOffset: 35,
          hoverBackgroundColor: "rgba(100, 0, 0, 0.5)",
          weight: 1,
          offset: 8,
          radius: 190,
        },
      ],
    };

    this.lineDataViews = {
      labels: [...(this.sales && this.sales.map((item) => item.name))],
      datasets: [
        {
          label: "Visualization",
          data: [...(this.sales && this.sales.map((item) => item.summary))],
          backgroundColor: "rgba(101, 110, 10, 0.75)",
          borderColor: "rgba(140, 155, 0, 1)",
          borderWidth: 1,
        },
      ],
    };

    this.lineDataSales = {
      labels: [
        ...(this.views.views && this.views.views.map((item) => item.name)),
      ],
      datasets: [
        {
          label: "Year 1",
          data: [
            ...(this.views.views &&
              this.views.views.map((item) => item.summary)),
          ],
          backgroundColor: "#6200EE",
          borderColor: "#6200EE",
          borderWidth: 1.5,
        },
        {
          label: "Year 2",
          data: [
            ...(this.views.sales &&
              this.views.sales.map((item) => item.summary)),
          ],
          backgroundColor: "#EE6002",
          borderColor: "#EE6002",
          borderWidth: 1.5,
        },
        {
          label: "Year 3",
          data: [
            ...(this.views.items &&
              this.views.items.map((item) => item.summary)),
          ],
          backgroundColor: "#26A69A",
          borderColor: "#26A69A",
          borderWidth: 1.5,
        },
      ],
    };

    this.barDataProjects = {
      labels: [...(this.projects && this.projects.map((item) => item.name))],
      datasets: [
        {
          label: "Students Performance",
          data: [
            ...(this.projects && this.projects.map((item) => item.summary)),
          ],
          backgroundColor: [
            ...(this.projects && this.projects.map((item) => item.color)),
          ],
          borderColor: "rgba(100, 155, 0, 1)",
          // barPercentage: 0.8,
          // categoryPercentage: 0.5,
          borderWidth: 0,
          hoverOffset: 35,
          hoverBackgroundColor: "#F88B2A",
          weight: 1,
          offset: 8,
          radius: 180,
        },
      ],
    };
  },
  computed: {
    ...mapState({ channels: (state) => state.mock.channels }),
    ...mapState({ projects: (state) => state.mock.projects }),
    ...mapState({ users: (state) => state.mock.users }),
    ...mapState({ views: (state) => state.mock.summary }),
    ...mapState({ sales: (state) => state.mock.summary.sales }),
  },
};
</script>


<style lang="scss" scoped>
</style>