<template>
    <div class="app">
        <form @submit.prevent>
            <h3>Сворення посту</h3>
            <input 
            v-bind:value="title" 
            @input="title = $event.target.value "
            class="input" 
            type="text" 
            placeholder="Назва"
            >
            <input 
            v-bind:value="body" 
            @input="body = $event.target.value"
            class="input" 
            type="text" 
            placeholder="Опис"
            >
            <button class="btn" @click="createPost">Створити</button>
        </form>

        <div class="post" v-for="post in posts">

            <div><strong>Назва:</strong> {{ post.title }}</div>

            <div><strong>Опис:</strong> {{ post.body }}</div>

        </div>
    </div>

</template>

<script>

export default {
    data() {
        return {
            posts: [
                { id: 1, title: 'JavaScript', body: 'Опис посту' },
                { id: 2, title: 'JavaScript 2', body: 'Опис посту 2' },
                { id: 3, title: 'JavaScript 3', body: 'Опис посту 3' },
                { id: 4, title: 'JavaScript 4', body: 'Опис посту 4' },
            ],
            title: '',
            body: ''
        }
    },
    methods: {
        createPost(event) {
            event.stopPropagation()
            const newPost = {
                id: Date.now(),
                title: this.title,
                body: this.body,
            }
            this.posts.push(newPost);
            this.title = '';
            this.body = '';
        },
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

.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 15px;
}

form {
    display: flex;
    flex-direction: column;
}

.input {
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin: 15px 0;
}

.btn {
    margin-top: 15px;
    align-self: flex-end;
    padding: 10px 15px;
    background: none;
    color: teal;
    border: 1px solid teal;
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