<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                newItem:""
            }
            
        },
        methods:{
            addItem(){
                this.items.push(this.newItem);

            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for="(item,idx) in items">
            {{ item }}
            <button @click="items.splice(idx,1)">Delete!</button>
            <!-- delete items from the list -->
        </li>
        
    </ul>

    <p><input type="text" v-model="newItem"></input><button @click="addItem">Add!</button></p>
   
</template>
