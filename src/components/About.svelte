<script>
  import { name } from "../store/store";
</script>

<div class="about">
  <h3>{$name}:~$ <span class="whitetext">about me</span></h3>
  <div class="aboutmetext">
    <h4>
      My name is Eetu, I am a passionate software developer currently studying
      in the field. I am interested in web and Android development and also
      Linux. In my free time i like to code and exercise. I have built multiple
      websites&webapps and also some android apps.
    </h4>
  </div>
</div>

<style lang="scss">
  .aboutmetext {
    width: 60%;
    line-height: 1.5;
    // letter-spacing: 0.05rem;
  }
  h3 {
    color: $foreground-color;
    margin-top: 1rem;
    margin-left: 1rem;
    font-size: 1.5rem;
  }
  h4 {
    color: $white;
    margin-top: 1rem;
    margin-left: 1rem;
    font-size: 1rem;
  }
</style>
