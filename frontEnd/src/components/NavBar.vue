<template>
    <nav nav class="navbar navbar-expand-md bg-dark navbar-dark">
        <div class="container py-2">
            <a href="#" class="navbar-brand">{{ logoName.toUpperCase() }}</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ms-auto ">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Books</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contact</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Login</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Register</a>
                    </li>
                </ul>

            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: "NavBar",
    data() {
        return {
            logoName: "BookBuy"
        }
    }
}
</script>

<style  scoped>
.navbar-brand {
    padding: 0;
    margin: 0;
    color: white;
    font-weight: bold;
    font-size: 24px;
}

.nav-link {
    padding: 10px 25px;
    color: white;
    text-align: center;
}
</style> 