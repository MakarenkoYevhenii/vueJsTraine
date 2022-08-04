<template>
    <div>
        <div class="post" v-for="post in posts" v-bind:key="post.id">
            название {{ post.tittle }}
            описание {{ post.body }}
            <button>удалить</button>
        </div>

    </div>
</template>

<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true
        }
    }
}
</script>

<style scoped>
.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 15px;
}
</style>