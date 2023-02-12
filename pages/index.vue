<template>
  <div>
    <section id="pageBody">
      <v-row class="content_row">
        <!-- title  -->
        <div class="col-12 header_wrapper">
          <header>Dashboard</header>
        </div>

        <v-row
          style="padding-right: 0"
          class="col-12 col-md-8 col-lg-8 col-xl-8"
        >
          <!-- analytics  -->
          <div class="col-12 row" style="margin: 0; padding-right: 0">
            <div
              class="col-6 col-md-3 col-lg-3 col-xl-3"
              style="padding-left: 0"
            >
              <v-card class="analyticsCard">
                <h3>Revenue</h3>
                <h4>345.8 M</h4>
                <span>57% increase</span>
              </v-card>
            </div>
            <div
              class="col-6 col-md-3 col-lg-3 col-xl-3"
              style="padding-left: 0"
            >
              <v-card class="analyticsCard">
                <h3>Users</h3>
                <h4>29,674</h4>
                <span>23% increase</span>
              </v-card>
            </div>
            <div
              class="col-6 col-md-3 col-lg-3 col-xl-3"
              style="padding-left: 0"
            >
              <v-card class="analyticsCard">
                <h3>Schools</h3>
                <h4>519</h4>
                <span>10% increase</span>
              </v-card>
            </div>
            <div
              class="col-6 col-md-3 col-lg-3 col-xl-3"
              style="padding-left: 0"
            >
              <v-card class="analyticsCard">
                <h3>Parents</h3>
                <h4>5,908</h4>
                <span class="danger">2% decrease</span>
              </v-card>
            </div>
          </div>
          <!-- Revenue Growth  -->
          <div class="col-12 chart">
            <v-card class="chart__container">
              <div class="chart__header">
                <div>
                  <h3 class="chart__title">Revenue Growth</h3>
                  <span class="chart__subtitle">Mar 21 - Mar 27</span>
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
                      <span>Weekly</span>
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

              <div class="chart__chart-area">
                <client-only v-if="barDataProjects" placeholder="Loading...">
                  <BarChart
                    :chartData="barDataProjects"
                    :chart-options="barChartOptions"
                    :height="50"
                    :width="100"
                  />
                </client-only>
              </div>
            </v-card>
          </div>
          <!-- User Growth  -->
          <div class="col-12 chart">
            <v-card class="chart__container">
              <div class="chart__header">
                <div>
                  <h3 class="chart__title">User Growth</h3>
                  <span class="chart__subtitle">Sept 2021 - Mar 2022</span>
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
                      <span>6 Months</span>
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

              <div class="chart__chart-area">
                <client-only v-if="lineDataSales" placeholder="Loading...">
                  <LineChart
                    :chart-options="lineChartOPtions"
                    :chart-data="lineDataSales"
                    :height="40"
                    :width="100"
                    chart-id="lineChart"
                  />
                </client-only>
              </div>
            </v-card>
          </div>
        </v-row>

        <v-row
          style="padding-left: 0; height: max-content"
          class="col-12 col-md-4 col-lg-4 col-xl-4"
        >
          <div style="height: max-content" class="col-12 chart mini">
            <v-card class="chart__container">
              <div class="chart__header">
                <div>
                  <h3 class="chart__title">Tickets</h3>
                  <span class="chart__subtitle">Mar 21 - Mar 27</span>
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
                      <span>Weekly</span>
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

              <div style="margin: 0 -24px" class="chart__chart-area">
                <client-only v-if="pieChartData" placeholder="Loading...">
                  <PieChart
                    :chartData="pieChartData"
                    :chart-options="pieChartOptions"
                  />
                </client-only>
              </div>
            </v-card>
          </div>
          <div class="col-12 chart">
            <v-card class="chart__container mini">
              <div class="chart__header">
                <div>
                  <h3 class="chart__title">Notification</h3>
                </div>
                <v-btn
                  :ripple="false"
                  dark
                  color="var(--faded-color))"
                  outlined
                  class="button button--outlined button--danger"
                >
                  <span>clear</span>
                  <svg
                    width="10"
                    height="11"
                    viewBox="0 0 10 11"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M6.80469 5.75L9.53906 3.01562C9.89453 2.6875 9.89453 2.14062 9.53906 1.8125L8.9375 1.21094C8.60938 0.855469 8.0625 0.855469 7.73438 1.21094L5 3.94531L2.23828 1.21094C1.91016 0.855469 1.36328 0.855469 1.03516 1.21094L0.433594 1.8125C0.078125 2.14062 0.078125 2.6875 0.433594 3.01562L3.16797 5.75L0.433594 8.51172C0.078125 8.83984 0.078125 9.38672 0.433594 9.71484L1.03516 10.3164C1.36328 10.6719 1.91016 10.6719 2.23828 10.3164L5 7.58203L7.73438 10.3164C8.0625 10.6719 8.60938 10.6719 8.9375 10.3164L9.53906 9.71484C9.89453 9.38672 9.89453 8.83984 9.53906 8.51172L6.80469 5.75Z"
                      fill="#B00020"
                    />
                  </svg>
                </v-btn>
              </div>
              <div class="chart__list">
                <div v-for="n in 5" :key="n" class="chart__list-info">
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
            radius: 100,
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
            align: "start",
            labels: {
              pointStyle: "line",
              usePointStyle: true,
              textAlign: "start",
              padding: 14,
              color: "#00000099",
              boxWidth: 90,
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

<style scoped lang="scss">
.content_row {
  .users_table {
    display: none;
    .table_card_container {
      background: #fff;
      border-radius: 12px;
      box-shadow: none !important;

      .userImage {
        width: 4rem;
        height: 4rem;
        background-color: var(--secondary-color);
        display: inline-flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        border-radius: 50%;
        span {
          color: #fff;
          text-transform: uppercase;
          font-weight: 500;
          font-size: 1.8rem;
        }
      }
    }
  }
  .user_details {
    display: flex;
    flex-direction: column;
    h3 {
      font-weight: 500;
      color: var(--bar-text-color);
      font-size: 1.4rem;
    }
    a {
      &:hover {
        p {
          color: var(--primary-color);
          transition: all 0.2s ease-in-out;
        }
      }
    }
    p {
      margin: 0;
      color: var(--bar-sub-text-color);
      font-weight: 400;
      font-size: 1.4rem;
      transition: all 0.2s ease-in-out;
    }
  }
  p.table_number_stats {
    color: var(--primary-color);
    font-weight: 400;
    font-size: 1.6rem;
    margin: 0;
  }
  .viewMoreUsers {
    text-align: left;
    border-top: 1px solid var(--border-color);
    padding: 8px 16px;
    span {
      color: var(--primary-color);
      font-size: 1.4rem;
      font-weight: 500;
      cursor: pointer;
    }
  }
  .captionTable {
    text-align: left;
    border-bottom: 1px solid var(--border-color);
    padding: 8px 16px;
    span {
      color: var(--secondary-color);
      font-size: 1.4rem;
      font-weight: 500;
      cursor: pointer;
    }
  }
  .no_content_data {
    min-height: 27.8rem;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    grid-gap: 20px;
    text-align: center;
    h3 {
      font-weight: 700;
      font-size: 2.4rem;
      color: var(--bar-text-color);
    }
    span {
      font-weight: 500;
      font-size: 1.6rem;
      color: var(--bar-sub-text-color);
    }
  }
}
.sidebar_informatics {
  .main_recent_container {
    padding: 22px 20px;
    height: 100%;
    width: 100%;
    .header_informatics {
      display: flex;
      align-items: center;
      justify-content: space-between;
      grid-gap: 10px;
      h3 {
        text-transform: capitalize;
        font-weight: 600;
        font-size: 1.4rem;
        color: var(--info-dark-color);
      }
      svg {
        cursor: pointer;
      }
    }
    .list {
      .user_content_details {
        margin: 10px 0;
        .userImage {
          width: 2rem;
          height: 2rem;
          background-color: var(--secondary-color);
          display: inline-flex;
          align-items: center;
          justify-content: center;
          text-align: center;
          border-radius: 50%;
          span {
            color: #fff;
            text-transform: uppercase;
            font-weight: 500;
            font-size: 1rem;
          }
        }
        .user_details {
          display: flex;
          flex-direction: column;
          h3 {
            font-weight: 400;
            color: var(--info-dark-color);
            font-size: 1.4rem;
          }
          a {
            &:hover {
              p {
                color: var(--primary-color);
                transition: all 0.2s ease-in-out;
              }
            }
          }
          p {
            margin: 0;
            color: var(--bar-sub-text-color);
            font-weight: 400;
            font-size: 1rem;
            transition: all 0.2s ease-in-out;
            .property_name {
              color: var(--primary-color);
            }
          }
        }
        & > a {
          p {
            color: var(--primary-color);
            font-weight: 400;
            font-size: 1.4rem;
            margin: 0;
          }
        }
        &.popProp {
          padding-bottom: 0;
        }
      }
    }
  }
}

.dropdownList {
  margin: 0;
  padding: 0;
  .list_item {
    border-radius: 0;
    margin-bottom: 0 !important;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    .list_title {
      font-weight: 500;
      font-size: 1.6rem;
      color: var(--secondary-color);
      overflow: visible !important;
      transition: all 0.2s ease-in-out;
    }
    &::before {
      border-radius: 0;
    }
    // &:hover {
    //   background: var(--primary-color);
    //   transition: all 0.2s ease-in-out;
    //   .list_title {
    //     color: #fff;
    //     transition: all 0.2s ease-in-out;
    //   }
    // }
    &.active {
      background: var(--primary-color);
      transition: all 0.2s ease-in-out;
      .list_title {
        color: #fff;
        transition: all 0.2s ease-in-out;
      }
    }
  }
  .ItemList {
    border-radius: 0;
    margin-bottom: 0 !important;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    .item_title {
      font-weight: 400;
      font-size: 1.4rem;
      color: var(--label02-color);
      overflow: visible !important;
      transition: all 0.2s ease-in-out;
    }
    &:hover {
      background: var(--primary-color);
      transition: all 0.2s ease-in-out;
      .item_title {
        color: #fff;
        transition: all 0.2s ease-in-out;
      }
      svg {
        transition: all 0.2s ease-in-out;
        rect {
          stroke: #fff !important;
          transition: all 0.2s ease-in-out;
        }
        path {
          stroke: #fff !important;
          transition: all 0.2s ease-in-out;
        }
        circle {
          stroke: #fff !important;
          transition: all 0.2s ease-in-out;
        }
        &.delete {
          path {
            fill: #fff !important;
            transition: all 0.2s ease-in-out;
          }
        }
      }
    }
    &:has(.delete):hover {
      background: red;
      transition: all 0.2s ease-in-out;
    }
  }
}

@media (max-width: 959px) {
  .row.content_row > .col-12 {
    padding: 0 !important;
  }
}
</style>