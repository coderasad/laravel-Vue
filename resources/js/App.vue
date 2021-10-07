<template>
    <div>
        <nav>
            <div class="nav-item d-flex">
                <router-link to="/" class="nav-link">Home</router-link>
                <router-link to="/about" class="nav-link">About</router-link>
                <router-link to="/contact" class="nav-link">Contact</router-link>
            </div>
        </nav>
        <router-view></router-view>
    </div>
</template>

<script>
export default {

}
</script>
