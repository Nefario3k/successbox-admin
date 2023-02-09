<template>
  <div>
    <section id="pageBody">
      <v-row class="content_row">
        <!-- title  -->
        <div style="padding-right: 24px" class="col-12 header_wrapper">
          <div style="display: flex; align-items: center; grid-gap: 25px">
            <header>Tickets</header>
            <v-menu nudge-bottom="5" bottom offset-y>
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  :ripple="false"
                  color="var(--faded-color)"
                  outlined
                  dark
                  v-bind="attrs"
                  v-on="on"
                  class="button button--left--outlined"
                >
                  <span>Last 6 Months</span>
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
          <div class="header_wrapper-buttons">
            <v-btn color="var(--primary-color)" class="button button--header">
              <svg
                width="14"
                height="15"
                viewBox="0 0 14 15"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7 0.96875C3.25391 0.96875 0.21875 4.00391 0.21875 7.75C0.21875 11.4961 3.25391 14.5312 7 14.5312C10.7461 14.5312 13.7812 11.4961 13.7812 7.75C13.7812 4.00391 10.7461 0.96875 7 0.96875ZM10.9375 8.51562C10.9375 8.70703 10.7734 8.84375 10.6094 8.84375H8.09375V11.3594C8.09375 11.5508 7.92969 11.6875 7.76562 11.6875H6.23438C6.04297 11.6875 5.90625 11.5508 5.90625 11.3594V8.84375H3.39062C3.19922 8.84375 3.0625 8.70703 3.0625 8.51562V6.98438C3.0625 6.82031 3.19922 6.65625 3.39062 6.65625H5.90625V4.14062C5.90625 3.97656 6.04297 3.8125 6.23438 3.8125H7.76562C7.92969 3.8125 8.09375 3.97656 8.09375 4.14062V6.65625H10.6094C10.7734 6.65625 10.9375 6.82031 10.9375 6.98438V8.51562Z"
                  fill="white"
                />
              </svg>
              <span>NEW TICKET</span>
            </v-btn>
          </div>
        </div>
        <!-- analytics  -->
        <div class="col-12 row" style="margin: 0">
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>All</h3>
              <h4>675</h4>
              <span>57% increase</span>
            </v-card>
          </div>
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>Resolved</h3>
              <h4>532</h4>
              <span>23% increase</span>
            </v-card>
          </div>
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>Open</h3>
              <h4>29</h4>
              <span>10% increase</span>
            </v-card>
          </div>
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>Pending</h3>
              <h4>14</h4>
              <span class="danger">2% decrease</span>
            </v-card>
          </div>
        </div>
        <v-row class="col-12">
          <div class="col-3 ticket">
            <div class="ticket__search">
              <div class="relative">
                <input type="text" placeholder="Search.." />
              </div>

              <v-menu nudge-bottom="5" bottom offset-y>
                <template v-slot:activator="{ on, attrs }">
                  <v-btn
                    v-bind="attrs"
                    v-on="on"
                    :ripple="false"
                    color="#fff"
                    class="button button--filter"
                  >
                    <span>Newest first</span>
                    <svg
                      width="12"
                      height="7"
                      viewBox="0 0 12 7"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M1.70661 0C1.0738 0 0.757392 0.773438 1.21442 1.23047L5.71442 5.73047C5.99567 6.01172 6.4527 6.01172 6.73395 5.73047L11.234 1.23047C11.691 0.773438 11.3746 0 10.7418 0H1.70661Z"
                        fill="#383B4C"
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
            <div class="ticket__area">
              <v-card class="ticket__card">
                <v-list nav class="ticket__list">
                  <v-list-item
                    v-for="n in 20"
                    :key="n"
                    class="ticket__list-item"
                  >
                    <v-list-item-icon>
                      <svg
                        width="13"
                        height="12"
                        viewBox="0 0 13 12"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <ellipse
                          cx="6.30551"
                          cy="6"
                          rx="6.30551"
                          ry="6"
                          fill="#FFBA07"
                        />
                      </svg>
                    </v-list-item-icon>
                    <v-list-item-content>
                      <v-list-item-title class="ticket__list-title"
                        >Ticket ID 0203</v-list-item-title
                      >
                      <v-list-item-subtitle class="ticket__list-subtitle"
                        ><span>Today</span>
                        <span>24 mins ago</span>
                      </v-list-item-subtitle></v-list-item-content
                    >
                  </v-list-item>
                </v-list>
              </v-card>
            </div>
          </div>
          <div class="col-9 messages">
            <v-card class="messages__card">
              <v-row class="messages__row">
                <!-- header -->
                <div class="col-12 header_wrapper">
                  <div class="header_area">
                    <header>
                      Grenville International School (687543343) - Ticket ID
                      0203
                    </header>
                  </div>
                  <div class="header_wrapper-buttons">
                    <v-btn
                      outlined
                      color="var(--primary-color)"
                      class="button button--header button--outlined"
                    >
                      <svg
                        width="15"
                        height="15"
                        viewBox="0 0 15 15"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M7.5 0.96875C3.75391 0.96875 0.71875 4.03125 0.71875 7.75C0.71875 11.4961 3.75391 14.5312 7.5 14.5312C11.2188 14.5312 14.2812 11.4961 14.2812 7.75C14.2812 4.03125 11.2188 0.96875 7.5 0.96875ZM11.0547 4.19531C12.832 6 12.9688 8.73438 11.6016 10.6484L4.60156 3.64844C6.51562 2.28125 9.25 2.41797 11.0547 4.19531ZM3.91797 11.332C2.14062 9.52734 2.00391 6.79297 3.37109 4.87891L10.3711 11.8789C8.45703 13.2461 5.72266 13.1094 3.91797 11.332Z"
                          fill="#383B4C"
                        />
                      </svg>

                      <span>MARK AS BLOCKED</span>
                    </v-btn>
                    <v-btn
                      color="var(--nav-h3-color)"
                      class="button button--header"
                    >
                      <svg
                        width="14"
                        height="15"
                        viewBox="0 0 14 15"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M13.7812 7.75C13.7812 4.03125 10.7188 0.96875 7 0.96875C3.25391 0.96875 0.21875 4.03125 0.21875 7.75C0.21875 11.4961 3.25391 14.5312 7 14.5312C10.7188 14.5312 13.7812 11.4961 13.7812 7.75ZM6.20703 11.3594C6.04297 11.5234 5.74219 11.5234 5.57812 11.3594L2.73438 8.51562C2.57031 8.35156 2.57031 8.05078 2.73438 7.88672L3.36328 7.28516C3.52734 7.09375 3.80078 7.09375 3.96484 7.28516L5.90625 9.19922L10.0078 5.09766C10.1719 4.90625 10.4453 4.90625 10.6094 5.09766L11.2383 5.69922C11.4023 5.86328 11.4023 6.16406 11.2383 6.32812L6.20703 11.3594Z"
                          fill="white"
                        />
                      </svg>

                      <span>Mark as resolved</span>
                    </v-btn>
                  </div>
                </div>
                <!-- ticket title  -->
                <div class="messages__title col-12">
                  <div class="messages__title-area">
                    <span class="messages__title-span"
                      >Subscription Activation Error</span
                    >
                  </div>
                </div>
                <!-- chat area  -->
                <v-row class="col-12 messages__area">
                  <div class="col-12 messages__area-message ticketer__message">
                    <div>
                      <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                        Cras elit, non nibh consequat. Ac nunc ut integer non.
                        Sit et tincidunt mauris massa tellus nisl urna. Mauris
                        sollicitudin fermentum interdum volutpat nisl quis
                        condimentum tempus. Tellus elementum tempus nunc nisi
                        etiam. Consectetur auctor ac diam dictum nec quam.
                        Tempus nisl morbi amet nunc id mauris nibh. Arcu, est
                        sollicitudin aliquet aliquam sed iaculis erat massa
                        arcu. Ac quam metus malesuada et felis ipsum phasellus
                        elit. Diam ipsum ut pulvinar aliquet neque, libero
                        placerat elit ut. Sit nunc, enim et egestas scelerisque
                        volutpat pulvinar id aliquam. Nullam lectus blandit at
                        eget scelerisque morbi et. Nibh eleifend sit nec orci
                        adipiscing vestibulum iaculis. Enim id suspendisse mi
                        id. Neque, gravida tellus id leo. Amet, purus tempor,
                        sem nec sit maecenas habitant consectetur. Et duis
                        viverra pulvinar sed.
                      </p>
                    </div>
                  </div>
                  <div class="col-12 messages__area-message admin__message">
                    <div>
                      <p>
                        Sit nunc, enim et egestas scelerisque volutpat pulvinar
                        id aliquam. Nullam lectus blandit at eget scelerisque
                        morbi et. Nibh eleifend sit nec orci adipiscing
                        vestibulum iaculis. Enim id suspendisse mi id. Neque,
                        gravida tellus id leo. Amet, purus tempor, sem nec sit
                        maecenas habitant consectetur. Et duis viverra pulvinar
                        sed.
                      </p>
                    </div>
                  </div>
                  <div class="col-12 messages__area-message ticketer__message">
                    <div>
                      <p>
                        Sit nunc, enim et egestas scelerisque volutpat pulvinar
                        id aliquam.
                      </p>
                    </div>
                  </div>
                  <div class="col-12 messages__area-message admin__message">
                    <div>
                      <p>
                        Sit nunc, enim et egestas scelerisque volutpat pulvinar
                        id aliquam. Nullam lectus blandit at eget scelerisque
                        morbi et. Nibh eleifend sit nec orci adipiscing
                        vestibulum iaculis. Enim id suspendisse mi id. Neque,
                        gravida tellus id leo. Amet, purus tempor, sem nec sit
                        maecenas habitant consectetur. Et duis viverra pulvinar
                        sed.
                      </p>
                    </div>
                    <p class="messages__status">
                      <svg
                        width="14"
                        height="10"
                        viewBox="0 0 14 10"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M13.125 1.25C13.125 1.49609 13.0156 1.71484 12.8516 1.87891L5.85156 8.87891C5.6875 9.04297 5.46875 9.125 5.25 9.125C5.00391 9.125 4.78516 9.04297 4.62109 8.87891L1.12109 5.37891C0.957031 5.21484 0.875 4.99609 0.875 4.75C0.875 4.25781 1.25781 3.875 1.75 3.875C1.96875 3.875 2.1875 3.98438 2.35156 4.14844L5.25 7.01953L11.6211 0.648438C11.7852 0.484375 12.0039 0.375 12.25 0.375C12.7148 0.375 13.125 0.757812 13.125 1.25Z"
                          fill="#F88B2A"
                        />
                      </svg>

                      <span>Read</span>
                    </p>
                  </div>
                </v-row>
                <!-- chat input  -->
                <div class="col-12 messages__inputs">
                  <div class="relative">
                    <input type="text" placeholder="Type here.." />
                    <div class="absolute">
                      <svg
                        width="22"
                        height="21"
                        viewBox="0 0 22 21"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19.5938 0.65625L1.46875 11.0859C0.765625 11.4766 0.84375 12.4922 1.54688 12.7656L5.72656 14.5234L16.9375 4.64062C17.1328 4.44531 17.4453 4.71875 17.25 4.95312L7.875 16.3984V19.5625C7.875 20.5 8.96875 20.8516 9.51562 20.1875L12.0156 17.1406L16.8594 19.2109C17.4062 19.4453 18.0703 19.0938 18.1484 18.4688L20.9609 1.59375C21.1172 0.8125 20.2578 0.265625 19.5938 0.65625Z"
                          fill="#383B4C"
                        />
                      </svg>
                    </div>
                  </div>
                </div>
              </v-row>
            </v-card>
          </div>
        </v-row>
      </v-row>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.button--left--outlined {
  background: transparent;
  outline: 1px solid var(--faded-color);
  height: 4.4rem !important;
  min-width: 13.7rem !important;
  border-radius: 4px;
  span {
    text-transform: initial;
    color: var(--faded-color);
    font-weight: var(--font-light);
    font-size: var(--normal-font-size);
  }
  svg {
    margin-left: 10px;
  }
}
.v-application--is-ltr .v-list-item__action:first-child,
.v-application--is-ltr .v-list-item__icon:first-child {
  margin-bottom: 0;
  margin-top: 20px;
  margin-right: 12px !important;
  padding-left: 5px;
}
</style>