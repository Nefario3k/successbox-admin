<template>
  <div>
    <section id="pageBody">
      <v-row class="content_row">
        <!-- title  -->
        <div style="padding-right: 24px" class="col-12 header_wrapper">
          <div style="display: flex; align-items: center; grid-gap: 25px">
            <header>Parents</header>
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
              outlined
              color="var(--primary-color)"
              class="button button--header button--outlined"
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
                  fill="#F88B2A"
                />
              </svg>

              <span>Bulk upload</span>
            </v-btn>
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
              <span>ADD Parent</span>
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
              <h3>New</h3>
              <h4>29,674</h4>
              <span>23% increase</span>
            </v-card>
          </div>
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>Active</h3>
              <h4>311,519</h4>
              <span>10% increase</span>
            </v-card>
          </div>
          <div class="col-6 col-md-3 col-lg-3 col-xl-3">
            <v-card class="analyticsCard">
              <h3>Inactive</h3>
              <h4>5,908</h4>
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
              <!-- TotNo of Wards -->
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
              <!-- School Affiliation  -->
              <template v-slot:item.category="{ item }">
                <div class="user_content">
                  <p>{{ item.category }}</p>
                </div>
              </template>
              <!-- School ID  -->
              <template v-slot:item.inactive="{ item }">
                <div class="user_content">
                  <p>{{ item.inactive }}</p>
                </div>
              </template>
              <!-- phone  -->
              <template v-slot:item.phone="{ item }">
                <div class="user_content">
                  <p>
                    <a :href="`tel:${item.phone}`">{{ item.phone }}</a>
                  </p>
                </div>
              </template>
              <!-- email  -->
              <template v-slot:item.email="{ item }">
                <div class="user_content">
                  <p>
                    <a :href="`mailto:${item.email}`">{{ item.email }}</a>
                  </p>
                </div>
              </template>
              <!-- status  -->
              <template v-slot:item.status="{ item }">
                <div class="user_content">
                  <p class="status" v-if="item.status == 'active'">
                    {{ item.status }}
                  </p>
                  <p class="status inactive" v-if="item.status == 'inactive'">
                    {{ item.status }}
                  </p>
                  <p class="status danger" v-if="item.status == 'churn'">
                    {{ item.status }}
                  </p>
                </div>
              </template>

              <!-- actions  -->
              <template v-slot:item.action="{ item }">
                <div class="user_content">
                  <div class="table__actions">
                    <nuxt-link to="/parent/525252662772">
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
                    </nuxt-link>
                    <div>
                      <svg
                        width="15"
                        height="15"
                        viewBox="0 0 15 15"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M10.4727 12.75H1.72266V4H5.98828L7.73828 2.25H1.72266C0.765625 2.25 0 3.04297 0 4V12.75C0 13.7344 0.765625 14.5 1.72266 14.5H10.4453C11.4023 14.5 12.168 13.7344 12.168 12.75V6.73438L10.4453 8.48438V12.75H10.4727ZM13.5898 1.67578L12.8242 0.910156C12.332 0.390625 11.4844 0.390625 10.9648 0.910156L9.92578 1.94922L12.5508 4.57422L13.5898 3.53516C14.1094 3.01562 14.1094 2.16797 13.5898 1.67578ZM4.01953 8.01953L3.5 10.6172C3.44531 10.8633 3.63672 11.0547 3.88281 11L6.48047 10.4805C6.61719 10.4531 6.72656 10.3984 6.80859 10.3164L11.9219 5.20312L9.29688 2.57812L4.18359 7.69141C4.10156 7.77344 4.04688 7.88281 4.01953 8.01953Z"
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
                    <div>
                      <svg
                        width="14"
                        height="15"
                        viewBox="0 0 14 15"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M1.75 13.1875C1.75 13.9258 2.32422 14.5 3.0625 14.5H10.9375C11.6484 14.5 12.25 13.9258 12.25 13.1875V4H1.75V13.1875ZM9.1875 6.1875C9.1875 5.96875 9.37891 5.75 9.625 5.75C9.84375 5.75 10.0625 5.96875 10.0625 6.1875V12.3125C10.0625 12.5586 9.84375 12.75 9.625 12.75C9.37891 12.75 9.1875 12.5586 9.1875 12.3125V6.1875ZM6.5625 6.1875C6.5625 5.96875 6.75391 5.75 7 5.75C7.21875 5.75 7.4375 5.96875 7.4375 6.1875V12.3125C7.4375 12.5586 7.21875 12.75 7 12.75C6.75391 12.75 6.5625 12.5586 6.5625 12.3125V6.1875ZM3.9375 6.1875C3.9375 5.96875 4.12891 5.75 4.375 5.75C4.59375 5.75 4.8125 5.96875 4.8125 6.1875V12.3125C4.8125 12.5586 4.59375 12.75 4.375 12.75C4.12891 12.75 3.9375 12.5586 3.9375 12.3125V6.1875ZM12.6875 1.375H9.625L9.29688 0.746094C9.21484 0.609375 9.07812 0.5 8.91406 0.5H5.05859C4.89453 0.5 4.75781 0.609375 4.67578 0.746094L4.375 1.375H1.3125C1.06641 1.375 0.875 1.59375 0.875 1.8125V2.6875C0.875 2.93359 1.06641 3.125 1.3125 3.125H12.6875C12.9062 3.125 13.125 2.93359 13.125 2.6875V1.8125C13.125 1.59375 12.9062 1.375 12.6875 1.375Z"
                          fill="#B00020"
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
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: [],
      headers: [
        {
          text: "Full Name",
          align: "start",
          value: "name",
        },
        { text: "ID", value: "id" },
        { text: "No of Wards", value: "week" },
        { text: "School Affiliation", value: "category" },
        { text: "School ID", value: "inactive" },
        { text: "Phone", value: "phone" },
        { text: "Email", value: "email" },
        { text: "Status", value: "status" },
        { text: "Actions", value: "action" },
      ],
      bookData: [
        {
          name: "Human Rights",
          week: 3,
          id: 8755443346,
          category: "Atlantic Hall College",
          inactive: 7876856869,
          author: "Kolawole Abraham",
          phone: "090123456786",
          email: "williams.ebube@gmail.com",
          status: "active",
          action: null,
        },
        {
          name: "Inter-Personal Relationships",
          week: 3,
          id: 8755443346,
          category: "Atlantic Hall College",
          inactive: 7876856869,
          author: "Kolawole Abraham",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "churn",
          action: null,
        },
        {
          name: "Citizenship & Nationalism.",
          week: 3,
          id: 8755443346,
          category: "-",
          inactive: 7876856869,
          author: "Kolawole Abraham",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "active",
          action: null,
        },
        {
          name: "Law and Order",
          week: 3,
          id: 8755443346,
          category: "Green Springs College",
          inactive: 7876856869,
          author: "Kolawole Abraham",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "inactive",
          action: null,
        },
        {
          name: "Human Right",
          week: 3,
          id: 8755443346,
          category: "Green Springs College",
          inactive: 8755443346,
          author: "Kolawole Abraham",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "active",
          action: null,
        },
        {
          name: "Law and Orders",
          week: 3,
          id: 8755443346,
          category: "-",
          inactive: 8755443346,
          author: "Kolawole Abraham",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "inactive",
          action: null,
        },
        {
          name: "Responsible Parenthood",
          week: 3,
          id: 8755443346,
          category: "Green Springs College",
          inactive: 8755443346,
          author: "Kolawole Abraham",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "active",
          action: null,
        },
        {
          name: "Traffic Regulations",
          week: 3,
          id: 8755443346,
          category: "Green Springs College",
          inactive: 8755443346,
          author: "Kolawole Abraham",
          phone: "090123456789",
          email: "williams.ebube@gmail.com",
          status: "active",
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