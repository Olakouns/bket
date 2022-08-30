<template>
  <div>
    <div class="flex h-screen">
      <div class="w-7/12 login-left-pane">
        <div class="relative h-full">
          <div class="flex h-5/6 justify-center items-center">
            <img class="w-8/12 mb-8" src="../assets/images/Bket_logo.svg" />
          </div>
          <div class="absolute bottom-px mb-1.5 text-center w-full text-white">
            <label>@ Powered by Bio Market</label>
          </div>
        </div>
      </div>
      <div class="w-5/12 relative">
        <div class="flex flex-col items-center justify-center h-full">
          <h3 class="text-3xl font-bold mb-2">Connexion</h3>
          <h4 class="black-49 mb-12 font-semibold">
            Premiere connexion ? S’inscrire
          </h4>
          <form class="block w-3/5">
            <div class="flex flex-col mb-3">
              <label class="black-67 mb-3 font-bold">Username</label>
              <input
                class="border w-full p-3 rounded-12 form-simple-input"
                type="text"
                placeholder="marius@gmail.com"
              />
            </div>
            <div class="flex flex-col mb-8">
              <label class="black-67 mb-3 font-bold">Password</label>
              <input
                class="border w-full p-3 rounded-12 form-simple-input"
                type="password"
                placeholder="**************"
              />
            </div>
            <div class="flex justify-center w-full mb-8">
              <button class="btn-login">Se connecter</button>
            </div>

            <div class="flex justify-center mb-8">
              <div class="flex w-8/12 items-center justify-between">
                <hr class="w-5/12 login-line" />
                <div class="w-2/12 login-rounder"></div>
                <hr class="w-5/12 login-line" />
              </div>
            </div>

            <div class="flex justify-center">
              <a href="#" class="login-forget-link black-49"
                >Mot de passe oublie ?</a
              >
            </div>
          </form>
        </div>
        <div class="absolute bottom-4 right-4">
          <img class="w-20" src="../assets/images/Bket_logo_g.png" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginView",
};
</script>

<style scoped lang="scss">
@import "src/assets/styles/colors.scss";

.login-left-pane {
  background-color: $bket-green-color;
}
.login {
  &-tilte {
    font-size: 24px;
    font-weight: bold;
  }
  &-line {
    background-color: rgba(217, 217, 217, 1);
  }
  &-rounder {
    width: 1.5rem;
    height: 1.5rem;
    border-radius: 50%;
    background-color: rgba(217, 217, 217, 1);
  }
  &-forget-link {
    text-decoration: underline;
    font-weight: 700;
    font-size: 12px;
    line-height: 15px;
  }
}

.btn-login {
  background-color: $bket-green-color;
  border-radius: 12px;
  padding: 12px;
  color: $bket-white-color;
  width: 40%;
  font-weight: 600;
  transition: font-weight, background-color, 0.2s;

  &:hover {
    color: white;
    font-weight: bold;
    background-color: rgba(0, 169, 54, 0.91);
  }
}
</style>
