<template>
    <div class="row">
        <div class="col-sm-6 col-md-4 col-xl-3 mt-3" v-for="book in books" :key="book.id">
            <BookItem :book='book' />

        </div>
    </div>
</template>

<script>
import BookItem from './BookItem.vue';
export default {
    name: "BookList",
    components: {
        BookItem
    },
    props: {
        books: {
            type: Array,
            default: () => ([])
        }
    }
}
</script>

<style lang="scss" scoped></style>