<template>
  <div>
    <section id="pageBody">
      <v-row class="content_row">
        <!-- title  -->
        <div class="col-12 header_wrapper">
          <header>Content</header>
          <div class="header_wrapper-buttons">
            <v-btn
              @click="$refs.uploadBook.showDialogue()"
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
                  d="M8.09375 11.25C8.44922 11.25 8.75 10.9766 8.75 10.5938V6H11.1289C11.6211 6 11.8672 5.42578 11.5117 5.07031L7.35547 0.914062C7.16406 0.722656 6.80859 0.722656 6.61719 0.914062L2.46094 5.07031C2.10547 5.42578 2.35156 6 2.84375 6H5.25V10.5938C5.25 10.9766 5.52344 11.25 5.90625 11.25H8.09375ZM14 11.0312C14 10.6758 13.6992 10.375 13.3438 10.375H9.625V10.5938C9.625 11.4414 8.91406 12.125 8.09375 12.125H5.90625C5.05859 12.125 4.375 11.4414 4.375 10.5938V10.375H0.65625C0.273438 10.375 0 10.6758 0 11.0312V14.0938C0 14.4766 0.273438 14.75 0.65625 14.75H13.3438C13.6992 14.75 14 14.4766 14 14.0938V11.0312ZM10.6094 13.4375C10.6094 13.7383 10.3633 13.9844 10.0625 13.9844C9.76172 13.9844 9.51562 13.7383 9.51562 13.4375C9.51562 13.1367 9.76172 12.8906 10.0625 12.8906C10.3633 12.8906 10.6094 13.1367 10.6094 13.4375ZM12.3594 13.4375C12.3594 13.7383 12.1133 13.9844 11.8125 13.9844C11.5117 13.9844 11.2656 13.7383 11.2656 13.4375C11.2656 13.1367 11.5117 12.8906 11.8125 12.8906C12.1133 12.8906 12.3594 13.1367 12.3594 13.4375Z"
                  fill="#F88B2A"
                />
              </svg>

              <span>UPLOAD EBOOK</span>
            </v-btn>
            <v-btn
              to="/content/create"
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
              <span>CREATE CONTENT</span>
            </v-btn>
          </div>
        </div>
        <div style="padding-right: 0; padding-left: 24px" class="col-3">
          <!-- select card section -->
          <v-card class="select__card">
            <h3 class="select__card-header">SELECT CONTENT CLASS</h3>
            <v-expansion-panels
              focusable
              flat
              accordion
              class="select__card-tab"
            >
              <v-expansion-panel v-for="(item, index) in header" :key="index">
                <v-expansion-panel-header class="select__card-head">
                  <div>
                    <span>{{ item.title }}</span>
                  </div>
                  <template v-slot:actions>
                    <svg
                      width="9"
                      height="6"
                      viewBox="0 0 9 6"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M3.87109 5.00391C4.19922 5.35938 4.77344 5.35938 5.10156 5.00391L8.60156 1.50391C8.84766 1.25781 8.92969 0.875 8.79297 0.546875C8.65625 0.21875 8.35547 0 8 0H1C0.644531 0 0.316406 0.21875 0.179688 0.546875C0.0429688 0.875 0.125 1.25781 0.371094 1.50391L3.87109 5.00391Z"
                        fill="#000"
                      />
                    </svg>
                  </template>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  <v-list class="select__card-list">
                    <v-list-item
                      v-for="(items, index) in listItems"
                      :key="index"
                      class="select__card-list-item"
                      >{{ items.title }}</v-list-item
                    >
                  </v-list>
                </v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-card>
        </div>
        <div style="padding-left: 23px" class="col-9">
          <div>
            <v-tabs class="tab__container" v-model="tab" align-with-title>
              <v-tabs-slider color="var(--primary-color)"></v-tabs-slider>

              <v-tab :ripple="false" class="tab__container-item"> All </v-tab>
              <v-tab :ripple="false" class="tab__container-item">
                published
              </v-tab>
              <v-tab :ripple="false" class="tab__container-item"> Draft </v-tab>
              <v-tab :ripple="false" class="tab__container-item">
                Archived
              </v-tab>
            </v-tabs>
          </div>

          <!-- table  -->
          <div>
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
              <!-- topic  -->
              <template v-slot:item.topic="{ item }">
                <div class="user_content">
                  <p>{{ item.topic }}</p>
                </div>
              </template>
              <!-- week -->
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
              <!-- category  -->
              <template v-slot:item.category="{ item }">
                <div class="user_content">
                  <p class="category">{{ item.category }}</p>
                </div>
              </template>
              <!-- status  -->
              <template v-slot:item.status="{ item }">
                <div class="user_content">
                  <p class="status" v-if="item.status == 'published'">
                    {{ item.status }}
                  </p>
                  <p class="status draft" v-if="item.status == 'draft'">
                    {{ item.status }}
                  </p>
                  <p class="status danger" v-if="item.status == 'archived'">
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
        </div>
      </v-row>
    </section>
    <ModalUploadBook ref="uploadBook" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      tab: null,
      header: [
        { title: "jss 1 (year 7)" },
        { title: "jss 2 (year 8)" },
        { title: "jss 3 (year 9)" },
        { title: "sss 1 (year 10)" },
        { title: "sss 2 (year 11)" },
        { title: "sss 3 (year 12)" },
      ],
      listItems: [
        { title: "MATHEMATICS" },
        { title: "ENGLISH" },
        { title: "LITERATURE" },
        { title: "BIOLOGY" },
        { title: "ECONOMICS" },
        { title: "CIVIC EDUCATION" },
        { title: "COMPUTER STUDIES" },
        { title: "PHYSICS" },
        { title: "CHEMISTRY" },
        { title: "GOVERNMENT" },
        { title: "COMMERCE" },
      ],

      selected: [],
      headers: [
        {
          text: "Topic",
          align: "start",
          value: "topic",
        },
        { text: "Week", value: "week" },
        { text: "ID", value: "id" },
        { text: "Category", value: "category" },
        { text: "Status", value: "status" },
        { text: "Author", value: "author" },
        { text: "Actions", value: "action" },
      ],
      bookData: [
        {
          topic: "Human Rights",
          week: 3,
          id: 8755443346,
          category: "copy",
          status: "published",
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Inter-Personal Relationships",
          week: 3,
          id: 8755443346,
          category: "copy",
          status: "published",
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Citizenship & Nationalism.",
          week: 3,
          id: 8755443346,
          category: "test",
          status: "draft",
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Law and Order",
          week: 3,
          id: 8755443346,
          category: "test",
          status: "draft",
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Human Right",
          week: 3,
          id: 8755443346,
          category: "test",
          status: "draft",
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Law and Orders",
          week: 3,
          id: 8755443346,
          category: "test",
          status: "draft",
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Responsible Parenthood",
          week: 3,
          id: 8755443346,
          category: "test",
          status: "draft",
          author: "Kolawole Abraham",
          action: null,
        },
        {
          topic: "Traffic Regulations",
          week: 3,
          id: 8755443346,
          category: "test",
          status: "archived",
          author: "Kolawole Abraham",
          action: null,
        },
      ],
      footer: {
        options: { page: 1, itemsPerPage: 5 },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
</style>