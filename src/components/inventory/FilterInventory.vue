<template>
  <div class="mx-auto px-2 sm:px-6 lg:px-8">
      <div class="p-10">
        <!-- primera header -->
        <div class="justify-between inline-flex w-full">
          <div>
              <p class="text-2xl">Lista Inventario</p>
          </div>
          <div class="flex space-x-5">  
              <button @click="this.$emit('open-modal-inventory')">Añadir Inventario</button>
              <button @click="this.$emit('open-modal-category')">Añadir Categoria</button>
              <button @click="this.$emit('open-modal-product')">Añadir Producto</button>
              <button>Reporte</button>
          </div>
        </div>
        <!-- primera header -->
        <div class="flex justify-between mt-10">
            <input class="w-64" type="text" placeholder="Buscar">
            <input class="w-64" type="text" placeholder="Categoria">
            <input class="w-64" type="text" placeholder="Codigo de Barras">
            <button class="w-64">Filtrar</button>
        </div>
      </div>
  </div>
</template>

<script>
export default {    
    
}
</script>

<style>

</style>