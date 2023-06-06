<template>
    <childNode :value="objArr[0]"></childNode>
</template>

<script>
import childNode from "./childNode.vue";

export default {
  components: {
    childNode,
  },
  data() {
    return {
        objArr: [],
    };
  },
  mounted() {
    this.initArr();
  },
  methods: {
    initArr() {
        for (let i = 0; i < 5; i++) {
            this.objArr.push({
                name: `name${i}`,
            });
        }
    },
  },
}
</script>