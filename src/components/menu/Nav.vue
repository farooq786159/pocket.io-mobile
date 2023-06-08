
<template>
<main class=" top-0 " >
    <!-- <TheWelcome /> -->
    <nav class="  flex  justify-between pb-3 ">
      <div >
        <a  href="/" > <img src="../icons/pocketad.io_logo_final.png" class="  h-28 top-0 w-32"> </a>
      </div>
      <div class="flex  mt-7 rounded-full items-center h-12 py-5    px-3  shadow-2xl shadow-slate-500 cursor-pointer   mr-4" >
        <div>
          <img src="../icons/menu.png" alt="no img" class=" w-8  " @click='toggleModel'>
        </div>
        
      </div>
       <baseModel :modelActive='modelActive'  
        @close-model='toggleModel'       
       >
        <div class='text-white px-6'>
          <div class='border-b border-slate-500  mb-3'>
            <h3 class=' text-5xl  font-bold mt-10  mb-60   '>About</h3>
          </div>
          <div class='mt-10 grid grid-cols-10 '>
            <img src="../new_incons/linkedin-white.png" alt="" class=' col-span-2  w-12 place-items-start  '>
            <img src="../new_incons/behance-white.png" alt="" class=' col-span-2 w-12 '>
            <img src="../new_incons/Instagram-white.png" alt="" class=' col-span-2 w-12 '>
            <img src="../new_incons/facebook-white.png" alt="" class=' col-span-2 w-12 '>
            <img src="../new_incons/twitter-white.png" alt="" class=' col-span-2 w-12 '>
          </div>
          <div class='mt-10 grid grid-cols-7 mb-10 pl-3'>
            <div class=' col-span-4'>
              <p>Term and condition </p>
              <p>Cookies Policy </p>
              <p>Privacy </p>
            </div>
            <div class='col-span-3'>
              <div class=" outline outline-1 rounded-full "> 
                    <p class="  font-bold text-[16px]  py-1 flex justify-center  px-5 ">
                        ENG
                         <img src="../new_incons/icons8-collapse-arrow-50.png"  class=" -mt-5  ml-4 w-3 pb-5 rotate-180  inline-flex " >
                    </p>
              </div>
            </div>
            
          </div>  
        </div>
       
       </baseModel>     
    </nav>
  </main>  
</template>

<script setup>
import baseModel from "./baseModel.vue";
   import {ref} from "vue"
   const modelActive=ref(null);
    const toggleModel=()=>{
        modelActive.value=!modelActive.value
    }

</script>