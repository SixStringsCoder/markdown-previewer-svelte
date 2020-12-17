<script lang="ts">
  
  export let markDown: string;
</script>

<section id="editor-cont">
  <textarea id="editor" 
            placeholder="Type markdown here"
            on:change
            bind:value={markDown} />
</section>

<style>
  section#editor-cont {
    width: 100%;
    display: flex;
    justify-content: center;
  }

  #editor {
    width: 80%;
    height: 200px;
    padding: 10px;
    font-size: 1.2rem;
    resize: none;
    box-shadow: inset 0 0 3px black;
  }
</style>