<template>
    <form @submit.prevent="addToDo">
        <input type="text" v-model="nuevoToDo">
        <button type="submit">Añadir</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            nuevoToDo: ''
        }
    },
    methods: {
        addToDo() {
            if (this.nuevoToDo) {
                this.$emit('addtodo', {
                    descrip: this.nuevoToDo,
                    done: false
                })
                this.nuevoToDo = ''
            }
        },
    }
}
</script>