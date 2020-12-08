<template>
    <div>
        <h1>{{title}}</h1>
        <ul>
            <li>
                <book-item v-for="book in books">
                    {{book.title}}:{{book.author}}
                </book-item>
            </li>
        </ul>
        
    </div>
</template>

<script>
export default {
    name: 'BookList',
    data() {
       return {
            title: 'All Books',
            books: [
                    {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
                    {title: 'American Gods', author: 'Neil Gaiman'},
                    {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
            ]
        }

    }

}
</script>

<style>
    h1, h2 {
        font-weight: normal
    }

   
   
</style>