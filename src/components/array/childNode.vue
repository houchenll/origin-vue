<template>
    <div>
        <p>name: {{ computeName }}</p>
        <p>dataName: {{ dataName }}</p>
    </div>
</template>

<script>
export default {
  props: {
    value: Object,
  },
  data() {
    return {
      dataName: '--',
    };
  },
  watch: {
    value: {
      handler: function (val) {
        console.log('childNode: ', val);
        this.dataName = val?.name;
      },
    },
  },
  computed: {
    computeName() {
        console.log('childNode computed name: ', this.value);
        return this.value?.name;
    },
  },
}
</script>

<style>
p {
    color: black;
    font-size: 32px;
}
</style>