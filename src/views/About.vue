<template>
  <div class="about">
    <h1>This is an about page</h1>
    <KossieCoder>
      <template v-slot:header="props">
        <h1>hello...header {{ props.kossie }}</h1>
      </template>
      <template #footer>
        <h1>hello...footer</h1>
      </template>
      <template #default>
        <h1>hello...default</h1>
      </template>

    </KossieCoder>
  </div>
</template>

<script>
import KossieCoder from '../components/KossieCoder.vue';

export default {
  components: {
    KossieCoder
  },
}
</script>