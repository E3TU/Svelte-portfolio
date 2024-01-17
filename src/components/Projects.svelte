<script>
  import { name } from "../store/store";
</script>

<div class="projects">
  <h3>{$name}:~$ <span class="whitetext">projects</span></h3>
  <div class="project-item">
    <h4>Android password generator</h4>
    <a href="https://github.com/E3TU/Android-passwordgen">GitHub</a>
  </div>
  <div class="project-item">
    <h4>Javascript todo app</h4>
    <a href="https://github.com/E3TU/TodoApp">GitHub</a>
  </div>
  <div class="project-item">
    <h4>Javascript clock app</h4>
    <a href="https://github.com/E3TU/clock">GitHub</a>
  </div>
  <div class="project-item">
    <h4>Svelte WeatherApp</h4>
    <a href="https://github.com/E3TU/WeatherApp">GitHub</a>
  </div>
</div>

<style lang="scss">
  .projects {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    h3 {
      width: 100%;
    }
    h4 {
      margin-left: 1rem;
      color: $foreground-color;
    }
    a {
      margin-left: 1rem;
      background-color: transparent;
      color: $white;
      font-size: 0.8rem;
    }
  }
  .project-item {
    width: auto;
  }
</style>
