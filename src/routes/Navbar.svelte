<header class="navbar">
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#container2">About me</a></li>
      <li><a href="#container3">Skills</a></li>
      <li><a href="#container4">Projects</a></li>
      <li><a href="#container5">Contact</a></li>
    </ul>
  </nav>
</header>

<style lang="scss">

  $background-color: #191919;
  $foreground-color: #148a55;
  $white: #ffffff;
  $black: #000;
  $lighter-gray: #252525;

  .navbar {
    display: flex;
    position: fixed;
    height: 100%;
    width: 25rem;
    background-color: #148a55;
    align-items: center;
    justify-content: flex-start;
  }
  ul {
    display: flex;
    list-style: none;
     flex-direction: column;
    flex-direction: column;
    font-size: 1.75rem;
    margin-left: 5rem;
    li {
      padding: 1rem;
      a {
        text-decoration: none;
        color: $white;
        transition: 1s;
        &:hover{
          color: $background-color;
          transition: 1s;
        }
      }
    }
  }
</style>
