<script>
  import { name } from "../store/store";
</script>

<div class="skills">
  <h3>{$name}:~$ <span class="whitetext">skills</span></h3>
  <div class="flex-item">
    <h4>Web</h4>
    <h5>Html</h5>
    <h5>Css</h5>
    <h5>Javascript</h5>
    <h5>NodeJs</h5>
    <h5>Svelte</h5>
  </div>
  <div class="flex-item">
    <h4>Mobile</h4>
    <h5>Android</h5>
    <h5>Kotlin</h5>
  </div>
  <div class="flex-item">
    <h4>Other</h4>
    <h5>C#</h5>
    <h5>Linux</h5>
    <h5>Bash</h5>
  </div>
</div>

<style lang="scss">
  .skills {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    h3 {
      width: 100%;
    }
    h5 {
      margin-top: 0.5rem !important;
    }
  }
  .flex-item {
    width: 8rem;
  }
</style>
