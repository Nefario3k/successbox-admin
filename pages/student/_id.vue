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
            <header>Adeniyi Elisha</header>
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

              <span>edit student</span>
            </v-btn>
          </div>
        </div>

        <v-row style="padding-right: 0" class="col-12">
          <div class="school__info col-3">
            <v-card class="school__card">
              <img src="/images/png/student/logo.png" alt="" />

              <div class="school__content">
                <div>
                  <h2 class="school__content-title">Adeniyi Elisha</h2>
                  <span class="school__content-subtitle">Full Name</span>
                </div>
                <div class="school__content-status-area">
                  <!-- name  -->
                  <div>
                    <h4 class="school__content-text">6289178298</h4>
                    <span class="school__content-subtitle">ID</span>
                  </div>
                  <!-- id and status  -->
                  <div>
                    <h4 class="school__content-text status">Active</h4>
                    <span class="school__content-subtitle">Status</span>
                  </div>
                </div>
                <!-- number  -->
                <div>
                  <div>
                    <h4 class="school__content-text">07023456789</h4>
                    <span class="school__content-subtitle">Phone Number</span>
                  </div>
                </div>
                <!-- email  -->
                <div>
                  <div>
                    <h4 class="school__content-text">
                      adeniyi.elisha@gmail.com
                    </h4>
                    <span class="school__content-subtitle">Email Address</span>
                  </div>
                </div>
                <!-- school  -->
                <div>
                  <div>
                    <h4 class="school__content-text">
                      Grange International School
                    </h4>
                    <span class="school__content-subtitle"
                      >School Affiliation</span
                    >
                  </div>
                </div>

                <div class="school__content-status-area">
                  <!-- name  -->
                  <div>
                    <h4 class="school__content-text">942317905</h4>
                    <span class="school__content-subtitle">School ID</span>
                  </div>
                  <!-- id and status  -->
                  <div>
                    <h4 class="school__content-text">942317905</h4>
                    <span class="school__content-subtitle">Parent ID</span>
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
          </div>
          <div style="height: max-content" class="col-9 chart">
            <v-card class="chart__container mini">
              <div style="margin-bottom: -9%" class="chart__header">
                <div>
                  <h3 class="chart__title">Report Summary</h3>
                  <span class="chart__subtitle">Oct 21 - Mar 2022</span>
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

              <div
                style="
                  display: flex;
                  align-items: center;
                  justify-content: space-between;
                  gap: 15px;
                "
              >
                <div class="chart__chart-area mini__area">
                  <client-only v-if="pieChartData" placeholder="Loading...">
                    <PieChart
                      :chartData="pieChartData"
                      :chart-options="pieChartOptions"
                      :height="100"
                    />
                  </client-only>
                </div>
                <div class="chart__chart-area mini__area">
                  <client-only v-if="lineDataSales" placeholder="Loading...">
                    <LineChart
                      :chart-options="lineChartOPtions"
                      :chart-data="lineDataSales"
                      chart-id="lineChart"
                      :height="200"
                    />
                  </client-only>
                </div>
              </div>
              <div
                style="
                  display: flex;
                  align-items: center;
                  justify-content: space-between;
                "
              >
                <span class="chart__subtitle-under"
                  >Pie chart of time spent on all subjects</span
                >
                <span class="chart__subtitle-under"
                  >Graph of scores for test practice of all subject over
                  time</span
                >
              </div>
            </v-card>
          </div>
          <div class="col-3 chart">
            <v-card class="chart__container">
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
          <div style="margin-top: -14%" class="col-9">
            <v-data-table
              v-model="selected"
              :headers="headers"
              :items="bookData"
              :single-select="false"
              item-key="topic"
              :disable-filtering="true"
              :disable-pagination="false"
              :disable-sort="true"
              :items-per-page="5"
              checkbox-color="var(--primary-color)"
              :hide-default-footer="false"
              show-select
              class="generic_data_table"
            >
              <!-- subject  -->
              <template v-slot:item.topic="{ item }">
                <div class="user_content">
                  <p>{{ item.topic }}</p>
                </div>
              </template>
              <!-- test type -->
              <template v-slot:item.week="{ item }">
                <div class="user_content">
                  <p>{{ item.week }}</p>
                </div>
              </template>
              <!-- id  -->
              <template v-slot:item.id="{ item }">
                <div class="user_content">
                  <p>{{ item.id }}</p>
                </div>
              </template>
              <!-- grade  -->
              <template v-slot:item.category="{ item }">
                <div class="user_content">
                  <p class="category">{{ item.category }}</p>
                </div>
              </template>
              <!-- improvement  -->
              <template v-slot:item.status="{ item }">
                <div class="user_content">
                  <p class="status" v-if="item.status >= 10">
                    <svg
                      width="12"
                      height="13"
                      viewBox="0 0 12 13"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M11.0879 6.25391C10.9238 6.41797 10.7051 6.5 10.4863 6.5C10.2402 6.5 10.0215 6.41797 9.85742 6.25391L6.98633 3.38281V11.75C6.98633 12.2422 6.57617 12.625 6.11133 12.625C5.67383 12.625 5.23633 12.2422 5.23633 11.75V3.38281L2.33789 6.25391C2.00977 6.60938 1.43555 6.60938 1.10742 6.25391C0.751953 5.92578 0.751953 5.35156 1.10742 5.02344L5.48242 0.648438C5.81055 0.292969 6.38477 0.292969 6.71289 0.648438L11.0879 5.02344C11.4434 5.35156 11.4434 5.92578 11.0879 6.25391Z"
                        fill="#12B855"
                      />
                    </svg>
                    <span>{{ item.status }}%</span>
                  </p>
                  <p class="status danger" v-if="item.status <= 9">
                    <svg
                      width="12"
                      height="14"
                      viewBox="0 0 12 14"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M11.0879 8.50391L6.71289 12.8789C6.54883 13.043 6.33008 13.125 6.11133 13.125C5.86523 13.125 5.64648 13.043 5.48242 12.8789L1.10742 8.50391C0.751953 8.17578 0.751953 7.60156 1.10742 7.27344C1.43555 6.91797 2.00977 6.91797 2.33789 7.27344L5.23633 10.1445V1.75C5.23633 1.28516 5.61914 0.902344 6.08398 0.902344C6.52148 0.902344 6.98633 1.28516 6.98633 1.75V10.1445L9.85742 7.27344C10.1855 6.91797 10.7598 6.91797 11.0879 7.27344C11.4434 7.60156 11.4434 8.17578 11.0879 8.50391Z"
                        fill="#B00020"
                      />
                    </svg>
                    <span>{{ item.status }}%</span>
                  </p>
                </div>
              </template>
              <!-- actions  -->
              <template v-slot:item.action="{ item }">
                <div class="user_content">
                  <div class="table__actions">
                    <div>
                      <svg
                        width="17"
                        height="13"
                        viewBox="0 0 17 13"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M8.5 0.375C6.28516 0.375 4.50781 1.38672 3.22266 2.58984C1.9375 3.76562 1.08984 5.1875 0.679688 6.17188C0.597656 6.39062 0.597656 6.63672 0.679688 6.85547C1.08984 7.8125 1.9375 9.23438 3.22266 10.4375C4.50781 11.6406 6.28516 12.625 8.5 12.625C10.6875 12.625 12.4648 11.6406 13.75 10.4375C15.0352 9.23438 15.8828 7.8125 16.293 6.85547C16.375 6.63672 16.375 6.39062 16.293 6.17188C15.8828 5.1875 15.0352 3.76562 13.75 2.58984C12.4648 1.38672 10.6875 0.375 8.5 0.375ZM12.4375 6.5C12.4375 8.6875 10.6602 10.4375 8.5 10.4375C6.3125 10.4375 4.5625 8.6875 4.5625 6.5C4.5625 4.33984 6.3125 2.5625 8.5 2.5625C10.6602 2.5625 12.4375 4.33984 12.4375 6.5ZM8.5 4.75C8.5 5.73438 7.70703 6.5 6.75 6.5C6.42188 6.5 6.12109 6.41797 5.875 6.28125C5.875 6.36328 5.875 6.44531 5.875 6.5C5.875 7.94922 7.05078 9.125 8.5 9.125C9.94922 9.125 11.125 7.94922 11.125 6.5C11.125 5.05078 9.94922 3.875 8.5 3.875C8.41797 3.875 8.33594 3.90234 8.25391 3.90234C8.39062 4.14844 8.5 4.44922 8.5 4.75Z"
                          fill="black"
                          fill-opacity="0.6"
                        />
                      </svg>
                    </div>
                    <div>
                      <svg
                        width="13"
                        height="13"
                        viewBox="0 0 13 13"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M12.625 10C12.625 11.4766 11.4492 12.625 10 12.625C8.52344 12.625 7.375 11.4766 7.375 10C7.375 9.91797 7.375 9.80859 7.40234 9.69922L4.80469 8.41406C4.33984 8.85156 3.68359 9.125 3 9.125C1.52344 9.125 0.375 7.97656 0.375 6.5C0.375 5.05078 1.52344 3.875 3 3.875C3.68359 3.875 4.33984 4.17578 4.80469 4.61328L7.40234 3.32812C7.375 3.21875 7.375 3.10938 7.375 3C7.375 1.55078 8.52344 0.375 10 0.375C11.4492 0.375 12.625 1.55078 12.625 3C12.625 4.47656 11.4492 5.625 10 5.625C9.28906 5.625 8.63281 5.35156 8.16797 4.91406L5.57031 6.19922C5.59766 6.30859 5.625 6.39062 5.625 6.5C5.625 6.60938 5.59766 6.71875 5.57031 6.82812L8.16797 8.11328C8.63281 7.67578 9.28906 7.375 10 7.375C11.4492 7.375 12.625 8.55078 12.625 10Z"
                          fill="black"
                          fill-opacity="0.6"
                        />
                      </svg>
                    </div>
                    <div>
                      <svg
                        width="14"
                        height="13"
                        viewBox="0 0 14 13"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M0.875 0.375H13.125C13.5898 0.375 14 0.785156 14 1.25V2.125C14 2.61719 13.5898 3 13.125 3H0.875C0.382812 3 0 2.61719 0 2.125V1.25C0 0.785156 0.382812 0.375 0.875 0.375ZM0.875 3.875H13.125V10.875C13.125 11.8594 12.332 12.625 11.375 12.625H2.625C1.64062 12.625 0.875 11.8594 0.875 10.875V3.875ZM4.375 6.0625C4.375 6.30859 4.56641 6.5 4.8125 6.5H9.1875C9.40625 6.5 9.625 6.30859 9.625 6.0625C9.625 5.84375 9.40625 5.625 9.1875 5.625H4.8125C4.56641 5.625 4.375 5.84375 4.375 6.0625Z"
                          fill="black"
                          fill-opacity="0.6"
                        />
                      </svg>
                    </div>
                  </div>
                </div>
              </template>
            </v-data-table>
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
            radius: 120,
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
            display: false,
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
      selected: [],
      headers: [
        {
          text: "Subject",
          align: "start",
          value: "topic",
        },
        { text: "Test Type", value: "week" },
        { text: "ID", value: "id" },
        { text: "Grade", value: "category" },
        { text: "Improvement", value: "status" },
        { text: "Actions", value: "action" },
      ],
      bookData: [
        {
          topic: "Human Rights",
          week: "Standard",
          id: 8755443346,
          category: "copy",
          status: 24,
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Inter-Personal Relationships",
          week: "UTME",
          id: 8755443346,
          category: "copy",
          status: 24,
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Citizenship & Nationalism.",
          week: "Quick Practice",
          id: 8755443346,
          category: "test",
          status: 8,
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Law and Order",
          week: "Quick Practice",
          id: 8755443346,
          category: "test",
          status: 8,
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Human Right",
          week: "Quick Practice",
          id: 8755443346,
          category: "test",
          status: 8,
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Law and Orders",
          week: "Quick Practice",
          id: 8755443346,
          category: "test",
          status: 8,
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Responsible Parenthood",
          week: "Quick Practice",
          id: 8755443346,
          category: "test",
          status: 8,
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Traffic Regulations",
          week: "Quick Practice",
          id: 8755443346,
          category: "test",
          status: 10,
          author: "Kolawole Abraham",
          action: null,
        },
      ],
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
#pie-chart {
  height: 200px !important;
}
</style>