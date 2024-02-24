<script>
export default {
  data() {
    return {
      // 在 data 方法中定义组件的数据
      // 这里定义了一个用于控制移动菜单的变量
      isMobileMenuOpen: false
    }
  },
  methods: {
    // toggleMobileMenu 方法用于打开/关闭移动菜单
    toggleMobileMenu() {
  this.isMobileMenuOpen = !this.isMobileMenuOpen;
}
  }
}
</script>

<template>
  <main>
    <div class="w-screen h-screen bg-gray-600 flex flex-col md:flex-row">
      <div class="nav md:w-1/5 md:h-full bg-green-500 w-full h-20 flex md:flex-col items-center text-center leading-8 justify-between md:justify-start relative">
        <div class="logo bg-purple-700 w-16 h-16 md:mt-32 ml-2 md:ml-0 rounded-full"></div>
        
        <div class="absolute inset-y-0 right-2  flex items-center sm:hidden">
       
        <button type="button"  class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-800 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white" @click="toggleMobileMenu" aria-controls="mobile-menu" aria-expanded="false">
          <span class="absolute -inset-0.5"></span> 
          <span class="sr-only">Open main menu</span>
       
          <svg class="block h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
          </svg>
         
          <svg class="hidden h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
      
      <div :class="{ 'block': isMobileMenuOpen, 'hidden': !isMobileMenuOpen }" class="sm:hidden mt-52 bg-gray-700" id="mobile-menu">
  <div class="space-y-1 px-2 pb-3 pt-2">
  
    <a href="www.youtube.com" class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium">Youtube</a>
    <a href="www.google.com" class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium">Google</a>
    <a href="https://tw.yahoo.com/" class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium">Yahoo</a>
  </div>
</div>
        
        
        
        
        
        
        
        
      
        <div class="all-a sm:flex md:flex-col hidden">
        <div class="a bg-yellow-700 w-16 h-8 md:mt-8 "><a href="www.youtube.com">Youtube</a></div>
        <div class="a bg-yellow-700 w-16 h-8 md:mt-8"><a href="www.google.com">Google</a></div>
        <div class="a bg-yellow-700 w-16 h-8 md:mt-8 mr-2 md:mr-0"><a href="https://tw.yahoo.com/">Yahoo</a></div>
      </div>
      </div>

      <div class="md:w-4/5 md:h-full bg-red-700 flex flex-wrap justify-center items-center h-full w-full">
      <div class="w-4/5 h-4/5  flex flex-wrap xl:flex-nowrap sm:gap-2">
          <div class="my-img bg-gray-400 xl:w-1/3 xl:h-full sm:w-full sm:h-1/2 h-1/3 w-full"></div>
          <div class="my-img bg-teal-500 xl:w-1/3 xl:h-full sm:h-1/2 sm:w-1/2 sm:flex-1 h-1/3 w-full"></div>
          <div class="my-img bg-indigo-600 xl:w-1/3 xl:h-full sm:h-1/2 sm:w-1/2 sm:flex-1 h-1/3 w-full"></div>
        </div>
      </div>
  </div>
  </main>
</template>
