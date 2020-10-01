<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand href="#" style="font-family: 'Bangers', cursive;">PLAYROOM</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#">Incio</b-nav-item>
          <b-nav-item href="#">Productos</b-nav-item>
          <b-nav-item href="#">Contacto</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Buscar"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit">Buscar</b-button>
          </b-nav-form>

          <b-nav-item-dropdown text="Lenguaje" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template v-slot:button-content>
              <em>Ingresar</em>
            </template>
            <b-dropdown-item href="#">Iniciar Sesión</b-dropdown-item>
            <b-dropdown-item href="#">Salir</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  }
}
</script>
