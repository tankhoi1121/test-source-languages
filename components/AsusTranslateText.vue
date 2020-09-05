<template>
  <div class="wrapper-source-text">
    <label for="txtSource">
      <textarea
        id="txtSource"
        placeholder="Text to translate to."
        class="edit_box_9991"
        rows="1"
        name="txtSource"
      ></textarea>
    </label>
  </div>
</template>
<style>
.wrapper-source-text {
  width: 50%;
  border: 1px solid red;
  min-height: 268px;
}

.edit_box_9991 {
  backface-visibility: hidden;
  overflow: hidden;
  border: 0;
  outline: none;
  resize: none;
  display: inline-block;
  background: transparent;
  width: 100%;
}

label {
  width: 100%;
}
</style>

<script>
setTimeout(() => {
  var x = document.getElementById("txtSource");
  document.getElementById("txtSource").addEventListener("keydown", (event) => {
    if (event.isComposing || event.keyCode === 13) {
      setTimeout(() => {
        x.style.cssText = "height:auto; padding:0";
        x.style.cssText = "height:" + x.scrollHeight + "px";
      }, 0);
    }
  });
}, 5000);
</script>