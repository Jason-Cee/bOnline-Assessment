<template>
    <div class="table_main">
        <div class="table_header">
            <h3>Billing History</h3>
            <p>Choose a billing plan to see more details</p>
        </div>    
        <div class="table_data" v-for="item in data" :key="item.id">
            <div class="table_title">
                <div class="dates">
                    <h4>Date</h4>

                    <p>25 Feb 2022</p>
                    <p>25 Feb 2022</p>
                    <p>25 Feb 2022</p>
                    <p>25 Feb 2022</p>
                    <p>25 Feb 2022</p>
                    <p>25 Feb 2022</p>
                </div>
                <div class="types">
                    <h4>Type</h4>

                    <p>Invoice</p>
                    <p>Invoice</p>
                    <p>Invoice</p>
                    <p>Invoice</p>
                    <p>Invoice</p>
                    <p>Invoice</p>
                </div>
                <div class="amounts">
                    <h4>Amount</h4>

                    <p>€8.00</p>
                    <p>€8.00</p>
                    <p>€8.00</p>
                    <p>€8.00</p>
                    <p>€8.00</p>
                    <p>€8.00</p>
                </div>
                <div class="balance">
                    <h4>Balance</h4>

                    <p>€{{item.balance}}</p>
                    <p>€{{item.balance}}</p>
                    <p>€{{item.balance}}</p>
                    <p>€{{item.balance}}</p>
                    <p>€{{item.balance}}</p>
                    <p>€{{item.balance}}</p>
                </div>
                <div class="reference">
                    <h4>Reference</h4>

                    <p>{{item.account_id}}</p>
                    <p>{{item.account_id}}</p>
                    <p>{{item.account_id}}</p>
                    <p>{{item.account_id}}</p>
                    <p>{{item.account_id}}</p>
                    <p>{{item.account_id}}</p>
                </div>
                <div class="download">
                    <h4>Download</h4>

                    <p><i class="fa-solid fa-download"></i></p>
                    <p><i class="fa-solid fa-download"></i></p>
                    <p><i class="fa-solid fa-download"></i></p>
                    <p><i class="fa-solid fa-download"></i></p>
                    <p><i class="fa-solid fa-download"></i></p>
                    <p><i class="fa-solid fa-download"></i></p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Data from '../assets/Data.json'

 export default {
     name: 'Table',
     data(){
      return{
        data: Data
      }
    }
 }
</script>

<style>
    .table_main{
        background-color: #FFF;
        width: 90%;
        height: 30vh;
        overflow-y: scroll;

    }
    .table_title{
        display: flex;
        width: 90%;
        flex-direction: row;
        justify-content: space-evenly;
        border-bottom: 1px solid #F0F0F0;
    }

</style>