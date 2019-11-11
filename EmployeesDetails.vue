<template>
    <div>
      
  <div  v-if="!isDetail">  
           <b-table @row-clicked="detailpage" hover :items="users"  :fields="myfields"> </b-table> 
    
  </div>  
      <div class="detailpage" v-if="isDetail"> 
       <b-button @click="backbtn">Back</b-button>
       <h1>user full details</h1>
       <p>{{currentuser.name}}</p>
        </div>

    </div>
</template>
<script>

import axios from 'axios'
export default {
    
     data() {
         
      return{
            myfields: ['name', 'username', 'email'],  
            currentuser:{},
            isDetail:false,
           
 users: [ ],
 
           }
   
  },
  mounted() {
   
     axios.get('https://jsonplaceholder.typicode.com/users')
     .then(response => {this.users = response.data})
  },
     
methods:{

detailpage(items){
this.isDetail=true;
this.currentuser=items;

},
backbtn(){
  this.isDetail=false;
}
}

  
}
</script>      
