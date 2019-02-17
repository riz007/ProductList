<template>
<div class="row">
    <div class="col-12 col-sm-6 col-md-4 col-lg-3" v-for="item in items" :key="item.id">
       <div class="card mt-3">
        <img v-bind:src="item.image_url" alt="Item cover image" class="card-img-top">
        <div class="card-body">
            <p class="card-title"><a href="#" data-toggle="tooltip" data-placement="top" v-bind:title="item.title">{{item.title}}</a></p>
            <p class="card-text">{{item.created_at}}</p>
            <div class="row">
                <div class="col">
                    <p class="">{{item.price | toTHB}}</p>
                </div>
            </div>
        </div>
    </div>
</div>
  
</div>
</template>

<script>
export default {
    name: 'ItemList',
    props: ["items"]
}    
</script>

<style scoped>

.card-title {
    white-space:pre;
    overflow:hidden;
    text-overflow: ellipsis;
}

</style>