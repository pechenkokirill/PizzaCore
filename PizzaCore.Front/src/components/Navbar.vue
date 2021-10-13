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
        background: black;
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