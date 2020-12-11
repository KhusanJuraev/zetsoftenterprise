<template>
    <b-form-checkbox-group
      v-model="selected"
      :options="options"
      class="mb-3 d-flex mb-2"
      :class="flex"
    ></b-form-checkbox-group>
</template>

<script>
export default {
  name: "Checkbox",
  props: ["selected", "options", "flex"],
}
</script>

<style scoped>
</style>
