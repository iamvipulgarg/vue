<template>
    <form action="">
        <div v-for="(item, index) in feilds"> 
            <div v-for="(label, type) in item"> 
                <label :for="type">{{ label }}</label>
                <input :type="type" :name="label">
            </div>
        </div>
    </form>
</template>
<script>
export default{
    data(){
        return {
            feilds:[
                {"text" : "User Name"}, 
                {"text" : "Father Name"}, 
                {"password" : "Password", },
                {"number" : "Age"},
                {"text" : "Contact"}, 
            ],
            user:''
        }
    }
}
</script>