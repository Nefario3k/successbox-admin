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
            <header class="mini__header">
              <span>Year7/Civic Education/</span>Inter-Personal Relationships
            </header>
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
                  d="M11.3125 6.875H10.6562V4.90625C10.6562 2.63672 8.76953 0.75 6.5 0.75C4.20312 0.75 2.34375 2.63672 2.34375 4.90625V6.875H1.6875C0.949219 6.875 0.375 7.47656 0.375 8.1875V13.4375C0.375 14.1758 0.949219 14.75 1.6875 14.75H11.3125C12.0234 14.75 12.625 14.1758 12.625 13.4375V8.1875C12.625 7.47656 12.0234 6.875 11.3125 6.875ZM8.46875 6.875H4.53125V4.90625C4.53125 3.83984 5.40625 2.9375 6.5 2.9375C7.56641 2.9375 8.46875 3.83984 8.46875 4.90625V6.875Z"
                  fill="#F88B2A"
                />
              </svg>

              <span>ARCHIVE </span>
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
                  d="M8.09375 11.25C8.44922 11.25 8.75 10.9766 8.75 10.5938V6H11.1289C11.6211 6 11.8672 5.42578 11.5117 5.07031L7.35547 0.914062C7.16406 0.722656 6.80859 0.722656 6.61719 0.914062L2.46094 5.07031C2.10547 5.42578 2.35156 6 2.84375 6H5.25V10.5938C5.25 10.9766 5.52344 11.25 5.90625 11.25H8.09375ZM14 11.0312C14 10.6758 13.6992 10.375 13.3438 10.375H9.625V10.5938C9.625 11.4414 8.91406 12.125 8.09375 12.125H5.90625C5.05859 12.125 4.375 11.4414 4.375 10.5938V10.375H0.65625C0.273438 10.375 0 10.6758 0 11.0312V14.0938C0 14.4766 0.273438 14.75 0.65625 14.75H13.3438C13.6992 14.75 14 14.4766 14 14.0938V11.0312ZM10.6094 13.4375C10.6094 13.7383 10.3633 13.9844 10.0625 13.9844C9.76172 13.9844 9.51562 13.7383 9.51562 13.4375C9.51562 13.1367 9.76172 12.8906 10.0625 12.8906C10.3633 12.8906 10.6094 13.1367 10.6094 13.4375ZM12.3594 13.4375C12.3594 13.7383 12.1133 13.9844 11.8125 13.9844C11.5117 13.9844 11.2656 13.7383 11.2656 13.4375C11.2656 13.1367 11.5117 12.8906 11.8125 12.8906C12.1133 12.8906 12.3594 13.1367 12.3594 13.4375Z"
                  fill="white"
                />
              </svg>

              <span>UPLOAD</span>
            </v-btn>
          </div>
        </div>

        <!-- form  -->
        <form autocomplete="off" class="col-12 row row_form">
          <!-- course  -->
          <div class="col-6 inputArea">
            <v-menu
              max-height="240"
              v-model="course"
              bottom
              :nudge-bottom="5"
              offset-y
            >
              <template v-slot:activator="{ on, attrs }">
                <div class="relative" v-bind="attrs" v-on="on">
                  <input
                    :class="{ active: course }"
                    style="cursor: pointer !important"
                    disabled
                    required
                    type="text"
                    placeholder="Select option"
                    v-model="course_list[5].title"
                  />
                  <div class="absolute dropdownSvg">
                    <svg
                      width="17"
                      height="16"
                      viewBox="0 0 17 16"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M13.2361 5.55738C13.1653 5.48597 13.0811 5.4293 12.9882 5.39062C12.8954 5.35194 12.7958 5.33203 12.6953 5.33203C12.5947 5.33203 12.4951 5.35194 12.4023 5.39062C12.3094 5.4293 12.2252 5.48597 12.1544 5.55738L8.66524 9.0465C8.59442 9.1179 8.51016 9.17457 8.41733 9.21325C8.32449 9.25193 8.22492 9.27184 8.12435 9.27184C8.02378 9.27184 7.92421 9.25193 7.83137 9.21325C7.73854 9.17457 7.65428 9.1179 7.58346 9.0465L4.09433 5.55738C4.02351 5.48597 3.93925 5.4293 3.84642 5.39062C3.75358 5.35194 3.65401 5.33203 3.55344 5.33203C3.45287 5.33203 3.35329 5.35194 3.26046 5.39062C3.16763 5.4293 3.08337 5.48597 3.01255 5.55738C2.87066 5.70011 2.79102 5.89319 2.79102 6.09446C2.79102 6.29572 2.87066 6.4888 3.01255 6.63154L6.50929 10.1283C6.93782 10.5563 7.5187 10.7967 8.12435 10.7967C8.73 10.7967 9.31088 10.5563 9.7394 10.1283L13.2361 6.63154C13.378 6.4888 13.4577 6.29572 13.4577 6.09446C13.4577 5.89319 13.378 5.70011 13.2361 5.55738Z"
                        fill="#142232"
                      />
                    </svg>
                  </div>
                </div>
              </template>
              <v-list elevation="0" flat class="dropdownList">
                <v-list-item
                  v-for="(item, index) in course_list"
                  :key="index"
                  class="list_item"
                >
                  <v-list-item-title class="list_title">{{
                    item.title
                  }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>
          <!-- course type  -->
          <div class="col-6 inputArea">
            <v-menu
              max-height="240"
              v-model="test_type"
              bottom
              :nudge-bottom="5"
              offset-y
            >
              <template v-slot:activator="{ on, attrs }">
                <div class="relative" v-bind="attrs" v-on="on">
                  <input
                    :class="{ active: test_type }"
                    style="cursor: pointer !important"
                    disabled
                    required
                    type="text"
                    placeholder="Select option"
                    v-model="tab_list[test_type_tab].title"
                  />
                  <div class="absolute dropdownSvg">
                    <svg
                      width="17"
                      height="16"
                      viewBox="0 0 17 16"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M13.2361 5.55738C13.1653 5.48597 13.0811 5.4293 12.9882 5.39062C12.8954 5.35194 12.7958 5.33203 12.6953 5.33203C12.5947 5.33203 12.4951 5.35194 12.4023 5.39062C12.3094 5.4293 12.2252 5.48597 12.1544 5.55738L8.66524 9.0465C8.59442 9.1179 8.51016 9.17457 8.41733 9.21325C8.32449 9.25193 8.22492 9.27184 8.12435 9.27184C8.02378 9.27184 7.92421 9.25193 7.83137 9.21325C7.73854 9.17457 7.65428 9.1179 7.58346 9.0465L4.09433 5.55738C4.02351 5.48597 3.93925 5.4293 3.84642 5.39062C3.75358 5.35194 3.65401 5.33203 3.55344 5.33203C3.45287 5.33203 3.35329 5.35194 3.26046 5.39062C3.16763 5.4293 3.08337 5.48597 3.01255 5.55738C2.87066 5.70011 2.79102 5.89319 2.79102 6.09446C2.79102 6.29572 2.87066 6.4888 3.01255 6.63154L6.50929 10.1283C6.93782 10.5563 7.5187 10.7967 8.12435 10.7967C8.73 10.7967 9.31088 10.5563 9.7394 10.1283L13.2361 6.63154C13.378 6.4888 13.4577 6.29572 13.4577 6.09446C13.4577 5.89319 13.378 5.70011 13.2361 5.55738Z"
                        fill="#142232"
                      />
                    </svg>
                  </div>
                </div>
              </template>
              <v-list elevation="0" flat class="dropdownList">
                <v-list-item
                  @click="test_type_tab = index"
                  v-for="(item, index) in tab_list"
                  :key="index"
                  class="list_item"
                >
                  <v-list-item-title class="list_title">{{
                    item.title
                  }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>

          <!-- book  -->
          <div v-if="test_type_tab != 2" class="col-12 inputArea">
            <input
              autocomplete="false"
              required
              type="text"
              placeholder="Book"
              value="INTER-PERSONAL RELATIONSHIPS"
              id="description"
            />
          </div>
          <template v-else>
            <div class="col-6 inputArea">
              <input
                autocomplete="false"
                disabled
                type="number"
                placeholder="questions"
                v-model="standard_number"
              />
            </div>

            <div class="col-6 inputArea">
              <v-menu
                max-height="240"
                v-model="test_time"
                bottom
                :nudge-bottom="5"
                offset-y
              >
                <template v-slot:activator="{ on, attrs }">
                  <div class="relative" v-bind="attrs" v-on="on">
                    <input
                      :class="{ active: test_time }"
                      style="cursor: pointer !important"
                      disabled
                      required
                      type="text"
                      placeholder="Select option"
                      v-model="time[1].title"
                    />
                    <div class="absolute dropdownSvg">
                      <svg
                        width="17"
                        height="16"
                        viewBox="0 0 17 16"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M13.2361 5.55738C13.1653 5.48597 13.0811 5.4293 12.9882 5.39062C12.8954 5.35194 12.7958 5.33203 12.6953 5.33203C12.5947 5.33203 12.4951 5.35194 12.4023 5.39062C12.3094 5.4293 12.2252 5.48597 12.1544 5.55738L8.66524 9.0465C8.59442 9.1179 8.51016 9.17457 8.41733 9.21325C8.32449 9.25193 8.22492 9.27184 8.12435 9.27184C8.02378 9.27184 7.92421 9.25193 7.83137 9.21325C7.73854 9.17457 7.65428 9.1179 7.58346 9.0465L4.09433 5.55738C4.02351 5.48597 3.93925 5.4293 3.84642 5.39062C3.75358 5.35194 3.65401 5.33203 3.55344 5.33203C3.45287 5.33203 3.35329 5.35194 3.26046 5.39062C3.16763 5.4293 3.08337 5.48597 3.01255 5.55738C2.87066 5.70011 2.79102 5.89319 2.79102 6.09446C2.79102 6.29572 2.87066 6.4888 3.01255 6.63154L6.50929 10.1283C6.93782 10.5563 7.5187 10.7967 8.12435 10.7967C8.73 10.7967 9.31088 10.5563 9.7394 10.1283L13.2361 6.63154C13.378 6.4888 13.4577 6.29572 13.4577 6.09446C13.4577 5.89319 13.378 5.70011 13.2361 5.55738Z"
                          fill="#142232"
                        />
                      </svg>
                    </div>
                  </div>
                </template>
                <v-list elevation="0" flat class="dropdownList">
                  <v-list-item
                    v-for="(item, index) in time"
                    :key="index"
                    class="list_item"
                  >
                    <v-list-item-title class="list_title">{{
                      item.title
                    }}</v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-menu>
            </div>
          </template>

          <v-row class="col-12" style="padding: 0">
            <v-tabs-items
              class="col-12"
              style="padding: 0"
              v-model="test_type_tab"
            >
              <!-- copy tab  -->
              <v-tab-item>
                <!-- header  -->
                <div class="col-12 edit_section_header">
                  <header><span>CREATE COPY</span></header>
                </div>

                <!-- rich text editor  -->
                <div class="col-12 inputArea editor">
                  <div class="text_editor">
                    <client-only>
                      <VueEditor
                        id="editor"
                        v-model="description"
                        placeholder="Description"
                      />
                    </client-only>
                  </div>
                </div>

                <div class="btn__area col-12">
                  <v-btn color="#383B4C" class="Btn"
                    ><svg
                      width="14"
                      height="13"
                      viewBox="0 0 14 13"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M2.625 0.625C1.64062 0.625 0.875 1.41797 0.875 2.375V11.125C0.875 12.1094 1.64062 12.875 2.625 12.875H11.375C12.332 12.875 13.125 12.1094 13.125 11.125V4.50781C13.125 4.04297 12.9336 3.57812 12.6055 3.25L10.5 1.14453C10.1719 0.816406 9.70703 0.625 9.24219 0.625H2.625ZM2.625 3.25C2.625 2.78516 3.00781 2.375 3.5 2.375H8.75C9.21484 2.375 9.625 2.78516 9.625 3.25V5C9.625 5.49219 9.21484 5.875 8.75 5.875H3.5C3.00781 5.875 2.625 5.49219 2.625 5V3.25ZM7 11.125C6.01562 11.125 5.25 10.3594 5.25 9.375C5.25 8.41797 6.01562 7.625 7 7.625C7.95703 7.625 8.75 8.41797 8.75 9.375C8.75 10.3594 7.95703 11.125 7 11.125Z"
                        fill="white"
                      />
                    </svg>
                    <span>save</span></v-btn
                  >
                  <v-btn color="#F88B2A" class="Btn publish"
                    ><svg
                      width="11"
                      height="15"
                      viewBox="0 0 11 15"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M0.25 2.5C0.25 1.54297 1.01562 0.75 2 0.75H6.375V4.25C6.375 4.74219 6.75781 5.125 7.25 5.125H10.75V13C10.75 13.9844 9.95703 14.75 9 14.75H2C1.01562 14.75 0.25 13.9844 0.25 13V2.5ZM10.75 4.25H7.25V0.75L10.75 4.25Z"
                        fill="white"
                      />
                    </svg>
                    <span>publish</span></v-btn
                  >
                </div>
              </v-tab-item>

              <!-- weekly test tab  -->
              <v-tab-item class="row col-12">
                <!-- questions area  -->
                <v-row
                  style="padding: 12px 0; height: max-content"
                  class="col-6"
                >
                  <!-- header  -->
                  <div
                    style="padding-bottom: 0; height: max-content"
                    class="col-12 edit_section_header"
                  >
                    <header>
                      <span>QUESTION</span>
                      <div class="weekly__tab">
                        <span
                          @click="tabWeekly('prev')"
                          class="weekly__tab-nav left"
                          ><svg
                            width="8"
                            height="13"
                            viewBox="0 0 8 13"
                            fill="none"
                            xmlns="http://www.w3.org/2000/svg"
                          >
                            <path
                              d="M5.35156 12.3984L0.351562 7.4375C0.117188 7.16406 0 6.85156 0 6.5C0 6.10938 0.117188 5.83594 0.351562 5.60156L5.35156 0.640625C5.70312 0.289062 6.25 0.171875 6.71875 0.367188C7.1875 0.5625 7.5 1.03125 7.5 1.5V11.5C7.5 12.0078 7.1875 12.4375 6.71875 12.6328C6.25 12.8281 5.70312 12.75 5.35156 12.3984Z"
                              fill="#383B4C"
                            />
                          </svg>
                        </span>
                        <span class="weekly__tab-counter"
                          >{{ test_type_tab_weekly + 1 }}/5</span
                        >
                        <span
                          @click="tabWeekly('next')"
                          class="weekly__tab-nav right"
                        >
                          <svg
                            width="8"
                            height="13"
                            viewBox="0 0 8 13"
                            fill="none"
                            xmlns="http://www.w3.org/2000/svg"
                          >
                            <path
                              d="M2.60938 0.640625L7.60938 5.60156C7.84375 5.875 8 6.1875 8 6.5C8 6.77344 7.84375 7.125 7.60938 7.35938L2.60938 12.3203C2.25781 12.6719 1.71094 12.7891 1.24219 12.5938C0.773438 12.3984 0.5 12.0078 0.5 11.5V1.5C0.5 1.03125 0.773438 0.5625 1.24219 0.367188C1.71094 0.171875 2.25781 0.289062 2.60938 0.640625Z"
                              fill="#383B4C"
                            />
                          </svg>
                        </span>
                      </div>
                    </header>
                  </div>
                  <v-tabs-items class="col-12" v-model="test_type_tab_weekly">
                    <v-tab-item v-for="loop in 5" :key="loop">
                      <div class="weekly__question">
                        <!-- title  -->
                        <h3 class="weekly__question-title">
                          Enter question here
                        </h3>
                        <!-- question  -->
                        <div>
                          <textarea
                            rows=""
                            cols=""
                            placeholder="Select Topic"
                          ></textarea>
                          <v-btn outlined color="#383B4C" class="attach_btn">
                            <svg
                              width="19"
                              height="21"
                              viewBox="0 0 19 21"
                              fill="none"
                              xmlns="http://www.w3.org/2000/svg"
                            >
                              <path
                                d="M15.4688 3.78125C14.4922 2.84375 12.9688 2.84375 11.9922 3.78125L4.80469 10.9688C3.16406 12.6094 3.16406 15.3047 4.80469 16.9453C6.44531 18.5859 9.14062 18.5859 10.7812 16.9453L16.7188 11.0078C17.1484 10.5781 17.8125 10.5781 18.2422 11.0078C18.6719 11.4375 18.6719 12.1016 18.2422 12.5312L12.3047 18.4688C9.80469 20.9688 5.78125 20.9688 3.28125 18.4688C0.78125 15.9688 0.78125 11.9453 3.28125 9.44531L10.4688 2.25781C12.2656 0.421875 15.1953 0.421875 16.9922 2.25781C18.8281 4.05469 18.8281 6.98438 16.9922 8.78125L10.1172 15.6562C9.02344 16.7891 7.1875 16.7891 6.09375 15.6562C4.96094 14.5625 4.96094 12.7266 6.09375 11.6328L11.7188 6.00781C12.1484 5.57812 12.8125 5.57812 13.2422 6.00781C13.6719 6.4375 13.6719 7.10156 13.2422 7.53125L7.61719 13.1562C7.38281 13.4297 7.38281 13.8594 7.61719 14.1328C7.89062 14.3672 8.32031 14.3672 8.59375 14.1328L15.4688 7.25781C16.4062 6.28125 16.4062 4.75781 15.4688 3.78125Z"
                                fill="#383B4C"
                              />
                            </svg>

                            <span>attach image</span>
                          </v-btn>
                        </div>
                        <!-- title  -->
                        <h3 class="weekly__question-title">
                          Enter answer options, and select correct answer
                        </h3>
                        <!-- options  -->
                        <div class="weekly__question-options">
                          <div v-for="n in 5" :key="n" class="relative">
                            <input
                              type="text"
                              :placeholder="`Enter option ${n}`"
                            />
                            <div class="absolute">
                              <svg
                                width="24"
                                height="24"
                                viewBox="0 0 24 24"
                                fill="none"
                                xmlns="http://www.w3.org/2000/svg"
                              >
                                <path
                                  d="M12 24C18.6094 24 24 18.6562 24 12C24 5.39062 18.6094 0 12 0C5.34375 0 0 5.39062 0 12C0 18.6562 5.34375 24 12 24ZM17.2969 9.79688L11.2969 15.7969C10.8281 16.2656 10.125 16.2656 9.70312 15.7969L6.70312 12.7969C6.23438 12.375 6.23438 11.6719 6.70312 11.25C7.125 10.7812 7.82812 10.7812 8.29688 11.25L10.5 13.4531L15.7031 8.20312C16.125 7.78125 16.8281 7.78125 17.25 8.20312C17.7188 8.67188 17.7188 9.375 17.25 9.79688H17.2969Z"
                                  fill="#A1A1A1"
                                />
                              </svg>
                            </div>
                          </div>
                        </div>
                      </div>
                    </v-tab-item>
                  </v-tabs-items>
                </v-row>
                <v-row
                  style="
                    padding: 0;
                    max-width: calc(50% - 12px) !important;
                    height: auto;
                    background: #fff;
                    margin: 12px 0 24px 12px !important;
                    border: 1px solid rgba(179, 172, 182, 0.5);
                  "
                  class="col-6"
                >
                  <v-tabs-items
                    style="padding: 0 0 0 12px; height: inherit"
                    class="col-12"
                    v-model="test_type_tab_weekly"
                  >
                    <v-tab-item
                      v-for="loop in 5"
                      :key="loop"
                      class="row weekly__question-preview"
                    >
                      <!-- header  -->
                      <div class="col-12 edit_section_header">
                        <header>
                          <span>PREVIEW</span>
                        </header>
                      </div>
                      <div class="col-12 weekly__question-question">
                        <div>
                          <span>How does an acid differ from a base?</span>
                        </div>
                      </div>
                      <div class="col-12 weekly__question-preview-options">
                        <div>
                          <!-- loop item below -->
                          <div v-for="n in 5" :key="n">
                            <svg
                              width="39"
                              height="34"
                              viewBox="0 0 39 34"
                              fill="none"
                              xmlns="http://www.w3.org/2000/svg"
                            >
                              <ellipse
                                cx="19.748"
                                cy="16.9004"
                                rx="18.9252"
                                ry="16.5"
                                fill="#B3ACB6"
                              />
                            </svg>
                            <span
                              >An acid releases hydroxide (OH–) ions, whereas a
                              base releases hydrogen ions (H+)</span
                            >
                          </div>
                        </div>
                      </div>
                    </v-tab-item>
                  </v-tabs-items>
                </v-row>
                <div class="btn__area col-12">
                  <v-btn color="#383B4C" class="Btn"
                    ><svg
                      width="14"
                      height="13"
                      viewBox="0 0 14 13"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M2.625 0.625C1.64062 0.625 0.875 1.41797 0.875 2.375V11.125C0.875 12.1094 1.64062 12.875 2.625 12.875H11.375C12.332 12.875 13.125 12.1094 13.125 11.125V4.50781C13.125 4.04297 12.9336 3.57812 12.6055 3.25L10.5 1.14453C10.1719 0.816406 9.70703 0.625 9.24219 0.625H2.625ZM2.625 3.25C2.625 2.78516 3.00781 2.375 3.5 2.375H8.75C9.21484 2.375 9.625 2.78516 9.625 3.25V5C9.625 5.49219 9.21484 5.875 8.75 5.875H3.5C3.00781 5.875 2.625 5.49219 2.625 5V3.25ZM7 11.125C6.01562 11.125 5.25 10.3594 5.25 9.375C5.25 8.41797 6.01562 7.625 7 7.625C7.95703 7.625 8.75 8.41797 8.75 9.375C8.75 10.3594 7.95703 11.125 7 11.125Z"
                        fill="white"
                      />
                    </svg>
                    <span>save</span></v-btn
                  >
                  <v-btn disabled color="#F88B2A" class="Btn publish"
                    ><svg
                      width="11"
                      height="15"
                      viewBox="0 0 11 15"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M0.25 2.5C0.25 1.54297 1.01562 0.75 2 0.75H6.375V4.25C6.375 4.74219 6.75781 5.125 7.25 5.125H10.75V13C10.75 13.9844 9.95703 14.75 9 14.75H2C1.01562 14.75 0.25 13.9844 0.25 13V2.5ZM10.75 4.25H7.25V0.75L10.75 4.25Z"
                        fill="white"
                      />
                    </svg>
                    <span>publish</span></v-btn
                  >
                </div>
              </v-tab-item>

              <!-- standard test tab  -->
              <v-tab-item class="row col-12">
                <!-- questions area  -->
                <v-row
                  style="padding: 12px 0; height: max-content"
                  class="col-6"
                >
                  <!-- header  -->
                  <div
                    style="padding-bottom: 0; height: max-content"
                    class="col-12 edit_section_header"
                  >
                    <header>
                      <span>QUESTION</span>
                      <div
                        style="
                          display: flex;
                          align-items: center;
                          flex-wrap: wrap;
                          gap: 12px;
                        "
                      >
                        <span class="control__tab">Previous</span>
                        <v-menu
                          max-height="240"
                          v-model="tab_standard_dropdown"
                          bottom
                          :nudge-bottom="5"
                          offset-y
                        >
                          <template v-slot:activator="{ on, attrs }">
                            <div
                              v-bind="attrs"
                              v-on="on"
                              class="weekly__tab standard"
                            >
                              <span class="weekly__tab-counter"
                                >{{ test_type_tab_standard + 1 }}/{{
                                  standard_number
                                }}</span
                              >
                              <span class="standard__tab">
                                <svg
                                  width="14"
                                  height="8"
                                  viewBox="0 0 14 8"
                                  fill="none"
                                  xmlns="http://www.w3.org/2000/svg"
                                >
                                  <path
                                    d="M6.10156 7.14844C6.57031 7.65625 7.39062 7.65625 7.85938 7.14844L12.8594 2.14844C13.2109 1.79688 13.3281 1.25 13.1328 0.78125C12.9375 0.3125 12.5078 0 12 0H2C1.49219 0 1.02344 0.3125 0.828125 0.78125C0.632812 1.25 0.75 1.79688 1.10156 2.14844L6.10156 7.14844Z"
                                    fill="#383B4C"
                                  />
                                </svg>
                              </span>
                            </div>
                          </template>
                          <v-list elevation="0" flat class="dropdownList">
                            <v-list-item
                              v-for="(item, index) in standard_number"
                              :key="index"
                              class="list_item"
                            >
                              <v-list-item-title class="list_title">{{
                                item
                              }}</v-list-item-title>
                            </v-list-item>
                          </v-list>
                        </v-menu>
                        <span class="control__tab">Next</span>
                      </div>
                    </header>
                  </div>
                  <v-tabs-items class="col-12" v-model="test_type_tab_standard">
                    <v-tab-item v-for="loop in 5" :key="loop">
                      <div class="weekly__question">
                        <!-- title  -->
                        <h3 class="weekly__question-title">
                          Enter question here
                        </h3>
                        <!-- question  -->
                        <div>
                          <textarea
                            rows=""
                            cols=""
                            placeholder="Select Topic"
                          ></textarea>
                          <v-btn outlined color="#383B4C" class="attach_btn">
                            <svg
                              width="19"
                              height="21"
                              viewBox="0 0 19 21"
                              fill="none"
                              xmlns="http://www.w3.org/2000/svg"
                            >
                              <path
                                d="M15.4688 3.78125C14.4922 2.84375 12.9688 2.84375 11.9922 3.78125L4.80469 10.9688C3.16406 12.6094 3.16406 15.3047 4.80469 16.9453C6.44531 18.5859 9.14062 18.5859 10.7812 16.9453L16.7188 11.0078C17.1484 10.5781 17.8125 10.5781 18.2422 11.0078C18.6719 11.4375 18.6719 12.1016 18.2422 12.5312L12.3047 18.4688C9.80469 20.9688 5.78125 20.9688 3.28125 18.4688C0.78125 15.9688 0.78125 11.9453 3.28125 9.44531L10.4688 2.25781C12.2656 0.421875 15.1953 0.421875 16.9922 2.25781C18.8281 4.05469 18.8281 6.98438 16.9922 8.78125L10.1172 15.6562C9.02344 16.7891 7.1875 16.7891 6.09375 15.6562C4.96094 14.5625 4.96094 12.7266 6.09375 11.6328L11.7188 6.00781C12.1484 5.57812 12.8125 5.57812 13.2422 6.00781C13.6719 6.4375 13.6719 7.10156 13.2422 7.53125L7.61719 13.1562C7.38281 13.4297 7.38281 13.8594 7.61719 14.1328C7.89062 14.3672 8.32031 14.3672 8.59375 14.1328L15.4688 7.25781C16.4062 6.28125 16.4062 4.75781 15.4688 3.78125Z"
                                fill="#383B4C"
                              />
                            </svg>

                            <span>attach image</span>
                          </v-btn>
                        </div>
                        <!-- title  -->
                        <h3 class="weekly__question-title">
                          Enter answer options, and select correct answer
                        </h3>
                        <!-- options  -->
                        <div class="weekly__question-options">
                          <div v-for="n in 5" :key="n" class="relative">
                            <input
                              type="text"
                              :placeholder="`Enter option ${n}`"
                            />
                            <div class="absolute">
                              <svg
                                width="24"
                                height="24"
                                viewBox="0 0 24 24"
                                fill="none"
                                xmlns="http://www.w3.org/2000/svg"
                              >
                                <path
                                  d="M12 24C18.6094 24 24 18.6562 24 12C24 5.39062 18.6094 0 12 0C5.34375 0 0 5.39062 0 12C0 18.6562 5.34375 24 12 24ZM17.2969 9.79688L11.2969 15.7969C10.8281 16.2656 10.125 16.2656 9.70312 15.7969L6.70312 12.7969C6.23438 12.375 6.23438 11.6719 6.70312 11.25C7.125 10.7812 7.82812 10.7812 8.29688 11.25L10.5 13.4531L15.7031 8.20312C16.125 7.78125 16.8281 7.78125 17.25 8.20312C17.7188 8.67188 17.7188 9.375 17.25 9.79688H17.2969Z"
                                  fill="#A1A1A1"
                                />
                              </svg>
                            </div>
                          </div>
                        </div>
                      </div>
                    </v-tab-item>
                  </v-tabs-items>
                </v-row>
                <v-row
                  style="
                    padding: 0;
                    max-width: calc(50% - 12px) !important;
                    height: auto;
                    background: #fff;
                    margin: 12px 0 24px 12px !important;
                    border: 1px solid rgba(179, 172, 182, 0.5);
                  "
                  class="col-6"
                >
                  <v-tabs-items
                    style="padding: 0 0 0 12px; height: inherit"
                    class="col-12"
                    v-model="test_type_tab_standard"
                  >
                    <v-tab-item
                      v-for="loop in 5"
                      :key="loop"
                      class="row weekly__question-preview"
                    >
                      <!-- header  -->
                      <div class="col-12 edit_section_header">
                        <header>
                          <span>PREVIEW</span>
                        </header>
                      </div>
                      <div class="col-12 weekly__question-question">
                        <div>
                          <span>How does an acid differ from a base?</span>
                        </div>
                      </div>
                      <div class="col-12 weekly__question-preview-options">
                        <div>
                          <!-- loop item below -->
                          <div v-for="n in 5" :key="n">
                            <svg
                              width="39"
                              height="34"
                              viewBox="0 0 39 34"
                              fill="none"
                              xmlns="http://www.w3.org/2000/svg"
                            >
                              <ellipse
                                cx="19.748"
                                cy="16.9004"
                                rx="18.9252"
                                ry="16.5"
                                fill="#B3ACB6"
                              />
                            </svg>
                            <span
                              >An acid releases hydroxide (OH–) ions, whereas a
                              base releases hydrogen ions (H+)</span
                            >
                          </div>
                        </div>
                      </div>
                    </v-tab-item>
                  </v-tabs-items>
                </v-row>
                <div class="btn__area col-12">
                  <v-btn color="#383B4C" class="Btn"
                    ><svg
                      width="14"
                      height="13"
                      viewBox="0 0 14 13"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M2.625 0.625C1.64062 0.625 0.875 1.41797 0.875 2.375V11.125C0.875 12.1094 1.64062 12.875 2.625 12.875H11.375C12.332 12.875 13.125 12.1094 13.125 11.125V4.50781C13.125 4.04297 12.9336 3.57812 12.6055 3.25L10.5 1.14453C10.1719 0.816406 9.70703 0.625 9.24219 0.625H2.625ZM2.625 3.25C2.625 2.78516 3.00781 2.375 3.5 2.375H8.75C9.21484 2.375 9.625 2.78516 9.625 3.25V5C9.625 5.49219 9.21484 5.875 8.75 5.875H3.5C3.00781 5.875 2.625 5.49219 2.625 5V3.25ZM7 11.125C6.01562 11.125 5.25 10.3594 5.25 9.375C5.25 8.41797 6.01562 7.625 7 7.625C7.95703 7.625 8.75 8.41797 8.75 9.375C8.75 10.3594 7.95703 11.125 7 11.125Z"
                        fill="white"
                      />
                    </svg>
                    <span>save</span></v-btn
                  >
                  <v-btn disabled color="#F88B2A" class="Btn publish"
                    ><svg
                      width="11"
                      height="15"
                      viewBox="0 0 11 15"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M0.25 2.5C0.25 1.54297 1.01562 0.75 2 0.75H6.375V4.25C6.375 4.74219 6.75781 5.125 7.25 5.125H10.75V13C10.75 13.9844 9.95703 14.75 9 14.75H2C1.01562 14.75 0.25 13.9844 0.25 13V2.5ZM10.75 4.25H7.25V0.75L10.75 4.25Z"
                        fill="white"
                      />
                    </svg>
                    <span>publish</span></v-btn
                  >
                </div>
              </v-tab-item>
            </v-tabs-items>
          </v-row>
        </form>
      </v-row>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      course: false,
      test_type: false,
      test_time: false,
      tab_standard_dropdown: false,
      test_type_tab: 0,
      test_type_tab_weekly: 0,
      test_type_tab_standard: 0,
      standard_number: 10,
      course_list: [
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
      tab_list: [
        { title: "COPY" },
        { title: "WEEKLY TEST" },
        { title: "STANDARD TEST" },
      ],
      time: [
        { title: "10 minutes" },
        { title: "20 minutes" },
        { title: "35 minutes" },
        { title: "45 minutes" },
        { title: "60 minutes" },
      ],
      customToolbar: [
        ["bold", "italic", "underline", "link"],
        ["code-block", { list: "bullet" }, { list: "ordered" }],
        ["image"],
      ],
      description: "",
    };
  },
  methods: {
    tabWeekly(value) {
      switch (value) {
        case "next":
          if (this.test_type_tab_weekly != 4) {
            this.test_type_tab_weekly = this.test_type_tab_weekly + 1;
          } else {
            this.test_type_tab_weekly = 0;
          }
          break;
        case "prev":
          if (this.test_type_tab_weekly == 0) {
            this.test_type_tab_weekly = 4 - this.test_type_tab_weekly;
          } else {
            this.test_type_tab_weekly = this.test_type_tab_weekly - 1;
          }

          break;

        default:
          break;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.row_form {
  .edit_section_header {
    // margin-bottom: 11px;
    padding-top: 0;
    header {
      text-align: left;
      display: flex;
      align-items: center;
      justify-content: space-between;
      & > span {
        font-weight: var(--font-medium);
        font-size: var(--header-font-size);
        color: var(--nav-h3-color);
      }
    }
    &.underSide {
      padding-top: 20px;
    }
  }
  .inputArea {
    padding-top: 0;
    &.listing_action {
      text-align: right;
      .Btn {
        min-height: 4.2rem;
        max-width: 18rem;
        width: 100%;
        border-radius: 10px;
        font-weight: var(--font-medium);
        font-size: var(--normal-font-size);
        border: 1px solid #b3acb6;
        color: var(--border02-color);
        background: transparent;
        box-shadow: none !important;
        svg {
          margin-right: 10px;
        }
        &.upload {
          background: #b3acb6 !important;
          color: #fff;
        }
      }
    }
    &.editor {
      border: 1px solid var(--border03-color);
      filter: drop-shadow(0px 1px 3px rgba(0, 0, 0, 0.07));
      border-radius: 12px;
      padding-bottom: 20px;
    }
    .ebook {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      padding-top: 8px;
      .ebook__input {
        //   width: 100%;
        height: 20.2rem;
        background-color: var(--body-color);
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 12px;
        text-align: center;
        border-radius: 10px;
        cursor: pointer;
        p {
          font-weight: var(--font-light);
          color: var(--nav-h3-color);
          font-size: var(--normal-font-size);
          margin-bottom: 8px;
        }
        span {
          font-weight: var(--font-light);
          color: #b3acb6;
          font-size: var(--normal-font-size);
          line-height: 16px;
          display: inline-block;
        }
      }
    }
    .drag__content {
      height: 13.6rem;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 10px;
      border: 1px dashed var(--nav-h3-color);
      text-align: center;
      // transform: matrix(1, 0, 0, -1, 0, 0);
      p {
        margin-top: 10px;
        margin-bottom: 10px;
        color: #b3acb6;
        font-weight: var(--font-light);
        font-size: var(--normal-font-size);
      }
      span {
        font-weight: var(--font-light);
        font-size: var(--normal-font-size);
        color: var(--nav-h3-color);
        .browse {
          color: var(--primary-color);
          cursor: pointer;
        }
      }
    }
    &.fileInputArea {
      & svg {
        cursor: pointer;
        &:hover {
          rect {
            stroke: var(--primary-color);
          }
          path {
            fill: var(--primary-color);
          }
        }
      }
    }
    .relative {
    }
  }
  .label__area {
    header {
      font-weight: var(--font-light);
      font-size: 1.8rem;
      color: var(--secondary-color);
    }
  }
  .btn__area {
    display: flex;
    align-items: center;
    grid-gap: 29px;
    flex-wrap: wrap;
    .Btn {
      max-width: 23.5rem;
      width: 100%;
      height: 4.4rem;
      text-transform: capitalize;
      color: #fff;
      box-shadow: 0px 4px 20px rgba(56, 59, 76, 0.25);
      border-radius: 10px;
      span {
        font-size: var(--normal-font-size);
        font-weight: var(--font-medium);
      }
      svg {
        margin-right: 10px;
      }
      &[disabled] {
        span {
          color: #fff;
        }
      }
    }
  }
  label {
    font-weight: 500;
    font-size: 1.4rem;
    color: var(--secondary-color);
    margin-bottom: 4px;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    svg {
      cursor: pointer;
    }
  }
  input {
    border: 1px solid var(--nav-h3-color);
    border-radius: 10px;
    height: 4.4rem;
    text-transform: initial;
    color: var(--nav-h3-color);
    font-size: var(--normal-font-size);
    &::placeholder {
      font-size: var(--small-font-size);
      color: #b3acb6;
      font-weight: 400;
    }
    &.active {
      border-color: var(--primary-color);
    }
    &:focus {
      border-color: var(--primary-color);
    }
    &.content {
      border-color: var(--primary-color);
    }
  }
  select {
    color: var(--nav-h3-color);
    font-size: var(--small-font-size);
    font-weight: var(font-medium);
    letter-spacing: -0.011em;
    text-align: left;
    -moz-appearance: none; /* Firefox */
    -webkit-appearance: none; /* Safari and Chrome */
    appearance: none;
    background-image: url("/images/svg/arrow_down.svg") !important;
    background-position: bottom 17px right 15px !important;
    background-repeat: no-repeat !important;
    height: 4.4rem !important;
    border-radius: 10px !important;
    width: 100%;
    padding: 10px;
    outline: none;
    border: 1px solid var(--nav-h3-color);
    cursor: pointer;
    option {
      color: var(--nav-h3-color);
      font-weight: var(--font-medium);
      font-size: var(--normal-font-size);
      &[selected] {
        background: var(--primary-color);
        color: #fff;
      }
      &:hover {
        background: var(--primary-color) !important;
        color: #fff !important;
      }
    }
  }
  textarea {
    height: 100%;
    border: 1px solid var(--nav-h3-color) !important;
    border-radius: 10px;
    resize: none;
    padding: 14px;
    &::placeholder {
      font-size: var(--normal-font-size);
      color: #b3acb6;
      font-weight: 400;
    }
    &:focus {
      border-color: var(--primary-color) !important;
    }
  }
}
.dropdownList {
  margin: 0;
  padding: 0;
  border: 1px solid var(--border03-color);
  box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.07) !important;
  border-radius: 8px;
  .list_item {
    border-radius: 0;
    margin-bottom: 0 !important;
    height: 3rem;
    min-height: 3rem;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    border-top: 1px solid var(--border03-color);
    .list_title {
      font-weight: 400;
      font-size: 1.4rem;
      color: var(--nav-color);
      overflow: visible !important;
      transition: all 0.2s ease-in-out;
      text-transform: capitalize;
    }
    &::before {
      border-radius: 0;
    }
    &:first-child {
      border: none;
      border-top-left-radius: 7px;
      border-top-right-radius: 7px;
    }
    &:last-child {
      border-bottom-left-radius: 7px;
      border-bottom-right-radius: 7px;
    }
    &:hover {
      background: var(--primary-color);
      transition: all 0.2s ease-in-out;
      .list_title {
        color: #fff;
        transition: all 0.2s ease-in-out;
      }
    }
    &.active {
      background: transparent;
      transition: all 0.2s ease-in-out;
      .list_title {
        color: var(--primary-color);
        transition: all 0.2s ease-in-out;
      }
    }
  }
}
.v-menu__content.theme--light {
  &::-webkit-scrollbar {
    width: 0;
    height: 0;
  }
  border-radius: 8px;
}
.theme--light.v-tabs-items {
  background-color: transparent !important;
}
.weekly__tab {
  display: flex;
  width: 100%;
  max-width: 14.2rem;
  height: 4.2rem;
  border: 1px solid #383b4c;
  border-radius: 10px;
  align-items: center;
  overflow: hidden;
  span {
    display: flex;
    height: 100%;
    justify-content: center;
    align-items: center;
    width: 100%;
    // max-width: 33.33%;
    // border-radius: inherit;
    svg {
      path {
        fill: #383b4c;
        transition: all 0.2s ease-in-out;
      }
    }
    &.weekly__tab-nav {
      cursor: pointer;
      transition: all 0.2s ease-in-out;
      &:hover {
        background: var(--primary-color);
        transition: all 0.2s ease-in-out;
        svg {
          path {
            fill: #fff;
            transition: all 0.2s ease-in-out;
          }
        }
      }
      &.left {
      }
    }
    &.weekly__tab-counter {
      color: #383b4c;
      font-size: 1.6rem;
      font-weight: var(--font-light);
    }
  }
  &.standard {
    height: 3.6rem;
    width: 9.1rem;
    justify-content: center;
    grid-gap: 8px;
    cursor: pointer;
    span {
      width: max-content;
    }
  }
}
.control__tab {
  color: #383b4c;
  font-size: 1.6rem;
  font-weight: var(--font-medium);
  cursor: pointer;
}
.weekly__question {
  display: flex;
  flex-direction: column;
  gap: 8px;
  h3.weekly__question-title {
    color: #383b4c;
    font-weight: var(--font-medium);
    font-size: 1.8rem;
  }
  textarea {
    height: 10.3rem;
  }
  .attach_btn {
    border-width: 2px;
    filter: drop-shadow(0px 4px 20px rgba(56, 59, 76, 0.25));
    border-radius: 10px;
    max-width: 19.6rem;
    width: 100%;
    height: 4.4rem;
    margin-top: 7px;
    margin-bottom: 19px;
    span {
      text-transform: capitalize;
      font-size: var(--normal-font-size);
      font-weight: var(--font-medium);
    }
    svg {
      margin-right: 10px;
    }
  }
}
.weekly__question-options {
  display: flex;
  flex-direction: column;
  gap: 8px;
  .relative {
    input {
      width: 100%;
      padding-right: 39px;
      background: transparent !important;
    }
    .absolute {
      right: 10px;
      top: 60%;
      transform: translateY(-50%);
      cursor: pointer;
      svg {
        width: 20px;
        height: 20px;
        path {
          transition: all 0.2s ease-in-out;
        }
      }
      &:hover {
        svg {
          path {
            transition: all 0.2s ease-in-out;
            fill: var(--success-color);
          }
        }
      }
    }
  }
}
.weekly__question-preview {
  padding: 12px 50px 50px 40px;
  & > .col-12 {
    padding: 12px 0;
  }
  .weekly__question-question {
    padding-top: 0;
    & > div {
      background-color: #383b4c;
      min-height: 12.8rem;
      border-radius: 10px;
      display: flex;
      align-items: center;
      text-align: center;
      justify-content: center;
      width: 100%;
      padding: 12px;
      span {
        color: #fff;
        font-weight: var(--font-medium);
        font-size: 2rem;
      }
    }
  }
  .weekly__question-preview-options {
    padding-top: 0;
    & > div {
      display: flex;
      flex-direction: column;
      gap: 15px;
      width: 100%;
      & > div {
        display: flex;
        grid-gap: 17px;
        align-items: center;
        min-height: 6.1rem;
        width: 100%;
        background: var(--body-color);
        border-radius: 10px;
        padding: 14px 17px;
        span {
          font-size: 1.6rem;
          color: var(--secondary-color);
          line-height: 19px;
          font-weight: var(--normal-font-size);
        }
        svg {
          cursor: pointer;
          path {
            transition: all 0.2s ease-in-out;
          }
          &:hover {
            path {
              transition: all 0.2s ease-in-out;
              fill: var(--success-color);
            }
          }
        }
      }
    }
  }
}
</style>