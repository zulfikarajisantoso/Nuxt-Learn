<template>
    <div>
        <nav class=" bg-gray-800 h-12 w-auto shadow-lg" >
            <div class=" flex py-2  justify-between">
                <div class="ml-10 md:ml-2">  
                    <p class="text-white cursor-pointer">Logo</p>
                </div>
                <div v-show="!mobile" class="hidden md:flex space-x-5  lg:-ml-96">
                    <a class="text-gray-100 hover:bg-gray-100 hover:text-gray-800 py-1 px-2 rounded-md text-base font-medium" v-for="item in navigation" :key="item" :href="item.href" >{{item.name}}</a>
                </div>
                <div class="flex justify-between space-x-2 mr-3 ">
                    <div class="flex justify-center items-center bg-white h-8 px-2  rounded-md z-0">
                       <input type="text" class=" w-20 md:w-60 pr-3 pl-2  focus:outline-none items-center" placeholder="Search anything...">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-100" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                        </svg>
                    </div>
                    <div class="flex">
                        <nuxt-link to="/keranjang" class="flex items-center space-x-1 mr-2">   <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 text-gray-100 cursor-pointer " fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                        </svg>
                        <span class="bg-green-200  px-1 rounded-xl text-xs ">0</span>
                        </nuxt-link>
                        <nuxt-link to="/profile">  <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 text-gray-100 cursor-pointer " viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-6-3a2 2 0 11-4 0 2 2 0 014 0zm-2 4a5 5 0 00-4.546 2.916A5.986 5.986 0 0010 16a5.986 5.986 0 004.546-2.084A5 5 0 0010 11z" clip-rule="evenodd" />
                        </svg></nuxt-link>
                    </div>
                    
                </div>
             
            </div>
        </nav>
    </div>
</template>


<script>





export default {
    name: "navbar",
    data: () =>{
        return {
            navigation :[
                {name: 'Home', href:'/'},
                {name: 'About', href:'/about'},
                {name: 'Contact US', href:'/contact'},
       
            ]
        }
    }
}

</script>

<style>

</style>