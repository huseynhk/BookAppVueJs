<template>
    <section>
        <div class="container">
            <SectionHeader title="Books"
                text="Books Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maiores quaerat nostrum inventore?" />
            <BookList :books="books" />
        </div>

    </section>
</template>

<script>
import SectionHeader from '@/components/SectionHeader.vue';
import BookList from '@/components/BookList.vue';
import books from '@/db.js';
export default {
    name: "BooksView",
    components: {
        SectionHeader,
        BookList,
    },
    data() {
        return {
            books: books,
        }
    }
}
</script>

<style  >
.imgs {
    height: 180px;
    width: 100%;
    object-fit: cover;
    border-radius: 10px 10px 0 0;
}
</style>