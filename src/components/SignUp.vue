<template>
    <img src="/images/Site logo.png"/>
    <h1>Sign up</h1>
    <div class="form_box">
        <input type="text" v-model="fname" placeholder="First name " />
        <input type="text" v-model="lname" placeholder="Last name "/>
        <input type="email" v-model="email" placeholder="@email "/>
        <button v-on:click="SignUp">Sign up</button>
    </div>
</template>
<script>
export default {
    name:'SignUp',
    methods:{
        SignUp(){  
            const data = [
                {
                    first_name:  this.fname,
                    last_name: this.lname,
                    Email :this.email,
                }
            ]
            localStorage.setItem('user-data',JSON.stringify(data))
            console.log(`First name :  ${this.fname} Last name : ${this.fname} Email : ${this.email}`)
        }
    },
    mounted(){
        const val  = localStorage.getItem('user-data')
        console.log('working ',JSON.parse(val))
    }
}
</script>
<style>
*{
    background-color: rgb(0, 0, 0);
    box-sizing: border-box;
    color:#fff;
    border-color: #fff;
}
.form_box{
    max-width: 600px;
    margin:auto;
    width:100%;
    border: 2px solid rgb(255, 255, 255);
    padding:30px;
    margin-top: 30px;
}
.form_box input{
    width: -webkit-fill-available;
    padding:10px;
    margin:10px;
}
</style>