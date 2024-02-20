<template>
    <section>
        <div class="container">
            <SectionHeader title="Books"
                text="Books Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maiores quaerat nostrum inventore?" />
            <BookList :books="paginatedBooks" />
            <Pagination :currentPage="currentPage" :totalPages="totalPages" @pageChanged="updatePage"/>
        </div>

    </section>
</template>

<script>
import SectionHeader from '@/components/SectionHeader.vue';
import BookList from '@/components/BookList.vue';
import books from '@/db.js';
import Pagination from '@/components/Pagination.vue';
export default {
    name: "BooksView",
    components: {
        SectionHeader,
        BookList,
        Pagination,
    },
    data() {
        return {
            books: books,
            currentPage: 1,
            itemsPerPage: 4,
        }
    },
    computed: {
        totalPages() {
            return Math.ceil(this.books.length / this.itemsPerPage)
        },
        paginatedBooks() {
            const startIndex = (this.currentPage - 1) * this.itemsPerPage;
            const endIndex = startIndex + this.itemsPerPage;
            return this.books.slice(startIndex, endIndex)
        }
    },
    methods: {
        updatePage(page) {
            this.currentPage =  page;
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