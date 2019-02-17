<template>
    <nav class="mt-3" aria-label="...">
        <ul class="pagination">
            <!-- <li class="page-item disabled">
                <a class="page-link" href="#" tabindex="-1">&#8249;</a>
            </li> -->
            <li class="page-item active"><a class="page-link" href="#">1</a></li>
            <li class="page-item">
                <a class="page-link" href="#">2 <span class="sr-only">(current)</span></a>
            </li>
            <li class="page-item">
                <a class="page-link" href="#"><i class="fa fa-angle-right"></i></a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'Pagination'
}    
</script>

<style>
.pagination {
   justify-content: center;
}
.page-item.active .page-link {
    border-color: #dd534c;
    background-color: #dd534c;

}
.page-link {
    border: none;
    color: #000000;
    background-color: #fae1e2;
    margin-right: 5px;
}
.page-item:first-child .page-link {
    border-top-left-radius: 0;
    border-bottom-left-radius: 0;
}

.page-item:last-child .page-link {
    border-top-right-radius: 0;
    border-bottom-right-radius: 0;
    background-color: #d0d0d0;
}

.fa-angle-right{
    color: #ffffff;
}
</style>