<template>
  <!-- <div>
    <button @click="filteredItems">All</button>
    <button @click="filteredItems">JS</button>
    <button @click="filteredItems">Vue</button>
    <button @click="filteredItems">React</button>
  </div> -->
  <div class="projects">
    <div class="item">
      <div v-for="project in projects" :key="project.id">
        <a :href="project.url" target="_blank">
          <img :src="project.img" :alt="project.text" />
        </a>

        <a :href="project.url" target="_blank" class="btn-light">
          <i class="fas fa-eye"></i> Project
        </a>
        <a :href="project.github" target="_blank" class="btn-dark">
          <i class="fab fa-github"></i> Github
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: "9",
          text: "Live Chat",
          img: require("../assets/images/projects/chatroom.png"),
          url: "https://live-chat-a3bf2.web.app/chatroom",
          github: "https://github.com/rjmcbain/Vue-Live-Chat",
          tech: "vue",
        },
        {
          id: "10",
          text: "Hiker Blog",
          img: require("../assets/images/projects/hikerblog.png"),
          url: "https://hikers-blog.web.app/",
          github: "https://github.com/rjmcbain/Vue-Hiker-Blog",
          tech: "vue",
        },
        {
          id: "1",
          text: "Loruki",
          img: require("../assets/images/projects/loruki.jpg"),
          url: "https://loving-hugle-f16475.netlify.app/",
          github: "https://github.com/rjmcbain/loruki-website",
          tech: "js",
        },
        {
          id: "2",
          text: "Wildfire Tracker",
          img: require("../assets/images/projects/wildfire.jpg"),
          url: "https://stormy-shore-09827.herokuapp.com/",
          github: "https://github.com/rjmcbain/react-wildfire-tracker",
          tech: "react",
        },
        {
          id: "3",
          text: "Gradius",
          img: require("../assets/images/projects/gradius.png"),
          url: "https://rjmcbain.github.io/Gradius/",
          github: "https://github.com/rjmcbain/Gradius",
          tech: "js",
        },
        {
          id: "4",
          text: "Github Users",
          img: require("../assets/images/projects/githubfinder.png"),
          url: "https://gifted-pare-8f6fde.netlify.app/",
          github: "https://github.com/rjmcbain/github-finder-JS",
          tech: "js",
        },
        {
          id: "5",
          text: "Word Beater",
          img: require("../assets/images/projects/wordbeater.png"),
          url: "https://rjmcbain.github.io/JS-wordbeater/",
          github: "https://github.com/rjmcbain/JS-wordbeater",
          tech: "js",
        },
        {
          id: "6",
          text: "Drag N Drop",
          img: require("../assets/images/projects/dragndrop.png"),
          url: "https://reverent-pare-fb5fd0.netlify.app/",
          github: "https://github.com/rjmcbain/dragndrop",
          tech: "js",
        },
        {
          id: "7",
          text: "DevConnector",
          img: require("../assets/images/projects/devconnector.jpg"),
          url: "https://devconnectorreactapp.herokuapp.com/",
          github: "https://github.com/rjmcbain/devconnector",
          tech: "react",
        },
        {
          id: "8",
          text: "Todos",
          img: require("../assets/images/projects/todos.png"),
          url: "https://rjmcbain.github.io/Todos_JS/",
          github: "https://github.com/rjmcbain/Todos_JS",
          tech: "js",
        },
      ],
    };
  },
  // computed: {
  //   filteredItems() {
  //     return this.projects.filter((item) => {
  //       console.log(item.tech);
  //       return item;
  //     });
  //   },
  // },
};
</script>

<style scoped>
.projects {
  margin: 5% 0;
}
.item {
  display: contents;
}
</style>
