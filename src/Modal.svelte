<script lang="ts">

export let modalOpen: boolean;
$: console.log(modalOpen)

</script>

<section class="ref-modal" class:show-modal={modalOpen}>
  <header>
    <h3>Markdown Reference</h3>
    <div id="closer" on:click><span>X</span></div>    
  </header>
  
  <div id="img-cont">
    <img src="https://assets.codepen.io/504854/markdown_ref.jpg" alt="markdown reference guide" />
  </div>

  <footer>
    <a href="https://guides.github.com/features/mastering-markdown/#GitHub-flavored-markdown" target="_blank">More Info</a>
    </footer>
 </section>


<style>
  .ref-modal {
    position: absolute;
    width: 0;
    height: 98%;
    top: 10px;
    right: 0;
    transition: .3s width;
    overflow: auto;
  }

  .show-modal {
    width: 300px;
  }


  .ref-modal header {
    width: 100%;
    padding: 5px;
    background-color: #111;
    color: whitesmoke;
    border-bottom: 1px solid black;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  h3 {
    margin: 0;
  }

  #closer {
    font-family: 'Delius Swash Caps', cursive;
    /* width: 20px; */
    font-size: 1rem;
    padding: 4px 8px;
    margin: 5px 0;
    border: 1px solid whitesmoke;
    cursor: pointer;
    transition: all .3s ease-in-out;
  }
  #closer:hover {
    transform: rotate(180deg)
  }
  #closer:active {
    background-color: goldenrod;
    color: black;
    font-weight: bold;
  }

  #img-cont {
    margin: 0 0 -5px 0;
  }

  footer {
    width: 100%;
    padding: 10px;
    text-align: center;
    font-size: 1.3rem;
    background-color: whitesmoke;
  }
</style>