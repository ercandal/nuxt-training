<template>
    <div>
        <nav class="navbar navbar-expand-sm navbar-dark bg-dark">
            <div class="container">
                <NuxtLink to="/" class="btn btn-light rotate-on-hover">
                    <svg class="icon-rotate-hover" xmlns="http://www.w3.org/2000/svg" width="18" height="18"
                        viewBox="0 0 576 512">
                        <path fill="currentColor"
                            d="M280.37 148.26L96 300.11V464a16 16 0 0 0 16 16l112.06-.29a16 16 0 0 0 15.92-16V368a16 16 0 0 1 16-16h64a16 16 0 0 1 16 16v95.64a16 16 0 0 0 16 16.05L464 480a16 16 0 0 0 16-16V300L295.67 148.26a12.19 12.19 0 0 0-15.3 0M571.6 251.47L488 182.56V44.05a12 12 0 0 0-12-12h-56a12 12 0 0 0-12 12v72.61L318.47 43a48 48 0 0 0-61 0L4.34 251.47a12 12 0 0 0-1.6 16.9l25.5 31A12 12 0 0 0 45.15 301l235.22-193.74a12.19 12.19 0 0 1 15.3 0L530.9 301a12 12 0 0 0 16.9-1.6l25.5-31a12 12 0 0 0-1.7-16.93" />
                    </svg>
                    <span class="ms-2">Home</span>
                </NuxtLink>
                <div class="collapse navbar-collapse" id="mynavbar">
                    <div class="d-flex flex-row w-100">
                        <li class="navbar-nav dropdown col-6">
                            <a class="nav-link dropdown-toggle text-light" href="#" role="button"
                                data-bs-toggle="dropdown">Kategoriler</a>
                            <ul class="dropdown-menu">
                                <li><a class="dropdown-item" href="/products/1">Kategori 1</a></li>
                                <li><a class="dropdown-item" href="/products">Kategori 1</a></li>
                                <li><a class="dropdown-item" href="/products">Kategori 1</a></li>
                            </ul>
                        </li>
                        <form action="/search" method="GET" class="d-flex">
                            <div class="input-group">
                                <input type="text" class="form-control" name="query" placeholder="Ara..."
                                    aria-label="Search" aria-describedby="search-button">
                                <button class="btn btn-outline-secondary rotate-on-hover" type="submit"
                                    id="search-button">
                                    <svg class="icon-rotate-hover" xmlns="http://www.w3.org/2000/svg" width="18"
                                        height="18" viewBox="0 0 512 512">
                                        <path fill="currentColor"
                                            d="M505 442.7L405.3 343c-4.5-4.5-10.6-7-17-7H372c27.6-35.3 44-79.7 44-128C416 93.1 322.9 0 208 0S0 93.1 0 208s93.1 208 208 208c48.3 0 92.7-16.4 128-44v16.3c0 6.4 2.5 12.5 7 17l99.7 99.7c9.4 9.4 24.6 9.4 33.9 0l28.3-28.3c9.4-9.4 9.4-24.6.1-34M208 336c-70.7 0-128-57.2-128-128c0-70.7 57.2-128 128-128c70.7 0 128 57.2 128 128c0 70.7-57.2 128-128 128" />
                                    </svg>
                                </button>
                            </div>
                        </form>
                        <ul class="navbar-nav col-3">
                            <li class="nav-item nav-login">
                                <NuxtLink to="/about/login" class="nav-link btn">Giris yap</NuxtLink>
                            </li>
                            <li class="nav-item nav-signup">
                                <NuxtLink to="/about/signup" class="nav-link btn">Kayıt ol</NuxtLink>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </nav>
    </div>

    
</template>

<script>
export default {
    
}
</script>

<style scoped>
.rotate-on-hover .icon-rotate-hover {
    transition: transform 0.3s ease;
}

.rotate-on-hover:hover .icon-rotate-hover {
    transform: rotate(15deg);
    scale: 1.2;
}

.nav-login:hover {
    background-color: rgb(46, 65, 82);
    transition: 0.3s ease;
}

.nav-signup:hover {
    background-color: rgb(46, 65, 82);
    transition: 0.3s ease;
}
</style>