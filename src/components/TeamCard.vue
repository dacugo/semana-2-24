<template>
    <div class="d-flex">
      <div class="card border-dark text-dark">
        <div class="d-flex justify-content-center p-2">
          <img class="img-fluid" v-bind:src="member.imagen" alt="Imagen integrante equipo" />
        </div>
        <div class="card-body">
          <h5 class="card-title">{{member.nombre}}</h5>
          <p class="card-text">
            {{member.descripcion}}
          </p>
          <p class="card-text"><span>Codigo: </span>
            {{member.codigo}}
          </p>
        </div>
        <div class="card-footer">
          <small class="text-muted"><span>Rol: </span>{{member.rol}}</small>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
