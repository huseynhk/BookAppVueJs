<template>
    <div class="card border-0 shadow position-relative">
        <img src="../../public/images/main.jpg" alt="main" class="card-img-top imgs">

        <div class="card-body bg-dark-subtle py-3 ">
            <div class="text-center ">
                <span class="py-1 px-2 bg-dark text-white rounded-pill  ">{{ book.author }}</span>
                <h5 class="mb-2 mt-3  card-title fw-semibold">{{ book.name }}</h5>
                <p class="card-text mb-2">
                    {{ book.description }}
                </p>
                <div class="d-flex justify-content-between  align-items-center px-3">
                    <a href="#" class="card-link">Read More</a>
                    <p class="py-1 px-2 bg-dark text-white badge mb-0"> {{ book.uploadDate }}</p>
                </div>
            </div>
            <span :class="ratingBadgeClass"
                class="position-absolute top-0 start-100  translate-middle p-2  text-warning rounded-pill border border-2 border-warning">
                {{ book.rating }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: "BookItem",
    props: {
        book: {
            type: Object,
            default: () => ([])
        }
    },
    computed: {
        ratingBadgeClass() {
            if (this.book.rating > 8) {
                return 'bg-success'
            }
            else if (this.book.rating > 5) {
                return 'bg-secondary'
            }
            else {
                return 'bg-danger'

            }
        }
    }
}
</script>

<style lang="scss" scoped></style>