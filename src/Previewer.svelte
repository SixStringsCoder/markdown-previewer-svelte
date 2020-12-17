<script lang="ts">
  export let displayHTML;
</script>


<section id="preview-cont">
  <div id="preview">{@html displayHTML}</div>
</section>


<style>
section#preview-cont {
  width: 100%;
  display: flex;
  justify-content: center;
}

#preview {
  margin-top: 3%;
  background-color: #ddd;
  width: 80%;
  height: 400px;
  padding: 10px;
  font-size: 1.2rem;
  overflow: auto;
  box-shadow: inset 0 0 3px black;
}
</style>