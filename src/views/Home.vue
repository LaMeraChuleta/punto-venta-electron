<template>
    <FilterInventory 
        @open-modal-category="open_modal_category()"
        @open-modal-product="open_modal_product()"
        @open-modal-inventory="open_modal_inventory()">
    </FilterInventory>
    <ModalCategory            
        :showModalCategory="showModalCategory" 
        @close-modal-category="close_modal_category()">
    </ModalCategory>
    <ModalProduct 
        :showModalProduct="showModalProduct" 
        @close-modal-product="close_modal_product()">
    </ModalProduct>
    <ModalInventory
        :showModalInventory="showModalInventory" 
        @close-modal-inventory="close_modal_inventory()">
    </ModalInventory>
    <TableInventory></TableInventory>
</template>

<script>
import FilterInventory from "../components/inventory/FilterInventory";
import ModalCategory from "../components/inventory/ModalCategory";
import ModalProduct from "../components/inventory/ModalProduct";
import ModalInventory from "../components/inventory/ModalInventory";
import TableInventory from '../components/inventory/TableInventory'
export default {    
    components:{
        FilterInventory,
        ModalCategory,
        ModalProduct,
        TableInventory,
        ModalInventory
    },
    data(){
        return {
            showModalCategory: false,
            showModalProduct: false,
            showModalInventory: false,            
        }
    }, 
    methods:{
        open_modal_category() { this.showModalCategory = true },
        close_modal_category() { this.showModalCategory = false },
        open_modal_product() { this.showModalProduct = true },
        close_modal_product() { this.showModalProduct = false },
        open_modal_inventory() {this.showModalInventory = true},
        close_modal_inventory() { this.showModalInventory = false },
    }
}
</script>

<style>

</style>