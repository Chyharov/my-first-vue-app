<template>

    <div v-if="posts.length > 0">
        <!-- <div v-show="posts.length > 0"> буде відображати в інспекті -->
        <h3>Список користувачів</h3>

        <post-item 
        v-for="post in posts"
        :post="post"
        :key="post.id"
        @remove="$emit('remove', post)"
        />
        
    </div>

    <h2 v-else style="color: red">
        <!-- < v-show="posts.length === 0" style="color: red"> буде відображати в інспекті -->
        Зараз немає жодної публікації
    </h2>

</template>

<script>
import PostItem from './PostItem.vue'
    export default {
  components: { PostItem },
    props: {
            posts: {
                type: Array,
                required: true
            }
        }
    }
</script>

<style scoped>


</style>