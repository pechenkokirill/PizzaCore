<template>
    <div class="nav">
        <div class="flex">
           <router-link to="/">
                <div id="nav-logo">
                    <img src="../../public/img/pizzaicon.png" width="32" height="32" alt="">
                    <span class="text-white">PizzaCore</span>
                </div>
           </router-link>
        </div>
    </div>
</template>

<style>
    .nav
    {
        background: rgb(26, 26, 26);
        box-shadow: 0 4px 10px rgb(63 93 138 / 50%);
        padding: 32px;
    }

    #nav-logo
    {
        font-size: 21pt;
        font-family: 'Meter';
    }

    #nav-logo > img
    {
        margin-right: 8px;
        float: left;
    }
</style>