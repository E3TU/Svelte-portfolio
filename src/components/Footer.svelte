<script>
  import { name } from "../store/store";
</script>

<div class="footer">
  <h3>{$name}:~$ <span class="whitetext"></span></h3>
</div>

<style lang="scss">
  @media only screen and (max-width: 850px) {
    .footer {
      display: none;
    }
  }
</style>
