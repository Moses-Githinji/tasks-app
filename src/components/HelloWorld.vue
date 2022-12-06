<template>
  <div
    :class="{ 'dark-theme-bg-image': userTheme === 'dark-theme' }"
    class="app-name-theme-switcher-checkbox-textual-input-container"
  >
    <div class="app-name-theme-switcher-container">
      <div class="app-name-container">
        <h1>to<span>do</span></h1>
      </div>
      <div class="theme-switcher-container">
        <button
          @click="toggleTheme"
          v-if="userTheme === 'light-theme'"
          class="theme-switcher"
        >
          <svg
            width="35"
            height="35"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <g clip-path="url(#clip0_406_4)">
              <path
                d="M18 12C18 13.5913 17.3679 15.1174 16.2426 16.2426C15.1174 17.3679 13.5913 18 12 18C10.4087 18 8.88258 17.3679 7.75736 16.2426C6.63214 15.1174 6 13.5913 6 12C6 10.4087 6.63214 8.88258 7.75736 7.75736C8.88258 6.63214 10.4087 6 12 6C13.5913 6 15.1174 6.63214 16.2426 7.75736C17.3679 8.88258 18 10.4087 18 12V12ZM12 0C12.1989 0 12.3897 0.0790176 12.5303 0.21967C12.671 0.360322 12.75 0.551088 12.75 0.75V3.75C12.75 3.94891 12.671 4.13968 12.5303 4.28033C12.3897 4.42098 12.1989 4.5 12 4.5C11.8011 4.5 11.6103 4.42098 11.4697 4.28033C11.329 4.13968 11.25 3.94891 11.25 3.75V0.75C11.25 0.551088 11.329 0.360322 11.4697 0.21967C11.6103 0.0790176 11.8011 0 12 0V0ZM12 19.5C12.1989 19.5 12.3897 19.579 12.5303 19.7197C12.671 19.8603 12.75 20.0511 12.75 20.25V23.25C12.75 23.4489 12.671 23.6397 12.5303 23.7803C12.3897 23.921 12.1989 24 12 24C11.8011 24 11.6103 23.921 11.4697 23.7803C11.329 23.6397 11.25 23.4489 11.25 23.25V20.25C11.25 20.0511 11.329 19.8603 11.4697 19.7197C11.6103 19.579 11.8011 19.5 12 19.5V19.5ZM24 12C24 12.1989 23.921 12.3897 23.7803 12.5303C23.6397 12.671 23.4489 12.75 23.25 12.75H20.25C20.0511 12.75 19.8603 12.671 19.7197 12.5303C19.579 12.3897 19.5 12.1989 19.5 12C19.5 11.8011 19.579 11.6103 19.7197 11.4697C19.8603 11.329 20.0511 11.25 20.25 11.25H23.25C23.4489 11.25 23.6397 11.329 23.7803 11.4697C23.921 11.6103 24 11.8011 24 12ZM4.5 12C4.5 12.1989 4.42098 12.3897 4.28033 12.5303C4.13968 12.671 3.94891 12.75 3.75 12.75H0.75C0.551088 12.75 0.360322 12.671 0.21967 12.5303C0.0790176 12.3897 0 12.1989 0 12C0 11.8011 0.0790176 11.6103 0.21967 11.4697C0.360322 11.329 0.551088 11.25 0.75 11.25H3.75C3.94891 11.25 4.13968 11.329 4.28033 11.4697C4.42098 11.6103 4.5 11.8011 4.5 12ZM20.4855 3.5145C20.6261 3.65515 20.7051 3.84588 20.7051 4.04475C20.7051 4.24362 20.6261 4.43435 20.4855 4.575L18.3645 6.6975C18.2948 6.76713 18.212 6.82235 18.1209 6.86C18.0299 6.89765 17.9323 6.91699 17.8337 6.91692C17.6347 6.91678 17.4439 6.83758 17.3032 6.69675C17.2336 6.62702 17.1784 6.54425 17.1408 6.45318C17.1031 6.36211 17.0838 6.26452 17.0838 6.16597C17.084 5.96695 17.1632 5.77613 17.304 5.6355L19.425 3.5145C19.5656 3.3739 19.7564 3.29491 19.9553 3.29491C20.1541 3.29491 20.3449 3.3739 20.4855 3.5145V3.5145ZM6.696 17.304C6.8366 17.4446 6.91559 17.6354 6.91559 17.8342C6.91559 18.0331 6.8366 18.2239 6.696 18.3645L4.575 20.4855C4.43355 20.6221 4.2441 20.6977 4.04745 20.696C3.8508 20.6943 3.66269 20.6154 3.52364 20.4764C3.38458 20.3373 3.3057 20.1492 3.30399 19.9526C3.30229 19.7559 3.37788 19.5665 3.5145 19.425L5.6355 17.304C5.77615 17.1634 5.96688 17.0844 6.16575 17.0844C6.36462 17.0844 6.55535 17.1634 6.696 17.304V17.304ZM20.4855 20.4855C20.3449 20.6261 20.1541 20.7051 19.9553 20.7051C19.7564 20.7051 19.5656 20.6261 19.425 20.4855L17.304 18.3645C17.1674 18.223 17.0918 18.0336 17.0935 17.8369C17.0952 17.6403 17.1741 17.4522 17.3131 17.3131C17.4522 17.1741 17.6403 17.0952 17.8369 17.0935C18.0336 17.0918 18.223 17.1674 18.3645 17.304L20.4855 19.425C20.6261 19.5656 20.7051 19.7564 20.7051 19.9553C20.7051 20.1541 20.6261 20.3449 20.4855 20.4855ZM6.696 6.6975C6.55535 6.8381 6.36462 6.91709 6.16575 6.91709C5.96688 6.91709 5.77615 6.8381 5.6355 6.6975L3.5145 4.575C3.44287 4.50581 3.38573 4.42306 3.34642 4.33155C3.30712 4.24005 3.28643 4.14164 3.28556 4.04205C3.2847 3.94247 3.30367 3.84371 3.34138 3.75153C3.37909 3.65936 3.43478 3.57562 3.5052 3.5052C3.57562 3.43478 3.65936 3.37909 3.75153 3.34138C3.84371 3.30367 3.94247 3.2847 4.04205 3.28556C4.14164 3.28643 4.24005 3.30712 4.33155 3.34642C4.42306 3.38573 4.50581 3.44287 4.575 3.5145L6.696 5.6355C6.76585 5.70517 6.82126 5.78793 6.85907 5.87905C6.89688 5.97017 6.91634 6.06785 6.91634 6.1665C6.91634 6.26515 6.89688 6.36283 6.85907 6.45395C6.82126 6.54507 6.76585 6.62783 6.696 6.6975V6.6975Z"
                fill="white"
              />
            </g>
            <defs>
              <clipPath id="clip0_406_4">
                <rect width="24" height="24" fill="white" />
              </clipPath>
            </defs>
          </svg>
        </button>
        <button v-else @click="toggleTheme" class="theme-switcher">
          <svg
            width="35"
            height="35"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M12.97 3C11.7346 3.70288 10.7082 4.72146 9.99582 5.95145C9.28348 7.18143 8.91082 8.57864 8.916 10C8.916 14.418 12.438 18 16.782 18C17.928 18 19.018 17.75 20 17.302C18.39 19.544 15.787 21 12.849 21C7.962 21 4 16.97 4 12C4 7.03 7.962 3 12.849 3H12.969H12.97Z"
              fill="white"
            />
          </svg>
        </button>
      </div>
    </div>
    <div
      :class="{
        'taskValue-toggle-bg-color': userTheme === 'dark-theme',
      }"
      class="checkbox-textual-input-container"
    >
      <div class="round not-checked">
        <input type="checkbox" checked @change="toggleCheck" id="checkbox" />
        <label for="checkbox"></label>
      </div>
      <div class="textual-input-container">
        <input
          type="text"
          name="taskValue"
          id="taskValue"
          v-model="content"
          class="taskValue"
          @keyup.enter="addToDo"
          placeholder="Create a new todo..."
        />
      </div>
    </div>
  </div>
  <div
    :class="{ 'main-section-container-bg-toggle': userTheme === 'dark-theme' }"
    class="main-section-container"
  >
    <div
      :class="{ 'nav-filters-bg-toggle': userTheme === 'dark-theme' }"
      class="tasks-nav-filters-container"
    >
      <div
        v-for="todo in todos"
        :key="todo.id"
        class="array-of-tasks-container"
      >
        <div
          :class="{
            'single-task-container-border-bottom-toggle':
              userTheme === 'dark-theme',
          }"
          class="single-task-container"
        >
          <div class="round not-checked">
            <input
              type="checkbox"
              v-model="checked"
              @change="toggleCheck"
              id="checkbox"
            />
            <label for="checkbox"></label>
          </div>
          <div class="actual-content-container">
            <p
              :class="{
                'actual-content-color-toggle': userTheme === 'dark-theme',
              }"
              class="actual-content"
            >
              {{ todo.content }}
            </p>
          </div>
          <div class="delete-btn-container">
            <button
              :class="{
                'delete-btn-light-mode-color': userTheme === 'light-theme',
              }"
              class="delete-btn"
            >
              <svg
                width="30"
                height="30"
                viewBox="0 0 21 21"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M15.5 5.5L5.5 15.5M15.5 15.5L5.5 5.5L15.5 15.5Z"
                  stroke="hsl(234, 11%, 52%)"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>
      <div
        :class="{ 'nav-filters-bg-toggle': userTheme === 'dark-theme' }"
        class="nav-filters-container"
      >
        <div class="tasks-count-container">
          <p>5 items left</p>
        </div>
        <div class="filter-container">
          <div class="all-tasks-filter-container">
            <button class="all-filter">All</button>
          </div>
          <div class="active-tasks-filter-container">
            <button class="all-filter">Active</button>
          </div>
          <div class="completed-tasks-filter-container">
            <button class="all-filter">Completed</button>
          </div>
        </div>
        <div class="clear-all-completed-btn-container">
          <button class="clear-all-tasks">Clear Completed</button>
        </div>
      </div>
    </div>
    <div
      :class="{
        'mobile-responsive-filters-container-toggle':
          userTheme === 'dark-theme',
      }"
      class="mobile-responsive-filters-container"
    >
      <div class="all-tasks-filter-container">
        <button class="all-filter">All</button>
      </div>
      <div class="active-tasks-filter-container">
        <button class="all-filter">Active</button>
      </div>
      <div class="completed-tasks-filter-container">
        <button class="all-filter">Completed</button>
      </div>
    </div>
    <div>
      <p class="drag-and-drop-prompt">Drag and drop to reorder the list</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroSection",
  mounted() {
    const initUserTheme = this.getTheme() || this.getMediaPreference();
    this.setTheme(initUserTheme);
  },
  methods: {
    setTheme(theme) {
      localStorage.setItem("user-theme", theme);
      this.userTheme = theme;
      document.documentElement.className = theme;
    },
    toggleTheme() {
      const activeTheme = localStorage.getItem("user-theme");
      if (activeTheme === "light-theme") {
        this.setTheme("dark-theme");
      } else {
        this.setTheme("light-theme");
      }
    },
    getMediaPreference() {
      const hasDarkPreference = window.matchMedia(
        "(prefers-color-scheme: dark)"
      ).matches;
      if (hasDarkPreference) {
        return "dark-theme";
      } else {
        return "light-theme";
      }
    },
    getTheme() {
      return localStorage.getItem("user-theme");
    },
    toggleCheck() {
      console.log("clicked");
    },
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          content: "Brush your teeth",
          done: false,
        },
        {
          id: 2,
          content: "Polish your school-shoes",
          done: true,
        },
        {
          id: 3,
          content: "Take your dog for a walk",
          done: false,
        },
        {
          id: 4,
          content: "Brush your teeth",
          done: true,
        },
        {
          id: 5,
          content: "Wash your vehicle",
          done: false,
        },
      ],
      userTheme: "light-theme",
    };
  },
};
</script>

<style scoped>
/* Mobile First Responsive CSS */
@media only screen and (min-width: 320px) {
  @import url("https://fonts.googleapis.com/css2?family=Rubik:wght@400;700&display=swap");

  :root {
    --very-light-gray: hsl(0, 0%, 98%);
    --very-light-grayish-blue: hsl(236, 33%, 92%);
    --light-grayish-blue: hsl(233, 11%, 84%);
    --dark-grayish-blue: hsl(236, 9%, 61%);
    --very-dark-grayish-blue: hsl(235, 19%, 35%);
  }

  :root.dark-theme {
    --very-dark-blue: hsl(235, 21%, 11%);
    --very-light-grayish-blue: hsl(236, 33%, 50%);
    --very-dark-desaturated-blue: hsl(235, 24%, 19%);
    --light-grayish-blue: hsl(234, 39%, 85%);
    --light-grayish-blue-hover: hsl(236, 33%, 92%);
    --dark-grayish-blue: hsl(234, 11%, 52%);
    --very-dark-grayish-blue: hsl(233, 14%, 35%);
  }

  .app-name-theme-switcher-checkbox-textual-input-container {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Rubik", sans-serif;
    font-size: 19px;
    max-width: 100%;
    background-image: url("../assets/bg-desktop-dark.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .main-section-container {
    background-color: hsl(235, 21%, 11%);
    color: hsl(234, 11%, 52%);
    font-family: "Rubik", sans-serif;
    font-size: 13px;
    text-align: center;
    padding: 10px;
    height: 100vh;
    margin-top: -190px;
  }

  .main-section-container-bg-toggle {
    background-color: hsl(233, 11%, 98%);
    color: hsl(234, 11%, 52%);
  }

  .dark-theme-bg-image {
    background-image: url("../assets/bg-desktop-light.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .app-name-theme-switcher-container {
    background-color: inherit;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 90%;
    margin: 0 auto;
  }

  .theme-switcher-container {
    margin-top: 50px;
    margin-right: 5px;
  }

  .app-name-container {
    margin-top: 50px;
  }

  h1 {
    letter-spacing: 4px;
    font-weight: 400;
    color: #fff;
    font-size: 22px;
    text-transform: uppercase;
  }

  span {
    margin: 0 3px;
    font-size: 22px;
  }

  .theme-switcher {
    border: none;
    outline: none;
    background-color: inherit;
    cursor: pointer;
  }

  .checkbox-textual-input-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 10px;
    margin: 30px auto 30px auto;
    height: 65px;
    width: 90%;
    background-color: hsl(235, 24%, 19%);
    align-items: center;
  }

  .round {
    position: relative;
  }

  .round label {
    background-color: inherit;
    border: 1px solid hsl(233, 14%, 35%);
    border-radius: 50%;
    cursor: pointer;
    height: 30px;
    margin-top: -3px;
    margin-left: 15px;
    margin-right: 25px;
    left: 0;
    position: absolute;
    top: 0;
    width: 30px;
  }

  .round label:hover {
    border: 1px solid hsl(234, 11%, 82%);
  }

  .round label::after {
    border: 2px solid hsl(0, 0%, 98%);
    border-top: none;
    border-right: none;
    content: "";
    height: 6px;
    left: 7px;
    opacity: 0;
    position: absolute;
    top: 8px;
    transform: rotate(-45deg);
    width: 12px;
  }

  .round input[type="checkbox"] {
    visibility: hidden;
  }

  .round input[type="checkbox"]:checked + label {
    background-image: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
    border-color: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
  }

  .round input[type="checkbox"]:checked + label::after {
    opacity: 1;
  }

  .textual-input-container {
    height: auto;
    /* padding-left: -20px; */
    width: 80%;
  }

  .taskValue {
    padding: 0.9rem 0 0.9rem 0.6rem;
    border-radius: 10px;
    outline: none;
    border: none;
    font-size: 16px;
    color: hsl(234, 39%, 85%);
    background-color: inherit;
    font-family: "Rubik", sans-serif;
    width: 100%;
  }

  .taskValue-toggle-bg-color {
    color: hsl(232, 8%, 20%);
    background-color: hsl(0, 0%, 98%);
  }

  .tasks-nav-filters-container {
    width: 90%;
    margin: -80px auto 0 auto;
    border-radius: 10px;
    background-color: hsl(235, 24%, 19%);
    box-shadow: 3px 0px 5px -7px hsl(231, 10%, 27%);
  }

  .single-task-container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    border-bottom: 1px solid hsl(235, 19%, 35%);
    padding: 8px;
    align-items: center;
  }

  .single-task-container:last-child {
    border-bottom: none;
    padding-bottom: 0.9rem;
  }

  .single-task-container-border-bottom-toggle {
    border-bottom: 1px solid hsl(0, 0%, 89%);
  }

  .actual-content-container {
    width: 50%;
    font-size: 15px;
    margin-left: 5px;
    cursor: pointer;
    text-align: start;
  }

  .actual-content:hover {
    color: hsl(234, 11%, 82%);
  }

  .actual-content-color-toggle:hover {
    color: hsl(231, 7%, 21%);
  }

  .task-done-content-stying {
    text-decoration: line-through;
    color: hsl(235, 19%, 35%);
  }

  .delete-btn {
    background-color: inherit;
    border: none;
    outline: none;
    margin-right: 5px;
    cursor: pointer;
    opacity: 0;
  }

  .delete-btn:hover {
    opacity: 1;
  }

  .nav-filters-container {
    display: flex;
    padding: 8px;
    justify-content: space-around;
    /* display: none; */
    align-items: center;
  }

  /* Mobile Phones Only */
  .mobile-responsive-filters-container {
    width: 90%;
    display: flex;
    justify-content: space-between;
    padding: 10px;
    border-radius: 5px;
    align-items: center;
    margin: 20px auto 0 auto;
    background-color: hsl(235, 24%, 19%);
    box-shadow: 3px 0px 5px -7px hsl(231, 10%, 27%);
  }

  .mobile-responsive-filters-container-toggle {
    background-color: hsl(0, 0%, 98%);
    color: hsl(234, 11%, 52%);
    box-shadow: 0px 15px 43px 8px hsl(0, 0%, 89%);
  }

  .nav-filters-bg-toggle {
    background-color: hsl(0, 0%, 98%);
    color: hsl(234, 11%, 52%);
    box-shadow: 0px 15px 43px 8px hsl(0, 0%, 89%);
  }

  .filter-container {
    display: flex;
    padding: 15px;
    display: none;
    justify-content: space-between;
    width: 90%;
    align-items: center;
  }

  .all-filter {
    background-color: inherit;
    margin-right: 10px;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .all-filter:hover {
    color: hsl(234, 39%, 85%);
  }

  .all-filter:focus {
    color: hsl(220, 98%, 61%);
  }

  .clear-all-tasks {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .clear-all-tasks:hover {
    color: hsl(234, 39%, 85%);
  }

  .drag-and-drop-prompt {
    text-align: center;
    font-size: 14px;
    font-family: "Rubik", sans-serif;
    color: hsl(233, 14%, 45%);
    margin-top: 130px;
    margin-bottom: 50px;
    padding-bottom: 105px;
  }
}

/* Responsive CSS for IPads */
@media only screen and (min-width: 481px) {
  @import url("https://fonts.googleapis.com/css2?family=Rubik:wght@400;700&display=swap");

  :root {
    --very-light-gray: hsl(0, 0%, 98%);
    --very-light-grayish-blue: hsl(236, 33%, 92%);
    --light-grayish-blue: hsl(233, 11%, 84%);
    --dark-grayish-blue: hsl(236, 9%, 61%);
    --very-dark-grayish-blue: hsl(235, 19%, 35%);
  }

  :root.dark-theme {
    --very-dark-blue: hsl(235, 21%, 11%);
    --very-light-grayish-blue: hsl(236, 33%, 50%);
    --very-dark-desaturated-blue: hsl(235, 24%, 19%);
    --light-grayish-blue: hsl(234, 39%, 85%);
    --light-grayish-blue-hover: hsl(236, 33%, 92%);
    --dark-grayish-blue: hsl(234, 11%, 52%);
    --very-dark-grayish-blue: hsl(233, 14%, 35%);
  }

  .app-name-theme-switcher-checkbox-textual-input-container {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Rubik", sans-serif;
    font-size: 19px;
    max-width: 100%;
    background-image: url("../assets/bg-desktop-dark.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .main-section-container {
    background-color: hsl(235, 21%, 11%);
    color: hsl(234, 11%, 52%);
    font-family: "Rubik", sans-serif;
    font-size: 13px;
    text-align: center;
    padding: 10px;
    height: 100vh;
    margin-top: -270px;
  }

  .main-section-container-bg-toggle {
    background-color: hsl(233, 11%, 98%);
    color: hsl(234, 11%, 52%);
  }

  .dark-theme-bg-image {
    background-image: url("../assets/bg-desktop-light.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .app-name-theme-switcher-container {
    background-color: inherit;
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 50%;
    margin: 0 auto;
  }

  .theme-switcher-container {
    margin-top: 20px;
    margin-right: 5px;
  }

  .app-name-container {
    margin-top: 20px;
  }

  h1 {
    letter-spacing: 10px;
    font-weight: 400;
    color: #fff;
    font-size: 39px;
    text-transform: uppercase;
  }

  span {
    margin: 0 3px;
    font-size: 39px;
  }

  .theme-switcher {
    border: none;
    outline: none;
    background-color: inherit;
    cursor: pointer;
  }

  .checkbox-textual-input-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 10px;
    margin: 30px auto 30px auto;
    height: 65px;
    max-width: 50%;
    background-color: hsl(235, 24%, 19%);
    align-items: center;
  }

  .round {
    position: relative;
  }

  .round label {
    background-color: inherit;
    border: 1px solid hsl(233, 14%, 35%);
    border-radius: 50%;
    cursor: pointer;
    height: 30px;
    margin-top: -3px;
    margin-left: 15px;
    left: 0;
    position: absolute;
    top: 0;
    width: 30px;
  }

  .round label:hover {
    border: 1px solid hsl(234, 11%, 82%);
  }

  .round > label:hover {
    border: 3px solid
      linear-gradient(
        125deg,
        hsl(240deg 73% 84%) 0%,
        hsl(243deg 73% 82%) 5%,
        hsl(246deg 76% 81%) 10%,
        hsl(249deg 78% 79%) 15%,
        hsl(251deg 78% 77%) 20%,
        hsl(255deg 79% 75%) 25%,
        hsl(258deg 81% 74%) 30%,
        hsl(260deg 82% 72%) 35%,
        hsl(263deg 84% 71%) 40%,
        hsl(266deg 85% 69%) 45%,
        hsl(269deg 87% 67%) 50%,
        hsl(272deg 88% 65%) 55%,
        hsl(275deg 89% 64%) 60%,
        hsl(278deg 91% 62%) 65%,
        hsl(280deg 92% 60%) 70%,
        hsl(283deg 93% 59%) 75%,
        hsl(286deg 95% 57%) 80%,
        hsl(289deg 96% 55%) 85%,
        hsl(292deg 97% 54%) 90%,
        hsl(295deg 98% 52%) 95%,
        hsl(298deg 100% 50%) 100%
      );
  }

  .round label::after {
    border: 2px solid hsl(0, 0%, 98%);
    border-top: none;
    border-right: none;
    content: "";
    height: 6px;
    left: 7px;
    opacity: 0;
    position: absolute;
    top: 8px;
    transform: rotate(-45deg);
    width: 12px;
  }

  .round input[type="checkbox"] {
    visibility: hidden;
  }

  .round input[type="checkbox"]:checked + label {
    background-image: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
    border-color: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
  }

  .round input[type="checkbox"]:checked + label::after {
    opacity: 1;
  }

  .textual-input-container {
    height: auto;
    width: 90%;
  }

  .taskValue {
    padding: 0.9rem 0 0.9rem 0.9rem;
    border-radius: 10px;
    outline: none;
    border: none;
    font-size: 21px;
    color: hsl(234, 39%, 85%);
    background-color: inherit;
    font-family: "Rubik", sans-serif;
    width: 100%;
  }

  .taskValue-toggle-bg-color {
    color: hsl(232, 8%, 20%);
    background-color: hsl(0, 0%, 98%);
  }

  .tasks-nav-filters-container {
    max-width: 50%;
    margin: -40px auto 0 auto;
    border-radius: 10px;
    background-color: hsl(235, 24%, 19%);
    box-shadow: 3px 0px 5px -7px hsl(231, 10%, 27%);
  }

  .mobile-responsive-filters-container {
    display: none;
  }

  .single-task-container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    border-bottom: 1px solid hsl(235, 19%, 35%);
    padding: 8px;
    align-items: center;
  }

  .single-task-container-border-bottom-toggle {
    border-bottom: 1px solid hsl(0, 0%, 89%);
  }

  .actual-content-container {
    width: 40%;
    font-size: 15px;
    margin-left: -60px;
    cursor: pointer;
    text-align: start;
  }

  .task-done-content-stying {
    text-decoration: line-through;
    color: hsl(235, 19%, 35%);
  }

  .delete-btn {
    background-color: inherit;
    border: none;
    outline: none;
    margin-right: 5px;
  }

  .nav-filters-container {
    display: flex;
    padding: 8px;
    justify-content: space-around;
    align-items: center;
  }

  .nav-filters-bg-toggle {
    background-color: hsl(0, 0%, 98%);
    color: hsl(234, 11%, 52%);
    box-shadow: 0px 15px 43px 8px hsl(0, 0%, 89%);
  }

  .filter-container {
    display: flex;
    padding: 10px;
    justify-content: space-between;
    width: 40%;
    align-items: center;
  }

  .all-filter {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
  }
  .all-filter:focus {
    color: hsl(220, 98%, 61%);
  }

  .clear-all-tasks {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
  }

  .drag-and-drop-prompt {
    text-align: center;
    font-size: 14px;
    font-family: "Rubik", sans-serif;
    color: hsl(233, 14%, 45%);
    margin-top: 60px;
    margin-bottom: 50px;
    padding-bottom: 105px;
  }
}

/* Responsive CSS for Laptops */
@media only screen and (min-width: 769px) {
  @import url("https://fonts.googleapis.com/css2?family=Rubik:wght@400;700&display=swap");

  :root {
    --very-light-gray: hsl(0, 0%, 98%);
    --very-light-grayish-blue: hsl(236, 33%, 92%);
    --light-grayish-blue: hsl(233, 11%, 84%);
    --dark-grayish-blue: hsl(236, 9%, 61%);
    --very-dark-grayish-blue: hsl(235, 19%, 35%);
  }

  :root.dark-theme {
    --very-dark-blue: hsl(235, 21%, 11%);
    --very-light-grayish-blue: hsl(236, 33%, 50%);
    --very-dark-desaturated-blue: hsl(235, 24%, 19%);
    --light-grayish-blue: hsl(234, 39%, 85%);
    --light-grayish-blue-hover: hsl(236, 33%, 92%);
    --dark-grayish-blue: hsl(234, 11%, 52%);
    --very-dark-grayish-blue: hsl(233, 14%, 35%);
  }

  .app-name-theme-switcher-checkbox-textual-input-container {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Rubik", sans-serif;
    font-size: 19px;
    max-width: 100%;
    background-image: url("../assets/bg-desktop-dark.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .main-section-container {
    background-color: hsl(235, 21%, 11%);
    color: hsl(234, 11%, 52%);
    font-family: "Rubik", sans-serif;
    font-size: 13px;
    text-align: center;
    padding: 10px;
    height: 100vh;
    margin-top: -340px;
  }

  .main-section-container-bg-toggle {
    background-color: hsl(233, 11%, 98%);
    color: hsl(234, 11%, 52%);
  }

  .dark-theme-bg-image {
    background-image: url("../assets/bg-desktop-light.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .app-name-theme-switcher-container {
    background-color: inherit;
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 50%;
    margin: 0 auto;
  }

  .theme-switcher-container {
    margin-top: 50px;
    margin-right: 5px;
  }

  .app-name-container {
    margin-top: 50px;
  }

  h1 {
    letter-spacing: 10px;
    font-weight: 400;
    color: #fff;
    font-size: 39px;
    text-transform: uppercase;
  }

  span {
    margin: 0 3px;
    font-size: 39px;
  }

  .theme-switcher {
    border: none;
    outline: none;
    background-color: inherit;
    cursor: pointer;
  }

  .checkbox-textual-input-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 10px;
    margin: 30px auto 30px auto;
    height: 65px;
    max-width: 50%;
    background-color: hsl(235, 24%, 19%);
    align-items: center;
  }

  .round {
    position: relative;
  }

  .round label {
    background-color: inherit;
    border: 1px solid hsl(233, 14%, 35%);
    border-radius: 50%;
    cursor: pointer;
    height: 30px;
    margin-top: -3px;
    margin-left: 15px;
    left: 0;
    position: absolute;
    top: 0;
    width: 30px;
  }

  .round label:hover {
    border: 1px solid hsl(234, 11%, 82%);
  }

  .round > label:hover {
    border: 3px solid
      linear-gradient(
        125deg,
        hsl(240deg 73% 84%) 0%,
        hsl(243deg 73% 82%) 5%,
        hsl(246deg 76% 81%) 10%,
        hsl(249deg 78% 79%) 15%,
        hsl(251deg 78% 77%) 20%,
        hsl(255deg 79% 75%) 25%,
        hsl(258deg 81% 74%) 30%,
        hsl(260deg 82% 72%) 35%,
        hsl(263deg 84% 71%) 40%,
        hsl(266deg 85% 69%) 45%,
        hsl(269deg 87% 67%) 50%,
        hsl(272deg 88% 65%) 55%,
        hsl(275deg 89% 64%) 60%,
        hsl(278deg 91% 62%) 65%,
        hsl(280deg 92% 60%) 70%,
        hsl(283deg 93% 59%) 75%,
        hsl(286deg 95% 57%) 80%,
        hsl(289deg 96% 55%) 85%,
        hsl(292deg 97% 54%) 90%,
        hsl(295deg 98% 52%) 95%,
        hsl(298deg 100% 50%) 100%
      );
  }

  .round label::after {
    border: 2px solid hsl(0, 0%, 98%);
    border-top: none;
    border-right: none;
    content: "";
    height: 6px;
    left: 7px;
    opacity: 0;
    position: absolute;
    top: 8px;
    transform: rotate(-45deg);
    width: 12px;
  }

  .round input[type="checkbox"] {
    visibility: hidden;
  }

  .round input[type="checkbox"]:checked + label {
    background-image: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
    border-color: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
  }

  .round input[type="checkbox"]:checked + label::after {
    opacity: 1;
  }

  .textual-input-container {
    height: auto;
    width: 90%;
  }

  .taskValue {
    padding: 0.9rem 0 0.9rem 0.9rem;
    border-radius: 10px;
    outline: none;
    border: none;
    font-size: 21px;
    color: hsl(234, 39%, 85%);
    background-color: inherit;
    font-family: "Rubik", sans-serif;
    width: 100%;
  }

  .taskValue-toggle-bg-color {
    color: hsl(232, 8%, 20%);
    background-color: hsl(0, 0%, 98%);
  }

  .tasks-nav-filters-container {
    max-width: 50%;
    margin: -80px auto 0 auto;
    border-radius: 10px;
    background-color: hsl(235, 24%, 19%);
    box-shadow: 3px 0px 5px -7px hsl(231, 10%, 27%);
  }

  .mobile-responsive-filters-container {
    display: none;
  }

  .single-task-container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    border-bottom: 1px solid hsl(235, 19%, 35%);
    padding: 8px;
    align-items: center;
  }

  .single-task-container-border-bottom-toggle {
    border-bottom: 1px solid hsl(0, 0%, 89%);
  }

  .actual-content-container {
    width: 60%;
    font-size: 15px;
    margin-left: -60px;
    cursor: pointer;
    text-align: start;
  }

  /* .actual-content:hover {
    color: hsl(234, 11%, 82%);
  }

  .actual-content-color-toggle:hover {
    color: hsl(231, 7%, 21%);
  } */

  .task-done-content-stying {
    text-decoration: line-through;
    color: hsl(235, 19%, 35%);
  }

  .delete-btn {
    background-color: inherit;
    border: none;
    outline: none;
    margin-right: 5px;
    cursor: pointer;
    opacity: 0;
  }

  /* .delete-btn:hover {
    opacity: 1;
  } */

  .nav-filters-container {
    display: flex;
    padding: 8px;
    justify-content: space-around;
    align-items: center;
  }

  .nav-filters-bg-toggle {
    background-color: hsl(0, 0%, 98%);
    color: hsl(234, 11%, 52%);
    box-shadow: 0px 15px 43px 8px hsl(0, 0%, 89%);
  }

  .filter-container {
    display: flex;
    padding: 10px;
    justify-content: space-between;
    width: 40%;
    align-items: center;
  }

  .all-filter {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .all-filter:hover {
    color: hsl(234, 39%, 85%);
  }

  .all-filter:focus {
    color: hsl(220, 98%, 61%);
  }

  .clear-all-tasks {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .clear-all-tasks:hover {
    color: hsl(234, 39%, 85%);
  }

  .drag-and-drop-prompt {
    text-align: center;
    font-size: 14px;
    font-family: "Rubik", sans-serif;
    color: hsl(233, 14%, 45%);
    margin-top: 60px;
    margin-bottom: 50px;
    padding-bottom: 105px;
  }
}

/* Desktop CSS */
@media only screen and (min-width: 1025px) {
  @import url("https://fonts.googleapis.com/css2?family=Rubik:wght@400;700&display=swap");

  :root {
    --very-light-gray: hsl(0, 0%, 98%);
    --very-light-grayish-blue: hsl(236, 33%, 92%);
    --light-grayish-blue: hsl(233, 11%, 84%);
    --dark-grayish-blue: hsl(236, 9%, 61%);
    --very-dark-grayish-blue: hsl(235, 19%, 35%);
  }

  :root.dark-theme {
    --very-dark-blue: hsl(235, 21%, 11%);
    --very-light-grayish-blue: hsl(236, 33%, 50%);
    --very-dark-desaturated-blue: hsl(235, 24%, 19%);
    --light-grayish-blue: hsl(234, 39%, 85%);
    --light-grayish-blue-hover: hsl(236, 33%, 92%);
    --dark-grayish-blue: hsl(234, 11%, 52%);
    --very-dark-grayish-blue: hsl(233, 14%, 35%);
  }

  .app-name-theme-switcher-checkbox-textual-input-container {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Rubik", sans-serif;
    font-size: 19px;
    max-width: 100%;
    background-image: url("../assets/bg-desktop-dark.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .main-section-container {
    background-color: hsl(235, 21%, 11%);
    color: hsl(234, 11%, 52%);
    font-family: "Rubik", sans-serif;
    font-size: 13px;
    text-align: center;
    padding: 10px;
    height: 100vh;
    margin-top: -220px;
  }

  .main-section-container-bg-toggle {
    background-color: hsl(233, 11%, 98%);
    color: hsl(234, 11%, 52%);
  }

  .dark-theme-bg-image {
    background-image: url("../assets/bg-desktop-light.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .app-name-theme-switcher-container {
    background-color: inherit;
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 50%;
    margin: 0 auto;
  }

  .theme-switcher-container {
    margin-top: 50px;
    margin-right: 5px;
  }

  .app-name-container {
    margin-top: 50px;
  }

  h1 {
    letter-spacing: 10px;
    font-weight: 400;
    color: #fff;
    font-size: 39px;
    text-transform: uppercase;
  }

  span {
    margin: 0 3px;
    font-size: 39px;
  }

  .theme-switcher {
    border: none;
    outline: none;
    background-color: inherit;
    cursor: pointer;
  }

  .checkbox-textual-input-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 10px;
    margin: 30px auto 30px auto;
    height: 65px;
    max-width: 50%;
    background-color: hsl(235, 24%, 19%);
    align-items: center;
  }

  .round {
    position: relative;
  }

  .round label {
    background-color: inherit;
    border: 1px solid hsl(233, 14%, 35%);
    border-radius: 50%;
    cursor: pointer;
    height: 30px;
    margin-top: -3px;
    margin-left: 15px;
    left: 0;
    position: absolute;
    top: 0;
    width: 30px;
  }

  .round label:hover {
    border: 1px solid hsl(234, 11%, 82%);
  }

  .round > label:hover {
    border: 3px solid
      linear-gradient(
        125deg,
        hsl(240deg 73% 84%) 0%,
        hsl(243deg 73% 82%) 5%,
        hsl(246deg 76% 81%) 10%,
        hsl(249deg 78% 79%) 15%,
        hsl(251deg 78% 77%) 20%,
        hsl(255deg 79% 75%) 25%,
        hsl(258deg 81% 74%) 30%,
        hsl(260deg 82% 72%) 35%,
        hsl(263deg 84% 71%) 40%,
        hsl(266deg 85% 69%) 45%,
        hsl(269deg 87% 67%) 50%,
        hsl(272deg 88% 65%) 55%,
        hsl(275deg 89% 64%) 60%,
        hsl(278deg 91% 62%) 65%,
        hsl(280deg 92% 60%) 70%,
        hsl(283deg 93% 59%) 75%,
        hsl(286deg 95% 57%) 80%,
        hsl(289deg 96% 55%) 85%,
        hsl(292deg 97% 54%) 90%,
        hsl(295deg 98% 52%) 95%,
        hsl(298deg 100% 50%) 100%
      );
  }

  .round label::after {
    border: 2px solid hsl(0, 0%, 98%);
    border-top: none;
    border-right: none;
    content: "";
    height: 6px;
    left: 7px;
    opacity: 0;
    position: absolute;
    top: 8px;
    transform: rotate(-45deg);
    width: 12px;
  }

  .round input[type="checkbox"] {
    visibility: hidden;
  }

  .round input[type="checkbox"]:checked + label {
    background-image: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
    border-color: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
  }

  .round input[type="checkbox"]:checked + label::after {
    opacity: 1;
  }

  .textual-input-container {
    height: auto;
    width: 90%;
  }

  .taskValue {
    padding: 0.9rem 0 0.9rem 0.9rem;
    border-radius: 10px;
    outline: none;
    border: none;
    font-size: 21px;
    color: hsl(234, 39%, 85%);
    background-color: inherit;
    font-family: "Rubik", sans-serif;
    width: 100%;
  }

  .taskValue-toggle-bg-color {
    color: hsl(232, 8%, 20%);
    background-color: hsl(0, 0%, 98%);
  }

  .tasks-nav-filters-container {
    max-width: 50%;
    margin: -80px auto 0 auto;
    border-radius: 10px;
    background-color: hsl(235, 24%, 19%);
    box-shadow: 3px 0px 5px -7px hsl(231, 10%, 27%);
  }

  .mobile-responsive-filters-container {
    display: none;
  }

  .single-task-container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    border-bottom: 1px solid hsl(235, 19%, 35%);
    padding: 8px;
    align-items: center;
  }

  .single-task-container-border-bottom-toggle {
    border-bottom: 1px solid hsl(0, 0%, 89%);
  }

  .actual-content-container {
    width: 60%;
    font-size: 15px;
    margin-left: -60px;
    cursor: pointer;
    text-align: start;
  }

  .actual-content:hover {
    color: hsl(234, 11%, 82%);
  }

  .actual-content-color-toggle:hover {
    color: hsl(231, 7%, 21%);
  }

  .task-done-content-stying {
    text-decoration: line-through;
    color: hsl(235, 19%, 35%);
  }

  .delete-btn {
    background-color: inherit;
    border: none;
    outline: none;
    margin-right: 5px;
    cursor: pointer;
    opacity: 0;
  }

  .delete-btn:hover {
    opacity: 1;
  }

  .nav-filters-container {
    display: flex;
    padding: 8px;
    justify-content: space-around;
    align-items: center;
  }

  .nav-filters-bg-toggle {
    background-color: hsl(0, 0%, 98%);
    color: hsl(234, 11%, 52%);
    box-shadow: 0px 15px 43px 8px hsl(0, 0%, 89%);
  }

  .filter-container {
    display: flex;
    padding: 10px;
    justify-content: space-between;
    width: 40%;
    align-items: center;
  }

  .all-filter {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .all-filter:hover {
    color: hsl(234, 39%, 85%);
  }

  .all-filter:focus {
    color: hsl(220, 98%, 61%);
  }

  .clear-all-tasks {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .clear-all-tasks:hover {
    color: hsl(234, 39%, 85%);
  }

  .drag-and-drop-prompt {
    text-align: center;
    font-size: 14px;
    font-family: "Rubik", sans-serif;
    color: hsl(233, 14%, 45%);
    margin-top: 60px;
    margin-bottom: 50px;
    padding-bottom: 105px;
  }
}

@media only screen and (min-width: 1201px) {
  @import url("https://fonts.googleapis.com/css2?family=Rubik:wght@400;700&display=swap");

  :root {
    --very-light-gray: hsl(0, 0%, 98%);
    --very-light-grayish-blue: hsl(236, 33%, 92%);
    --light-grayish-blue: hsl(233, 11%, 84%);
    --dark-grayish-blue: hsl(236, 9%, 61%);
    --very-dark-grayish-blue: hsl(235, 19%, 35%);
  }

  :root.dark-theme {
    --very-dark-blue: hsl(235, 21%, 11%);
    --very-light-grayish-blue: hsl(236, 33%, 50%);
    --very-dark-desaturated-blue: hsl(235, 24%, 19%);
    --light-grayish-blue: hsl(234, 39%, 85%);
    --light-grayish-blue-hover: hsl(236, 33%, 92%);
    --dark-grayish-blue: hsl(234, 11%, 52%);
    --very-dark-grayish-blue: hsl(233, 14%, 35%);
  }

  .app-name-theme-switcher-checkbox-textual-input-container {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Rubik", sans-serif;
    font-size: 19px;
    max-width: 100%;
    background-image: url("../assets/bg-desktop-dark.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .main-section-container {
    background-color: hsl(235, 21%, 11%);
    color: hsl(234, 11%, 52%);
    font-family: "Rubik", sans-serif;
    font-size: 13px;
    text-align: center;
    padding: 10px;
    height: 100vh;
    margin-top: -270px;
  }

  .main-section-container-bg-toggle {
    background-color: hsl(233, 11%, 98%);
    color: hsl(234, 11%, 52%);
  }

  .dark-theme-bg-image {
    background-image: url("../assets/bg-desktop-light.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .app-name-theme-switcher-container {
    background-color: inherit;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 50%;
    margin: 0 auto;
  }

  .theme-switcher-container {
    margin-top: 50px;
    margin-right: 5px;
  }

  .app-name-container {
    margin-top: 50px;
  }

  h1 {
    letter-spacing: 10px;
    font-weight: 400;
    color: #fff;
    font-size: 39px;
    text-transform: uppercase;
  }

  span {
    margin: 0 3px;
    font-size: 39px;
  }

  .theme-switcher {
    border: none;
    outline: none;
    background-color: inherit;
    cursor: pointer;
  }

  .checkbox-textual-input-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 10px;
    margin: 30px auto 30px auto;
    height: 65px;
    width: 50%;
    background-color: hsl(235, 24%, 19%);
    align-items: center;
  }

  .round {
    position: relative;
  }

  .round label {
    background-color: inherit;
    border: 1px solid hsl(233, 14%, 35%);
    border-radius: 50%;
    cursor: pointer;
    height: 30px;
    margin-top: -3px;
    margin-left: 15px;
    left: 0;
    position: absolute;
    top: 0;
    width: 30px;
  }

  .round label:hover {
    border: 1px solid hsl(234, 11%, 82%);
  }

  .round > label:hover {
    border: 3px solid
      linear-gradient(
        125deg,
        hsl(240deg 73% 84%) 0%,
        hsl(243deg 73% 82%) 5%,
        hsl(246deg 76% 81%) 10%,
        hsl(249deg 78% 79%) 15%,
        hsl(251deg 78% 77%) 20%,
        hsl(255deg 79% 75%) 25%,
        hsl(258deg 81% 74%) 30%,
        hsl(260deg 82% 72%) 35%,
        hsl(263deg 84% 71%) 40%,
        hsl(266deg 85% 69%) 45%,
        hsl(269deg 87% 67%) 50%,
        hsl(272deg 88% 65%) 55%,
        hsl(275deg 89% 64%) 60%,
        hsl(278deg 91% 62%) 65%,
        hsl(280deg 92% 60%) 70%,
        hsl(283deg 93% 59%) 75%,
        hsl(286deg 95% 57%) 80%,
        hsl(289deg 96% 55%) 85%,
        hsl(292deg 97% 54%) 90%,
        hsl(295deg 98% 52%) 95%,
        hsl(298deg 100% 50%) 100%
      );
  }

  .round label::after {
    border: 2px solid hsl(0, 0%, 98%);
    border-top: none;
    border-right: none;
    content: "";
    height: 6px;
    left: 7px;
    opacity: 0;
    position: absolute;
    top: 8px;
    transform: rotate(-45deg);
    width: 12px;
  }

  .round input[type="checkbox"] {
    visibility: hidden;
  }

  .round input[type="checkbox"]:checked + label {
    background-image: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
    border-color: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
  }

  .round input[type="checkbox"]:checked + label::after {
    opacity: 1;
  }

  .textual-input-container {
    height: auto;
    width: 90%;
  }

  .taskValue {
    padding: 0.9rem 0 0.9rem 0.9rem;
    border-radius: 10px;
    outline: none;
    border: none;
    font-size: 21px;
    color: hsl(234, 39%, 85%);
    background-color: inherit;
    font-family: "Rubik", sans-serif;
    width: 100%;
  }

  .taskValue-toggle-bg-color {
    color: hsl(232, 8%, 20%);
    background-color: hsl(0, 0%, 98%);
  }

  .tasks-nav-filters-container {
    width: 50%;
    margin: -80px auto 0 auto;
    border-radius: 10px;
    background-color: hsl(235, 24%, 19%);
    box-shadow: 3px 0px 5px -7px hsl(231, 10%, 27%);
  }

  .mobile-responsive-filters-container {
    display: none;
  }

  .single-task-container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    border-bottom: 1px solid hsl(235, 19%, 35%);
    padding: 8px;
    align-items: center;
  }

  .single-task-container-border-bottom-toggle {
    border-bottom: 1px solid hsl(0, 0%, 89%);
  }

  .actual-content-container {
    width: 60%;
    font-size: 15px;
    margin-left: -60px;
    cursor: pointer;
    text-align: start;
  }

  .actual-content:hover {
    color: hsl(234, 11%, 82%);
  }

  .actual-content-color-toggle:hover {
    color: hsl(231, 7%, 21%);
  }

  .task-done-content-stying {
    text-decoration: line-through;
    color: hsl(235, 19%, 35%);
  }

  .delete-btn {
    background-color: inherit;
    border: none;
    outline: none;
    margin-right: 5px;
    cursor: pointer;
    opacity: 0;
  }

  .delete-btn:hover {
    opacity: 1;
  }

  .nav-filters-container {
    display: flex;
    padding: 8px;
    justify-content: space-around;
    align-items: center;
  }

  .nav-filters-bg-toggle {
    background-color: hsl(0, 0%, 98%);
    color: hsl(234, 11%, 52%);
    box-shadow: 0px 15px 43px 8px hsl(0, 0%, 89%);
  }

  .filter-container {
    display: flex;
    padding: 10px;
    justify-content: space-between;
    width: 40%;
    align-items: center;
  }

  .all-filter {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .all-filter:hover {
    color: hsl(234, 39%, 85%);
  }

  .all-filter:focus {
    color: hsl(220, 98%, 61%);
  }

  .clear-all-tasks {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .clear-all-tasks:hover {
    color: hsl(234, 39%, 85%);
  }

  .drag-and-drop-prompt {
    text-align: center;
    font-size: 14px;
    font-family: "Rubik", sans-serif;
    color: hsl(233, 14%, 45%);
    margin-top: 60px;
    margin-bottom: 50px;
    padding-bottom: 105px;
  }
}

@media only screen and (min-width: 1440px) {
  @import url("https://fonts.googleapis.com/css2?family=Rubik:wght@400;700&display=swap");

  :root {
    --very-light-gray: hsl(0, 0%, 98%);
    --very-light-grayish-blue: hsl(236, 33%, 92%);
    --light-grayish-blue: hsl(233, 11%, 84%);
    --dark-grayish-blue: hsl(236, 9%, 61%);
    --very-dark-grayish-blue: hsl(235, 19%, 35%);
  }

  :root.dark-theme {
    --very-dark-blue: hsl(235, 21%, 11%);
    --very-light-grayish-blue: hsl(236, 33%, 50%);
    --very-dark-desaturated-blue: hsl(235, 24%, 19%);
    --light-grayish-blue: hsl(234, 39%, 85%);
    --light-grayish-blue-hover: hsl(236, 33%, 92%);
    --dark-grayish-blue: hsl(234, 11%, 52%);
    --very-dark-grayish-blue: hsl(233, 14%, 35%);
  }

  .app-name-theme-switcher-checkbox-textual-input-container {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Rubik", sans-serif;
    font-size: 19px;
    max-width: 100%;
    background-image: url("../assets/bg-desktop-dark.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .main-section-container {
    background-color: hsl(235, 21%, 11%);
    color: hsl(234, 11%, 52%);
    font-family: "Rubik", sans-serif;
    font-size: 13px;
    text-align: center;
    padding: 10px;
    height: 100vh;
    margin-top: -580px;
  }

  .main-section-container-bg-toggle {
    background-color: hsl(233, 11%, 98%);
    color: hsl(234, 11%, 52%);
  }

  .dark-theme-bg-image {
    background-image: url("../assets/bg-desktop-light.jpg");
    background-position: cover;
    background-repeat: no-repeat;
    height: 90vh;
  }

  .app-name-theme-switcher-container {
    background-color: inherit;
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 50%;
    margin: 0 auto;
  }

  .theme-switcher-container {
    margin-top: 50px;
    margin-right: 5px;
  }

  .app-name-container {
    margin-top: 50px;
  }

  h1 {
    letter-spacing: 10px;
    font-weight: 400;
    color: #fff;
    font-size: 39px;
    text-transform: uppercase;
  }

  span {
    margin: 0 3px;
    font-size: 39px;
  }

  .theme-switcher {
    border: none;
    outline: none;
    background-color: inherit;
    cursor: pointer;
  }

  .checkbox-textual-input-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 10px;
    margin: 30px auto 30px auto;
    height: 65px;
    max-width: 50%;
    background-color: hsl(235, 24%, 19%);
    align-items: center;
  }

  .round {
    position: relative;
  }

  .round label {
    background-color: inherit;
    border: 1px solid hsl(233, 14%, 35%);
    border-radius: 50%;
    cursor: pointer;
    height: 30px;
    margin-top: -3px;
    margin-left: 15px;
    left: 0;
    position: absolute;
    top: 0;
    width: 30px;
  }

  .round label:hover {
    border: 1px solid hsl(234, 11%, 82%);
  }

  .round > label:hover {
    border: 3px solid
      linear-gradient(
        125deg,
        hsl(240deg 73% 84%) 0%,
        hsl(243deg 73% 82%) 5%,
        hsl(246deg 76% 81%) 10%,
        hsl(249deg 78% 79%) 15%,
        hsl(251deg 78% 77%) 20%,
        hsl(255deg 79% 75%) 25%,
        hsl(258deg 81% 74%) 30%,
        hsl(260deg 82% 72%) 35%,
        hsl(263deg 84% 71%) 40%,
        hsl(266deg 85% 69%) 45%,
        hsl(269deg 87% 67%) 50%,
        hsl(272deg 88% 65%) 55%,
        hsl(275deg 89% 64%) 60%,
        hsl(278deg 91% 62%) 65%,
        hsl(280deg 92% 60%) 70%,
        hsl(283deg 93% 59%) 75%,
        hsl(286deg 95% 57%) 80%,
        hsl(289deg 96% 55%) 85%,
        hsl(292deg 97% 54%) 90%,
        hsl(295deg 98% 52%) 95%,
        hsl(298deg 100% 50%) 100%
      );
  }

  .round label::after {
    border: 2px solid hsl(0, 0%, 98%);
    border-top: none;
    border-right: none;
    content: "";
    height: 6px;
    left: 7px;
    opacity: 0;
    position: absolute;
    top: 8px;
    transform: rotate(-45deg);
    width: 12px;
  }

  .round input[type="checkbox"] {
    visibility: hidden;
  }

  .round input[type="checkbox"]:checked + label {
    background-image: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
    border-color: linear-gradient(
      125deg,
      hsl(240deg 73% 84%) 0%,
      hsl(243deg 73% 82%) 5%,
      hsl(246deg 76% 81%) 10%,
      hsl(249deg 78% 79%) 15%,
      hsl(251deg 78% 77%) 20%,
      hsl(255deg 79% 75%) 25%,
      hsl(258deg 81% 74%) 30%,
      hsl(260deg 82% 72%) 35%,
      hsl(263deg 84% 71%) 40%,
      hsl(266deg 85% 69%) 45%,
      hsl(269deg 87% 67%) 50%,
      hsl(272deg 88% 65%) 55%,
      hsl(275deg 89% 64%) 60%,
      hsl(278deg 91% 62%) 65%,
      hsl(280deg 92% 60%) 70%,
      hsl(283deg 93% 59%) 75%,
      hsl(286deg 95% 57%) 80%,
      hsl(289deg 96% 55%) 85%,
      hsl(292deg 97% 54%) 90%,
      hsl(295deg 98% 52%) 95%,
      hsl(298deg 100% 50%) 100%
    );
  }

  .round input[type="checkbox"]:checked + label::after {
    opacity: 1;
  }

  .textual-input-container {
    height: auto;
    width: 90%;
  }

  .taskValue {
    padding: 0.9rem 0 0.9rem 0.9rem;
    border-radius: 10px;
    outline: none;
    border: none;
    font-size: 21px;
    color: hsl(234, 39%, 85%);
    background-color: inherit;
    font-family: "Rubik", sans-serif;
    width: 100%;
  }

  .taskValue-toggle-bg-color {
    color: hsl(232, 8%, 20%);
    background-color: hsl(0, 0%, 98%);
  }

  .tasks-nav-filters-container {
    max-width: 50%;
    margin: -80px auto 0 auto;
    border-radius: 10px;
    background-color: hsl(235, 24%, 19%);
    box-shadow: 3px 0px 5px -7px hsl(231, 10%, 27%);
  }

  .single-task-container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    border-bottom: 1px solid hsl(235, 19%, 35%);
    padding: 15px;
    align-items: center;
  }

  .single-task-container-border-bottom-toggle {
    border-bottom: 1px solid hsl(0, 0%, 89%);
  }

  .actual-content-container {
    width: 60%;
    font-size: 15px;
    margin-left: -60px;
    cursor: pointer;
    text-align: start;
  }

  .actual-content:hover {
    color: hsl(234, 11%, 82%);
  }

  .actual-content-color-toggle:hover {
    color: hsl(231, 7%, 21%);
  }

  .task-done-content-stying {
    text-decoration: line-through;
    color: hsl(235, 19%, 35%);
  }

  .delete-btn {
    background-color: inherit;
    border: none;
    outline: none;
    margin-right: 5px;
    cursor: pointer;
    opacity: 0;
  }

  .delete-btn:hover {
    opacity: 1;
  }

  .nav-filters-container {
    display: flex;
    padding: 8px;
    justify-content: space-around;
    align-items: center;
  }

  .nav-filters-bg-toggle {
    background-color: hsl(0, 0%, 98%);
    color: hsl(234, 11%, 52%);
    box-shadow: 0px 15px 43px 8px hsl(0, 0%, 89%);
  }

  .filter-container {
    display: flex;
    padding: 10px;
    justify-content: space-between;
    width: 40%;
    align-items: center;
  }

  .all-filter {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .all-filter:hover {
    color: hsl(234, 39%, 85%);
  }

  .all-filter:focus {
    color: hsl(220, 98%, 61%);
  }

  .clear-all-tasks {
    background-color: inherit;
    border: none;
    outline: none;
    color: hsl(234, 11%, 52%);
    cursor: pointer;
  }

  .clear-all-tasks:hover {
    color: hsl(234, 39%, 85%);
  }

  .drag-and-drop-prompt {
    text-align: center;
    font-size: 14px;
    font-family: "Rubik", sans-serif;
    color: hsl(233, 14%, 45%);
    margin-top: 60px;
    margin-bottom: 50px;
    padding-bottom: 105px;
  }
}
</style>
