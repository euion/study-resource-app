<template>
  <ul>
    <stored-resources :resources="storedResources"></stored-resources>
  </ul>
</template>

<script>
import StoredResources from "./components/learning-resources/StoredResources.vue";

export default {
  components: {
    StoredResources,
  },
  data() {
    return {
      //더미 리소스 2개
      storedResources: [
        {
          id: "study-vue.js",
          title: "Study Vue",
          description: "The Officieal Vue.js documentation",
          link: "https://vuejs.org",
        },
        {
          id: "study-react.js",
          title: "Study React",
          description: "The Officieal React.js documentation",
          link: "https://ko.reactjs.org/",
        },
      ],
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");

* {
  box-sizing: border-box;
}

html {
  font-family: "Roboto", sans-serif;
}

body {
  margin: 0;
}
</style>
