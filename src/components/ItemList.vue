<template>
<div class="row">
    <div class="col-12 col-sm-6 col-md-4 col-lg-3" v-for="item in items" :key="item.id">
       <div class="card mt-3">
            <img v-bind:src="item.image_url" alt="Item cover image" class="card-img-top">
            <div class="card-body">
                <p class="card-title"><a href="#" data-toggle="tooltip" data-placement="top" v-bind:title="item.title">{{item.title}}</a></p>
                <p class="card-text-timestamp">{{  format_date(item) }}</p>
                <!-- <star-rating v-bind:rating="item.vote" :config="config"></star-rating> -->
                <div class="is-pulled-left">
                    <p v-if="item.vote === 0" class="no-fa-star">Not rated yet</p>
                    <i v-if="item.vote === 1" class="fa fa-star"></i>
                    <i v-if="item.vote === 2" class="fa fa-star"></i>
                    <i v-if="item.vote === 2" class="fa fa-star"></i>
                    <i v-if="item.vote === 3" class="fa fa-star"></i>
                    <i v-if="item.vote === 3" class="fa fa-star"></i>
                    <i v-if="item.vote === 3" class="fa fa-star"></i>
                    <i v-if="item.vote === 4" class="fa fa-star"></i>
                    <i v-if="item.vote === 4" class="fa fa-star"></i>
                    <i v-if="item.vote === 4" class="fa fa-star"></i>
                    <i v-if="item.vote === 4" class="fa fa-star"></i>
                    <i v-if="item.vote === 5" class="fa fa-star"></i>
                    <i v-if="item.vote === 5" class="fa fa-star"></i>
                    <i v-if="item.vote === 5" class="fa fa-star"></i>
                    <i v-if="item.vote === 5" class="fa fa-star"></i>
                    <i v-if="item.vote === 5" class="fa fa-star"></i>
                </div>
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

import moment from 'moment'

export default {
    methods: {
        format_date(item){
            let CreatedDate = moment(item.created_at);
            return moment(CreatedDate).startOf('day').fromNow(); 
        }
    },
    name: 'ItemList',
    props: ["items"]
}    
</script>

<style scoped>

.card {
    border: none;
}

.card:hover {
    box-shadow: 0 0 11px rgba(33,33,33,.2); 
    -webkit-box-shadow: 0 0 11px rgba(33,33,33,.2); 
    -moz-box-shadow: 0 0 11px rgba(33,33,33,.2); 
    cursor: pointer;
}

.card-title {
    white-space:pre;
    overflow:hidden;
    text-overflow: ellipsis;
}

.card-text-timestamp {
    font-size: 14px;
}

.fa-star{
  color: #e92e1f;
  margin-right: 5px;
  margin-bottom: 15px;
}

.no-fa-star {
  color: #e92e1f;
  margin-bottom: 12px;
}

</style>