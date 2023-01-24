<template>
  <div>
    <base-card>
      <base-button
        @click="setSelectedTab('stored-resources')"
        :mode="selectedTab === 'stored-resources' ? null : 'flat'"
        >Stored Resources</base-button
      >
      <base-button @click="setSelectedTab('stored-resources')"
        >Add Resource</base-button
      >
    </base-card>
    <component :is="selectedTab"></component>
  </div>
</template>

<script>
import StoredResources from "./StoredResources.vue";
import AddResource from "./AddResource.vue";

export default {
  components: {
    StoredResources,
    AddResource,
  },
  data() {
    return {
      selectedTab: "stored-resources",
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
  provide() {
    return {
      resources: this.storedResources,
    };
  },
  computed: {},
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>
