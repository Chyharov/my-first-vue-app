<template>
    <div class="app">
        <post-form
        @create="createPost"
        />
        <post-list 
        :posts="posts"
        @remove="removePost"
        />
    </div>

</template>

<script>
import PostForm from "@/components/PostForm.vue"
import PostList from "@/components/PostList.vue"

export default {
    components: {
        PostList, PostForm
    },
    data() {
        return {
            posts: [
                { id: 1, title: 'JavaScript', body: 'Опис посту' },
                { id: 2, title: 'JavaScript 2', body: 'Опис посту 2' },
                { id: 3, title: 'JavaScript 3', body: 'Опис посту 3' },
                { id: 4, title: 'JavaScript 4', body: 'Опис посту 4' },
            ],
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
        },
        removePost(post) {
            this.posts = this.posts.filter(p => p.id !== post.id)
        }
    }
}
</script>

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.app {
    padding: 20px;
}

</style>

<!-- <div>
        <div>
            <button @click="addLike">Like</button>
            <button @click="addDislike">Dislike</button>
        </div>
<div>Кількість лайків: <strong>{{ likes }}</strong></div>
<div>Кількість дизлайків: <strong>{{ dislikes }}</strong></div>
    </div> -->