<template>
    <form action="">
        <label for="">User Name</label>
        <input type="text" v-model="user">
        <br>

        <label for="">Password</label>
        <input type="text" v-model="pass">
        <br>
        
        <label for="">Contact</label>
        <input type="text" v-model="contact">
        <br>
        
        <label for="">Age</label>
        <input type="text" v-model="age">
        <br>
        
        <label for="">Address</label>
        <input type="text" v-model="adddress">
        <br>     
        <div v-if="message">All fields are required!</div>
        <input type="submit" @click="isSubmitted">
        
</form>
</template>
<script>
export default{
    datea(){
        return{
            user:'',
            pass:'',
            contact:'',
            age:'',
            adddress:'',
            feilds:["user","pass","contact","age","adddress"],
            count:0,
            message:false
        }
    },
    computed:{
        isSubmitted(){
         for (let i = 0; i < feilds.length; i++) {
            if(this.feilds[i]===""){
                 this.count++;   
            }
         }   
         if(this.count!=0){
            this.message=true;
         }
         else{
            console.log(this.user);
            console.log(this.pass);
            console.log(this.contact);
            console.log(this.age);
            console.log(this.adddress);
         }
        }
    }
}
</script>