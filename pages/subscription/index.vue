<template>
  <div>
    <section id="pageBody">
      <v-row class="content_row">
        <!-- title  -->
        <div style="padding-right: 24px" class="col-12 header_wrapper">
          <div style="display: flex; align-items: center; grid-gap: 25px">
            <header>Subscriptions</header>
            <v-menu nudge-bottom="5" bottom offset-y>
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  :ripple="false"
                  color="var(--faded-color))"
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
            <v-btn
              @click="$refs.addSub.showDialogue()"
              color="var(--primary-color)"
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
                  d="M7 0.96875C3.25391 0.96875 0.21875 4.00391 0.21875 7.75C0.21875 11.4961 3.25391 14.5312 7 14.5312C10.7461 14.5312 13.7812 11.4961 13.7812 7.75C13.7812 4.00391 10.7461 0.96875 7 0.96875ZM10.9375 8.51562C10.9375 8.70703 10.7734 8.84375 10.6094 8.84375H8.09375V11.3594C8.09375 11.5508 7.92969 11.6875 7.76562 11.6875H6.23438C6.04297 11.6875 5.90625 11.5508 5.90625 11.3594V8.84375H3.39062C3.19922 8.84375 3.0625 8.70703 3.0625 8.51562V6.98438C3.0625 6.82031 3.19922 6.65625 3.39062 6.65625H5.90625V4.14062C5.90625 3.97656 6.04297 3.8125 6.23438 3.8125H7.76562C7.92969 3.8125 8.09375 3.97656 8.09375 4.14062V6.65625H10.6094C10.7734 6.65625 10.9375 6.82031 10.9375 6.98438V8.51562Z"
                  fill="white"
                />
              </svg>
              <span>new subscription</span>
            </v-btn>
          </div>
        </div>
        <!-- analytics  -->
        <div class="col-12 row" style="margin: 0">
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>All</h3>
              <h4>345,900</h4>
              <span>57% increase</span>
            </v-card>
          </div>
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>Schools</h3>
              <h4>29,674</h4>
              <span>23% increase</span>
            </v-card>
          </div>
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>Individual</h3>
              <h4>311,519</h4>
              <span>10% increase</span>
            </v-card>
          </div>
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>Active</h3>
              <h4>315,890</h4>
              <span class="danger">2% decrease</span>
            </v-card>
          </div>
        </div>
        <div style="padding: 0 24px 12px" class="col-12">
          <!-- table  -->
          <div>
            <v-data-table
              v-model="selected"
              :headers="headers"
              :items="bookData"
              :single-select="false"
              item-key="name"
              :disable-filtering="true"
              :disable-pagination="false"
              :disable-sort="true"
              :items-per-page="10"
              checkbox-color="var(--primary-color)"
              :hide-default-footer="false"
              show-select
              class="generic_data_table"
            >
              <!-- name  -->
              <template v-slot:item.name="{ item }">
                <div class="user_content">
                  <p>{{ item.name }}</p>
                </div>
              </template>
              <!-- trans id-->
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
              <!-- No of Subscriptions  -->
              <template v-slot:item.category="{ item }">
                <div class="user_content">
                  <p>{{ item.category }}</p>
                </div>
              </template>
              <!-- No of Activations  -->
              <template v-slot:item.inactive="{ item }">
                <div class="user_content">
                  <p>
                    {{ item.inactive }}
                  </p>
                </div>
              </template>
              <!-- status  -->
              <template v-slot:item.status="{ item }">
                <div class="user_content">
                  <p class="status" v-if="item.status == 'Successful'">
                    {{ item.status }}
                  </p>
                  <p class="status draft" v-if="item.status == 'Pending'">
                    {{ item.status }}
                  </p>
                  <p class="status danger" v-if="item.status == 'Failed'">
                    {{ item.status }}
                  </p>
                </div>
              </template>
              <!-- author  -->
              <template v-slot:item.author="{ item }">
                <div class="user_content">
                  <p class="author">{{ item.author }}</p>
                </div>
              </template>
              <!-- actions  -->
              <template v-slot:item.action="{ item }">
                <div class="user_content">
                  <div class="table__actions">
                    <div>
                      <svg
                        @click="$refs.receipt.showDialogue()"
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
                        width="14"
                        height="15"
                        viewBox="0 0 14 15"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M10.5 0.5V4H14L10.5 0.5ZM9.625 4V0.5H4.8125C4.07422 0.5 3.5 1.10156 3.5 1.8125V8.375H8.25781L7.19141 7.30859C6.91797 7.0625 6.91797 6.65234 7.19141 6.40625C7.4375 6.13281 7.84766 6.13281 8.12109 6.40625L10.3086 8.59375C10.5547 8.83984 10.5547 9.25 10.3086 9.49609L8.12109 11.6836C7.84766 11.957 7.4375 11.957 7.19141 11.6836C7.05469 11.5742 7 11.4102 7 11.2188C7 11.0547 7.05469 10.8906 7.19141 10.7812L8.25781 9.6875H3.5V13.1875C3.5 13.9258 4.07422 14.5 4.8125 14.5H12.6875C13.3984 14.5 14 13.9258 14 13.1875V4.875H10.5C10.0078 4.875 9.625 4.49219 9.625 4ZM0.65625 8.375C0.273438 8.375 0 8.67578 0 9.03125C0 9.41406 0.273438 9.6875 0.65625 9.6875H3.5V8.375H0.65625Z"
                          fill="black"
                          fill-opacity="0.6"
                        />
                      </svg>
                    </div>
                    <div>
                      <svg
                        width="14"
                        height="15"
                        viewBox="0 0 14 15"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M13.125 10.125H9.46094L8.23047 11.3828C7.90234 11.7109 7.46484 11.875 7 11.875C6.50781 11.875 6.07031 11.7109 5.74219 11.3828L4.51172 10.125H0.875C0.382812 10.125 0 10.5352 0 11V13.625C0 14.1172 0.382812 14.5 0.875 14.5H13.125C13.5898 14.5 14 14.1172 14 13.625V11C14 10.5352 13.5898 10.125 13.125 10.125ZM11.8125 12.9688C11.4297 12.9688 11.1562 12.6953 11.1562 12.3125C11.1562 11.957 11.4297 11.6562 11.8125 11.6562C12.168 11.6562 12.4688 11.957 12.4688 12.3125C12.4688 12.6953 12.168 12.9688 11.8125 12.9688ZM6.37109 10.7539C6.53516 10.918 6.75391 11 7 11C7.21875 11 7.4375 10.918 7.60156 10.7539L11.1016 7.25391C11.457 6.92578 11.457 6.35156 11.1016 6.02344C10.7734 5.66797 10.1992 5.66797 9.87109 6.02344L7.875 8.01953V1.375C7.875 0.910156 7.46484 0.5 7 0.5C6.50781 0.5 6.125 0.910156 6.125 1.375V8.01953L4.10156 6.02344C3.77344 5.66797 3.19922 5.66797 2.87109 6.02344C2.51562 6.35156 2.51562 6.92578 2.87109 7.25391L6.37109 10.7539Z"
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
        </div>
      </v-row>
    </section>
    <ModalAddSub ref="addSub" />
    <ModalReceipt ref="receipt" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: [],
      headers: [
        {
          text: "User Name",
          align: "start",
          value: "name",
        },
        { text: "User ID", value: "id" },
        { text: "Category", value: "author" },
        { text: "No of Subscriptions", value: "category" },
        { text: "Transaction ID", value: "week" },
        { text: "Status", value: "status" },
        { text: "No of Activations", value: "inactive" },
        { text: "Actions", value: "action" },
      ],
      bookData: [
        {
          name: "Daniel Nwachukwu",
          week: 8755443346,
          id: 8755443346,
          category: 3,
          inactive: 1,
          author: "Individual",
          phone: "090123456786",
          email: "williams.ebube@gmail.com",
          status: "Successful",
          action: null,
        },
        {
          name: "Grange Secondary School",
          week: 8755443346,
          id: 8755443346,
          category: 600,
          inactive: 2,
          author: "School",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "Failed",
          action: null,
        },
        {
          name: "Dowen College",
          week: 8755443346,
          id: 8755443346,
          category: 12,
          inactive: "-",
          author: "School",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "Successful",
          action: null,
        },
        {
          name: "Mohamed Hauwa",
          week: 8755443346,
          id: 8755443346,
          category: 120,
          inactive: "-",
          author: "School",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "Pending",
          action: null,
        },
        {
          name: "Adeniyi Taiwo",
          week: 8755443346,
          id: 8755443346,
          category: 600,
          inactive: 60,
          author: "Eko Success Cloud",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "Successful",
          action: null,
        },
        {
          name: "High Flyer International School",
          week: 8755443346,
          id: 8755443346,
          category: 570,
          inactive: 1,
          author: "Eko Success Cloud",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "Pending",
          action: null,
        },
        {
          name: "Gopher Wood Montessori Sch..",
          week: 8755443346,
          id: 8755443346,
          category: 200,
          inactive: 22,
          author: "Eko Success Cloud",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "Successful",
          action: null,
        },
        {
          name: "Isiaka Ibrahim",
          week: 8755443346,
          id: 8755443346,
          category: 3,
          inactive: 30,
          author: "Individual",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "Successful",
          action: null,
        },
      ],
    };
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
</style>