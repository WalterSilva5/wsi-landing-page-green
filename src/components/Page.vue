<template>
  <div class="container-fluid mb-5">
    <div class="mt-lg-12 d-flex justify-content-center row">
      <div class="col-lg-10 d-flex justify-content-center row mt-3">
        <a href="https://waltersilva5.github.io/">
          <h1 class="header">@WALTERSILVA5</h1></a
        >
      </div>
      <div class="col-lg-11">
        <div
          class="
            page-body
            mt-1
            col-lg-12
            justify-content-center
            row
            d-flex
            container-fluid
          "
        >
          <div class="col-lg-6 page-card mx-md-4">
            <div>
              <h4>Exemplo de titulo para landing page.</h4>
            </div>

            <div class="card-border mt-3">
              <h5 class="px-2">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Deserunt aliquam neque quibusdam soluta voluptas nulla
                voluptatum aperiam maxime veritatis ipsa quos maiores omnis iure
                a est dolorum itaque, ad dolorem.
              </h5>
            </div>
            <div class="card-border mt-3">
              <h6 class="px-2">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Deserunt aliquam neque quibusdam soluta voluptas nulla
                voluptatum aperiam maxime veritatis ipsa quos maiores omnis iure
                a est dolorum itaque, ad dolorem. Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Vel blanditiis id cupiditate
                consectetur et, adipisci enim asperiores nisi voluptatem
                repellat molestiae sint ex labore iste omnis quae obcaecati
                placeat ratione?
              </h6>
            </div>
            <div class="card-border mt-3">
              <h6 class="px-2">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                Deserunt aliquam neque quibusdam soluta voluptas nulla
                voluptatum aperiam maxime veritatis ipsa quos maiores omnis iure
                a est dolorum itaque, ad dolorem.
              </h6>
            </div>
          </div>
          <div class="col-lg-5 page-card">
            <div>
              <h3><b>EXEMPLO CADASTRO</b></h3>
            </div>
            <form autocomplete="off">
              <div class="card-border p-3 mt-5">
                <div class="form-group">
                  <label for="nome">nome</label>
                  <input autocomplete="off"
                    type="text"
                    class="form-control"
                    name="nome"
                    v-model="campos"
                  />
                </div>
                <div class="form-group">
                  <label for="email">email</label>
                  <input autocomplete="off"
                    type="text"
                    class="form-control"
                    name="email"
                    v-model="campos"
                  />
                </div>
                <div class="form-group">
                  <label for="telefone">telefone</label>
                  <input autocomplete="off"
                    type="text"
                    class="form-control"
                    name="telefone"
                    v-model="campos"
                  />
                </div>
              </div>
              <div class="d-flex justify-content-end mt-2">
                <button class="card-border btn">CADASTRAR</button>
              </div>
            </form>
            <div
              class="alert alert-danger mt-3"
              role="alert"
              v-show="camposativos"
            >
              <b>ESSE FORMULARIO É APENAS DE EXEMPLO!</b>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row"></div>
  </div>
  <page-footer />
</template>

<script>
import PageFooter from "./PageFooter.vue";
export default {
  components: { PageFooter },
  data() {
    return {
      campos: "",
      camposativos: false,
    };
  },
  watch: {
    campos(newValue) {
      if (newValue != "") {
        this.camposativos = true;
      } else {
        this.camposativos = false;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
$text-color: rgb(0, 20, 0);
.header {
  border-bottom: 4px solid $text-color;
}

.form-group {
  margin-top: 10px;
  input {
    border: 1px solid rgba(3, 255, 242, 0.26);
    background-color: rgba(124, 255, 248, 0.534);
  }
}

@mixin card-border {
  text-align: left;
  border-radius: 4px;
  background: rgba($text-color, 0.1);
  box-shadow: 1px 1px 4px;
  padding-top: 10px;
  transition: 1s;
  &:hover {
    box-shadow: 2px 2px 5px;
    transition: 1s;
  }
}

.card-border {
  @include card-border;
}

.btn{
  color:rgba(124, 255, 248, 0.658);
  font-weight:bold;
  background-color: rgba(0, 77, 73, 0.534);
  height: 40px;
  border: 2px solid rgba(0, 68, 0, 0.418);
  box-shadow: 2px 3px 4px black;
}

.page-card {
  @include card-border;
  text-align: center;
  min-height: 450px;
}

header,
a {
  color: $text-color;
  text-decoration: none;
  transition: 0.3s;
  &:hover {
    font-size: 110%;
    transition: 0.3s;
    color: rgba($text-color, 0.8);
  }
}
</style>
