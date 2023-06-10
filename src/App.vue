<template>
  <nav class="navbar navbar-expand-sm bg-dark navbar-dark">
  <a class="navbar-brand" href="#">Tutorial Sharing</a>
  
</nav>

<div class="container-fluid py-4">
  <div class="row justify-content-center">
        <div class="col-md-7">
          <div class="row">
            <div class="col-sm-2 p-1 mb-1" v-for="val in item" :key="val.id">
              <a href="#" class="text-decoration-none">
                <div class="card">
                <div class="card-body text-center p-1">
                  <img :src="require(`@/assets/${val.img}`)" width="50" height="50">
                  <p class="text-muted mt-2">{{ val.title }}</p>
                </div>
              </div>
              </a>
            </div>
          </div>
        </div>
    </div>
</div>
</template>

<script>
import itemdata from './json/item.json';
export default {
  name: 'App',
  data(){
    return{
      item : itemdata
    }
  }
}
</script>