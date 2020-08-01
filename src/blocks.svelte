<script>
export let color;
export let opacity;

function changeElem(e){
  e.preventDefault();
  document.getElementById("elem1").style.backgroundColor = color;
  document.getElementById("elem1").style.opacity = opacity;
}
</script>
<style>
.elem1{
  width: 100px;
  height: 100px;
  border: 1px solid black;
}
</style>
		<form on:submit={changeElem}>
		<label for="color">Color</label>
		<input id="color" bind:value={color} name="color" placeholder="#fff or blue"/>
		<label for="opacity">Opacity (from 0 to 1)</label>
		<input id="opacity" bind:value={opacity} name="opacity" placeholder="Ex: 0.3"/>
		<button type="submit">Ok</button>
		</form>
<div id="elem1" class="elem1">
</div>