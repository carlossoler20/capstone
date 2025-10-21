<template>
    <!-- Remix Icon -->
    <link href="https://cdn.jsdelivr.net/npm/remixicon@4.6.0/fonts/remixicon.css" rel="stylesheet">
    <header class="bg-light shadow-sm py-2">
        <div class="container">
            <div class="d-flex justify-content-between align-items-center">

                <!-- Logo -->
                <div class="d-flex align-items-center">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Emirates_logo.svg/131px-Emirates_logo.svg.png"
                        alt="Logo" class="me-2">
                    <span class="fw-bold fs-5 d-none d-md-inline">MyStore</span>
                </div>

                <!-- Desktop Navigation -->
                <nav class="d-none d-md-flex">
                    <a href="#" class="nav-link text-dark">Home</a>
                    <a href="#" class="nav-link text-dark">Shop</a>
                    <a href="#" class="nav-link text-dark">About</a>
                    <a href="#" class="nav-link text-dark">Contact</a>
                </nav>

                <!-- Right Section -->
                <div class="d-flex align-items-center">
                    <!-- Desktop Search Bar -->
                    <div class="d-none d-md-block me-3">
                        <input type="text" class="form-control form-control-sm" placeholder="Search...">
                    </div>
                    <a href="#" class="btn text-dark d-none d-md-block">
                        <i class="ri-login-circle-line"></i>
                    </a>
                    <a href="#" class="btn text-dark d-none d-md-block">
                        <i class="ri-shopping-cart-2-line"></i>
                    </a>

                    <!-- Mobile Menu Button -->
                    <button class="btn btn-outline-secondary d-md-none" @click="toggleMenu">
                        <i class="ri-menu-line"></i>
                    </button>
                </div>
            </div>

            <!-- Mobile Menu -->
            <div v-show="showMenu" class="d-md-none mt-2">
                <nav class="mb-3 d-flex flex-column align-items-center">
                    <a href="#" class="nav-link text-dark">Home</a>
                    <a href="#" class="nav-link text-dark">Shop</a>
                    <a href="#" class="nav-link text-dark">About</a>
                    <a href="#" class="nav-link text-dark">Contact</a>
                </nav>
                <div class="mb-3">
                    <a href="#" class="btn w-100 mb-2">
                        <i class="ri-login-circle-line"></i>
                    </a>
                    <a href="#" class="btn w-100 mb-2">
                        <i class="ri-shopping-cart-2-line"></i>
                    </a>
                </div>
                <input type="text" class="form-control" placeholder="Search...">
            </div>
        </div>
    </header>

</template>

<script setup>
import { ref } from 'vue';
const showMenu = ref(false);
const toggleMenu = () => {
    showMenu.value = !showMenu.value;
}

</script>
<style scoped>
#mobileMenu {
    display: none;
    background-color: #f8f9fa;
    padding: 1rem;
}

@media (min-width: 768px) {
    #mobileMenu {
        display: none !important;
    }
}

.nav-link {
    padding: 0.5rem 1rem;
}
</style>