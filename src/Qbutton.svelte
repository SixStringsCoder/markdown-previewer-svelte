<script lang="ts"></script>

<section id="q-btn-cont">
  <button id="q-btn" on:click>?</button>    
</section>

<style>
  section#q-btn-cont {
    width: 100%;
    display: flex;
    justify-content: center;
  }

  button#q-btn {
    font-family: 'Delius Swash Caps', cursive;
    font-size: 1.5rem;
    margin: 10px auto 0;
    padding: 5px 10px;
    cursor: pointer;
    transition: all .3s ease-in-out;
  }
  button#q-btn:hover {
    transform: rotate(360deg)
  }
  button#q-btn:active {
    background-color: goldenrod;
    color: black;
  }

</style>