<template>
    <form action="">
        <div v-for="(item, index) in feilds" :key="item.name" class="mb-3"> 
                <label v-if="item.label_display" :for="item.name">{{ item.name.charAt(0).toUpperCase() + item.name.slice(1) }}</label>
                <input :type="item.type" :name="item.name" :id="item.name" :class="item.class" :value="item.value" :placeholder="item.placeholder">
        </div>
    </form>
</template>
<script>
export default{
    data(){
        return {
            feilds:[
                {type : "text" , name : "name", class : "form-control", placeholder : "Enter Name", value : '', label_display : true }, 
                {type : "email" , name : "email", class : "form-control", placeholder : "Enter Email", value : '', label_display : true },
                {type : "password" , name : "password", class : "form-control", placeholder : "Enter Password", value : '', label_display : true },
                {type : "number" , name : "age", class : "form-control", placeholder : "Enter Age", value : '', label_display : true },
                {type : "tel" , name : "phone", class : "form-control", placeholder : "Enter Phone", value : '', label_display : true },
                {type : "submit" , name : "submit", class : "form-control", placeholder : "Submit", value : 'Submit', label_display : false },
            ],
            user:''
        }
    }
}
</script>
<style scoped>
    .mb-3{margin-bottom: 1rem}
    .form-control{margin: 0.25rem;}
</style>