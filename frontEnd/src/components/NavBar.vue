<template>
    <nav nav class="navbar navbar-expand-md bg-dark navbar-dark">
        <div class="container py-2">
            <RouterLink v-bind:to="{ name: 'Home' }" class="navbar-brand">{{ logoName.toUpperCase() }}</RouterLink>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ms-auto ">
                    <li class="nav-item">
                        <RouterLink v-bind:to="{ name: 'Home' }" class="nav-link">
                            Home </RouterLink>

                    </li>
                    <li class="nav-item">
                        <RouterLink v-bind:to="{ name: 'Books' }" class="nav-link">
                            Books </RouterLink>

                    </li>
                    <li class="nav-item">
                        <RouterLink v-bind:to="{ name: 'Contact' }" class="nav-link">
                            Contact </RouterLink>

                    </li>
                    <li class="nav-item">
                        <RouterLink v-bind:to="{ name: 'Login' }" class="nav-link">
                            Login </RouterLink>

                    </li>
                    <li class="nav-item">
                        <RouterLink v-bind:to="{ name: 'Register' }" class="nav-link">
                            Register </RouterLink>

                    </li>
                </ul>

            </div>
        </div>
    </nav>
</template>

<script>
import { RouterLink } from 'vue-router';

export default {
    name: "NavBar",
    data() {
        return {
            logoName: "BookBuy"
        };
    },
    components: { RouterLink }
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
    padding: 10px 20px !important;
    color: white;
    text-align: center;
}

.nav-link:hover {
    color: rgb(180, 225, 250);
}

.active-link {
    color: rgb(180, 225, 250);

}
</style> 