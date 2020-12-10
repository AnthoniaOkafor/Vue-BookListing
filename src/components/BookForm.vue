<template>
    <form class="" action="#" method="post" @submit.prevent="bookSubmit(bookTitle, bookAuthor)">
        <input type="text" name="title" id="title" value="" placeholder="Book Title" v-model="bookTitle">
        
            <input type="text" name="author" id="author" value="" placeholder="Book Author" v-model="bookAuthor">
        
        <button type="submit" name="button">Add Book</button>
    </form>
    
</template>

<script>
export default {
    name: 'BookForm',
    props: ['books'],
    data() {
        return {
            bookTitle: '',
            bookAuthor: ''
        }
    },
    methods: {
        bookSubmit(bookTitle, bookAuthor) {
            this.$emit('addBook', bookTitle, bookAuthor);
        }
    }
    
}
</script>

<style>
input {
    width: 20em;
    height: 2em;
    margin: 0 5px;
}

button {
    width: 10em;
    height: 2.5em;
    margin-left: 5px; 
    margin-bottom: 15px;
    
}

form {
    display: flex;
    justify-content: center;
    
}

@media screen and (max-width: 700px) {

    form {
        flex-direction: column;
        justify-content: center;
       
        align-items: center;
    }
        input, button {
        margin-top: 15px; 
    }
}

</style>