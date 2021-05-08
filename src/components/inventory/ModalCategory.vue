<template>    
    <div v-if="showModalCategory" class="flex flex-col w-11/12 sm:w-5/6 lg:w-1/2 max-w-2xl mx-auto rounded-lg border border-gray-300">
      <div class="flex flex-row justify-between p-6 bg-white border-b border-gray-200 rounded-tl-lg rounded-tr-lg">
        <p class="font-semibold text-gray-800">Nueva Categoria</p>
        <button @click="close_modal_diagnostic()">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
          </svg>
        </button>
      </div>
      <div class="flex flex-col px-6 py-5 bg-gray-50">
        <p class="mb-2 font-semibold text-gray-700">Marca</p>
        <input type="text" name="" class="w-full p-5 mb-5 bg-white border border-gray-200 rounded shadow-sm appearance-none" id="">                  
        <p class="mb-2 font-semibold text-gray-700">Descripcion</p>
        <textarea type="text" name="" class="p-5 mb-5 bg-white border border-gray-200 rounded shadow-sm h-36" id=""></textarea>                                 
        <hr />
        <div class="flex items-center mt-5 mb-3 space-x-4">
          <label class="inline-flex font-semibold text-gray-500">Numero Total de Productos: 10</label>            
          <br />
        </div>       
      </div>
      <div class="flex flex-row items-center p-5 bg-white border-t border-gray-200 rounded-bl-lg rounded-br-lg justify-end">          
        <button class="px-4 py-2 text-white font-semibold bg-blue-500 rounded">Guardar</button>
      </div>
    </div>    
</template>

<script>
export default {
    props:{
        showModalCategory:{
            type: Boolean,
            default: () => false
        }
    },        
    methods:{
        close_modal_diagnostic() { this.$emit('close-modal-category') }
    }
};
</script>

<style></style>
