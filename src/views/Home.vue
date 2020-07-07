<template>
  <div>
    <h1>This is Home page</h1><br>
    <!-- <p> {{ name }} </p> -->
    <!-- <KossieCoder title="Home title" name="Kossie Coder1" /> -->
    <form action="">
      <InputField v-model="name" />
      <br><button @click.prevent="updateName">Submit</button>
    </form>
    {{ name }}
  </div>
</template>

<script>
// import KossieCoder from '../components/KossieCoder.vue';
import InputField from '@/components/InputField.vue';

export default {
  components: {
    // KossieCoder
    InputField
  },
  data() {
    return {
      name: 'Kossie Coder'
    }
  },

  beforeCreate() {
    console.log("beforeCreate :: ", this.name);
  },
  created() {
    console.log("created :: ", this.name);
  },
  beforeMount() {
    console.log("beforeMount :: ", this.name);
  },
  mounted() {
    console.log("mounted :: ", this.name);
  },
  beforeUpdate() {
    console.log("beforeUpdate :: ", this.name);
  },
  updated() {
    console.log("updated :: ", this.name);
  },
  beforeDestory() {
    console.log("beforeDestory :: ", this.name);
    alert("beforeDestory");
  },
  destroyed() {
    console.log("destroyed :: ", this.name);
  },

  methods: {
      updateName() {
          this.name = 'hello...';
      }
  }
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>



<!--
<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
-->
