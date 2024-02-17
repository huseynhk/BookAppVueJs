<template>
    <nav class="navbar navbar-expand-md bg-dark navbar-dark">
        <div class="container py-2">
            <a href="#" class="navbar-brand">BookBuy</a>
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link" href="#">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Books</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Contact Us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Login</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Register</a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    name: "NavBar"
}
</script>

<style  scoped>
.navbar-brand{
    padding: 0;
    margin: 0;
    color: white;
    font-weight: bold;
    font-size: 24px;
}
.nav-link{
    padding: 10px 25px;
    color: white;
    text-align: center;
}
</style> 