<template>
  <div>
    <h1 class="scope-title">Parent Content</h1>
    <ScopeFirst/>
  </div>
</template>

<script>
import ScopeFirst from "@/components/scope/ScopeFirst";

export default {
  name: "ScopeParent",
  components: {
    ScopeFirst,
  },
}
</script>

<style scoped>
.scope-title {
  color: yellow;
  font-weight: bold;
  font-size: 72px;
}
</style>
