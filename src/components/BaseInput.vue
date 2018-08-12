<template>
  <input type="text" :placeholder='placeholder' :value='value' @input='valueChanged($event.target.value)' @keyup.enter="itemAdded">
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: ''
    },
    placeholder: {
      type: String
    }
  },
  methods: {
    valueChanged(value){
      this.$emit("input", value);
    },
    itemAdded(){
      this.$emit('itemAdded');
    }
  }
};
</script>

<style scoped>

</style>
