<template>
    <div class="container">
        Items 1-12 of {{items.length}}
         <hr />
        <ItemList :items="items"></ItemList>
        <div class="row">
            <div class="col-12">
                <Pagination />
            </div>
        </div>
        <hr />
    </div>
</template>

<script>

import ItemList from "./ItemList"
import Pagination from "./Pagination"
import axios from "axios"
import Vue from "vue"

Vue.filter('toTHB', function (value) {
    return `฿${value}`;
});

export default {
    components: {
        ItemList,
        Pagination
    },
    data() {
        return {
            items: [],
            errors: []
        }
    },
    created() {
        axios.get('list.json')
            .then(response => {
                // JSON responses are automatically parsed.
                this.items = response.data;
            })
            .catch(e => {
                this.errors.push(e);
                // console.log('error');
            })
    }
}
</script>