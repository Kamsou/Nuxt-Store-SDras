<template>
  <main>
    
    <section>
      <h1>Projects</h1>
      <div v-for="project in githubProjects" :key="project.id">
        <h3>
          <a :href="project.html_url">
          {{ project.name }}
          </a>
        </h3>
        <p>
          {{ project.stargazers_count }}
        </p>
        <p>
          {{ project.homepage }}
        </p>
        <p>
          {{ project.description }}
        </p>
      </div>
    </section>
    <aside>
      <h3>About</h3>
      <p>I am fancy. Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid, earum facilis harum quis natus quisquam. Sapiente aperiam praesentium tempore cumque placeat laborum ipsam, tempora laboriosam unde quas dolore, iure quidem!</p>
    </aside>
  </main>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: {
    ...mapState([
      'githubProjects',
    ])
  },

  mounted() {
    this.$store.dispatch("getGithubProjects")
  }
}
</script>

<style lang="scss" scoped>
main {
  width: 80vw;
  margin: 2% 8%;
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-template-rows: 1fr;
  grid-column-gap: 50px;
  grid-row-gap: 0px;
  section{ 
    grid-area: 1 / 1 / 2 / 2; 
    background: black;
    color: white;
    padding: 30px;
    a {
      color: green;
    }
    }
  aside { 
    grid-area: 1 / 2 / 2 / 3;
    }
}


</style>