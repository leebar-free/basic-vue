<template>
    <div>
        <!-- <h1>{{ title }}</h1> -->
        <!-- <p> {{ name }} </p> -->
        <!-- <button @click="updateName">Change Name</button> -->
        <p>header</p>
        <slot name="header" :kossie="kossie"></slot>
        <p>body</p>
        <slot name="body"></slot>
        <p>footer</p>
        <slot name="footer"></slot>
        <slot></slot>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            default: "default title"
            // required: true
        },
        name: {
            type: String,
            default: "default Kossie Coder"
        }
    },
    data() {
        return {
            // name: 'Kossie Coder',
            kossie: 'kossie'
        }
    },

    methods: {
        updateName() {
            this.name = "Kossie Coder Updated";
        }
    }
}
</script>

<style scoped>

</style>
