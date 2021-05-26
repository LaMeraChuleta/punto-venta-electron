<template>
    <FilterInventory 
        @open-modal-category="open_modal_category()"
        @open-modal-product="open_modal_product()"
    >
    </FilterInventory>
    <ModalCategory            
        :showModalCategory="showModalCategory" 
        @close-modal-category="close_modal_category()">
    </ModalCategory>
    <ModalProduct 
        :showModalProduct="showModalProduct" 
        @close-modal-product="close_modal_product()">
    </ModalProduct>
    <TableInventory></TableInventory>
</template>

<script>
import FilterInventory from "../components/inventory/FilterInventory";
import ModalCategory from "../components/inventory/ModalCategory";
import ModalProduct from "../components/inventory/ModalProduct";
import TableInventory from '../components/inventory/TableInventory'
export default {    
    components:{
        FilterInventory,
        ModalCategory,
        ModalProduct,
        TableInventory
    },
    data(){
        return {
            showModalCategory: false,
            showModalProduct: false
        }
    }, 
    methods:{
        open_modal_category() { this.showModalCategory = true },
        close_modal_category() { this.showModalCategory = false },
        open_modal_product() { this.showModalProduct = true },
        close_modal_product() { this.showModalProduct = false }
    }
}
</script>

<style>

</style>