<template lang="">
    <div>
        <div class="card">
            <!-- <img src="./img/1capricorn.jpg" alt="Avatar" style="width:100%"> -->
            <img :src="image" alt="name" style="width:100%" />
            <div class="container">
                <h2><b>ราศี :: {{ name }}</b></h2> 
                <h4><b>วันที่ :: {{ time }}</b></h4> 
                <p>ลักษณะนิสัย :: {{ detail }} </p> 
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['id', 'name', 'time', 'detail', 'image']
}
</script>

<style scoped>
.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  /* width: 40%; */
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 22px;
}  

h2 {
  color: black;
}

</style>