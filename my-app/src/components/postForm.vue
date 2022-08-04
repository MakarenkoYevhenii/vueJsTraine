<template>
    <div>
        <form @submit.prevent>
            <h4>создание поста</h4>
            <input type="text" placeholder="tittle" v-model="post.tittle">
            <input type="text" placeholder="body" v-model="post.body">
            <button @click="createPost"> создать</button>
        </form>

    </div>
</template>

<script>


export default {
    data() {
        return {
            post: {
                tittle: "",
                body: ""
            }
        }
    },
    methods: {
        createPost() {
            this.post.id= Date.now(),
            this.$emit("create",this.post,"sfsdf",'dsfsdfs')
            this.post={
                tittle:"",
                body:""
            }
        },
    },
}
</script>

<style scoped>
</style>