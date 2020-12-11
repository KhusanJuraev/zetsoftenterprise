<template>
    <b-form-checkbox-group
      v-model="selected"
      :options="options"
      class="mb-3"
    ></b-form-checkbox-group>
</template>

<script>
export default {
  name: "Checkbox",
  props: ["selected", "options"],
}
</script>

<style scoped>

</style>
