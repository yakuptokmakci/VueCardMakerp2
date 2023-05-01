<template>
   <body>
        <div class="d-flex align-items-center justify-content-center vh-100 bg-warning ">
            <div class="text-center">
                <h1 class="display-1 fw-bold">404</h1>
                <p class="fs-3"> <span class="text-danger">Opps!</span> Page not found.</p>
                <p class="lead">
                    Sorry pal the page you are looking for does not exist !!!!
                  </p>
                <router-link :to="{name:'home'}" class="btn btn-dark">
                    Go home
                </router-link>
            </div>
        </div>
    </body>
</template>

