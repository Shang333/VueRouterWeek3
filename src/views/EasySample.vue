<template>
    <div class="container">
        <header class="header g-4">這裡是header</header>
        <div class="row">
            <div class="col-4" v-for="i in 10" :key="i">
                <div class="card">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQeHt6_iRQt98JBuAk0XvrQAWvUIiFCgyP8CQ&s" alt="..."/>
                    <div class="card-body">
                        <h5 class="card-title">card title</h5>
                        <p class="card-text">AGHHDJWDBWJDKQWJEQNDQJNQKJDNJWNJDNWJNDJQNBDBHghfdjwq12</p>
                        <a href="#" class="btn btn-primary">Go somewhere</a>
                    </div>
                </div>
            </div>
        </div>
        <footer class="footer">這裡是footer</footer>
    </div>
</template>

<style>
.header{
    height: 200px;
    background-color: lightcoral;
}
</style>

<script>

</script>