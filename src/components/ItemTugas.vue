<template>
  <div>
    <div class="form-check">
      <input
        class="form-check-input"
        type="checkbox"
        onclick=""
        value=""
        id="defaultCheck1"
      />
      <label
        class="form-check-label item item-complate"
        v-bind:class="{ 'item-complate': tugasSaya.isDone }"
        for="defaultCheck1"
      >
        {{ tugasSaya.namaTugas }}
      </label>
    </div>
  </div>
</template>

<script>
export default {
  name: "tugasSaya",
  props: ["tugasSaya"],
};
</script>

<style scoped></style>
