<template>
  <div class="bill">
    <div class="wrapper" v-for="item in data" :key="item.id">
      <div class="header">
        <h1>Billing</h1>
        <p>Overview of your accounts</p>
      </div>
      <div class="accounts_container">
        <div class="accounts_content first">
            <h3>{{item.first_name}} {{item.last_name}}
              <span>Active</span>
            </h3>
            <div class="account_id">
              <h4>Account ID: {{item.account_id}}</h4>
            </div>
        </div>
        <div class="accounts_content">
            <h3>{{item.first_name}} {{item.last_name}}
              <span>Active</span>
            </h3>
            <div class="account_id">
              <h4>Account ID: {{item.account_id}}</h4>
            </div>
        </div>
        <div class="accounts_content">
            <h3>{{item.first_name}} {{item.last_name}}
              <span>Active</span>
            </h3>
            <div class="account_id">
              <h4>Account ID: {{item.account_id}}</h4>
            </div>
        </div>
      </div>
      <div class="payment_container">
        <div class="payment_details">
          <div class="payment_title">
            <h4>Payment Details</h4>
            <p>View details of your next invoice and payment method</p>
          </div>
          <div class="invoice">
            <h5>Next invoice: {{item.next_invoice_date}}</h5>
          </div>
          <div class="payment_row">
            <div class="payment_box">
              <div class="payment_box_title">
                <h5>Current Balance</h5>
                <h5>€{{item.balance}}</h5>
              </div>
              <div class="payment_info">
                <h6><i class="fa-solid fa-lock"></i></h6>
                <p>This is a secure 256-bit SSL encrypted payment. You're safe.</p>
              </div>
              <div class="payment_button">
                <button>Pay Now</button>
              </div>
            </div>
            <div class="payment_box">
              <div class="payment_box_title">
                <h5>Payment Method</h5>
                <span>Annual</span>
              </div>
              <div class="payment_info">
                <h6><i class="fa-solid fa-lightbulb"></i></h6>
                <p>
                  <span>Guide:</span>
                  To Manage your payments more easily, we recommend switching to Direct Debit.
                </p>
              </div>
              <div class="payment_button">
                <button>Switch to Direct Debit</button>
              </div>
            </div>
          </div>
        </div>
        <div class="payment_details payment_products">
          <div class="payment_title">
            <h4>My products</h4>
            <p>All your products at a glance</p>
          </div>
          <div class="payment_product">
            <i class="fa-solid fa-phone"></i>
            <h6>{{item.products.product_kind}} - </h6>
            <p>{{item.products.product_detail}}</p>
          </div>
          <div class="payment_product">
            <i class="fa-solid fa-wifi"></i>
            <h6>Fibre - </h6>
            <p>{{item.address_post_code}}</p>
          </div>
          <div class="payment_product">
            <i class="fa-solid fa-laptop"></i>
            <h6>Website - </h6>
            <p>www.website.com</p>
          </div>
        </div>
      </div>
      <Table />
    </div>
  </div>
</template>

<script>

import Table from './Table.vue'
// import Sidenav from "./Sidenav.vue";
import Data from '../assets/Data.json'
export default {
    name: "Billing",
    data(){
      return{
        data: Data
      }
    },
    components: {
      Table
    }
}
</script>

<style >
  .bill{
    width: 100vw - 10vw;
    display: flex;
    background-color: #F7F8FA;
    flex-direction: row;
    left: 9.6vw;
    position: relative;
  }
  .wrapper{
    display: flex;
    flex-direction: column;
  }
  .header{
    background-color: #fff;
    width: 100vw;
    height: 8vh;
    
  }

  .header h1{
    font-size: .8rem;
    display: flex;
    justify-content: flex-start;
    margin-left: 10px;
  }

  .header p{
    font-size: .7rem;
    display: flex;
    margin-left: 10px;
    justify-content: flex-start;
  }

  .accounts_container{
    width: 100vw;
    display: flex;
    border-bottom: 1px solid #F0F0F0;
    margin-left: 20px;
  }


  .accounts_content{
    background-color: #fff;
    height: 70px;
    width: 200px;
    display: flex;
    align-items: center;
    flex-direction: column;
    border-radius: 10px;
    border: 1px solid #F0F0F0;
    margin: 5px;
  }

  .first{
    background-color: #D1EAFF;
    border: 1px solid #1E8CEB;
  }

  .accounts_content h3, h4{
    font-size: .7rem;
  }
  .accounts_content h3{
    color: #1E8CEB;
  }

  .payment_container{
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    width: 100%;
    height: 40vh;
    margin-top: 5px;
    margin-left: 20px;
    border-bottom: 1px solid #F0F0F0;
  }

  .payment_details{
    background: #fff;
    width: 50vw;
    height: 35vh;
    border-radius: 10px;
  }

  .payment_row{
    display:flex;
    flex-direction: row;
    justify-content: space-evenly;
  }
  .payment_title{
    border-bottom: 1px solid #F0F0F0;
    width: 100%;
  }

  .payment_title p{
    font-size: .8rem;
  }

  .payment_box{
    margin: 10px;
    background-color: #F7F8FA;
    border-radius: 10px;
  }

  .invoice{
    font-size: .8rem;
  }

  .payment_info{
    display:flex;
    justify-content: center;
    align-items: center;
    margin: 4px;
  }
  .payment_info p{
    font-size: .8rem;
    text-align: center;
    margin: 5px;
  }

  .payment_button button{
    height: 30px;
    border: none;
    border-radius: 10px;
    background-color: #1E8CEB;
    color: #fff;
    margin-bottom: 10px;
  }

  span{
    border-radius: 10px;
    background-color: #fff;
    color: #17C0A0;
  }

  .payment_products{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 30vw;
    height: 37vh;
    background-color: #fff;
    border-radius: 10px;
    margin-right: 200px;
  }
  .payment_product{
    display: flex;
    justify-content: flex-start;
    flex-direction: row;
    align-items: center;
    margin: 19px;
    width: 100%;
    border-bottom: 1px solid #F0F0F0;
  }

  .payment_product i , .payment_product h6, .payment_product p{
    margin: 20px;
  }
</style>
