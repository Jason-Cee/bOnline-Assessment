<template>
    <div class="main">
        <div class="content">
            <span></span>
            <button><i class="fa-solid fa-house"> Home</i></button>
        </div>
        <div class="content">
            <span></span>
            <button><i class="fa-solid fa-credit-card"> Billing</i></button>
        </div>
    </div>
</template>

<script>

</script>

<style>
    .main{
        width: 10vw;
        height: 100vh;
        left: 0;
        background-color: #fff;
        border-right: 1px solid #F7F8FA;
        position: fixed;
    }

    .content{
        transition: .2s ease-in;
        width: 100%;
        /* height: 50px; */
        display: flex;
        justify-content: center;
        align-items: center;
    }


    .content button{
        background: none;
        border: none;
        width: 80%;
        height: 50px;
        transition: .2s ease;
        border-radius: 10px;
    }
    .content button:hover {
        background-color: #1E8CEB;
        color: #fff;
    }
</style>