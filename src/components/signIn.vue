<template>
  <HEAD>
    <link
      href="https://fonts.googleapis.com/css?family=Roboto"
      rel="stylesheet"
      type="text/css"
    />
  </HEAD>
  <header>
    <div class="bg-black h-screen w-full px-24 py-6">
      <div class="h-32 hover:border-blue-700"></div>
      <h1 class="text-white font-bold text-7xl font-sans">Sign In</h1>
      <div class="py-10">
        <form>
          <div
            class="
              text-white
              border-2 border-[#141414]
              w-80
              hover:border-blue-700
              border-solid-blue
              p-1
              my-2
            "
          >
            <input class="bg-black w-36" type="text" v-model="state.userName" placeholder="Username" />
          </div>
          <div class="">
            <div
              class="
                text-white
                border-2 border-[#141414]
                w-80
                hover:border-blue-700
                p-1
                my-2
              "
            >
              <input
                class="bg-black flex-auto b-1 w-36"  v-model="state.password"
                placeholder="Password"
                :type="show ? 'password' : 'text'"
              />
            </div>
            <div>
              <svg
                class="h-1 flex-auto text-green-700"
                fill="none"
                @click="show = !show"
                :class="{ hidden: !show, block: show }"
                xmlns="http://www.w3.org/2000/svg"
                viewbox="0 0 576 512"
              >
                <path
                  fill="currentColor"
                  d="M572.52 241.4C518.29 135.59 410.93 64 288 64S57.68 135.64 3.48 241.41a32.35 32.35 0 0 0 0 29.19C57.71 376.41 165.07 448 288 448s230.32-71.64 284.52-177.41a32.35 32.35 0 0 0 0-29.19zM288 400a144 144 0 1 1 144-144 143.93 143.93 0 0 1-144 144zm0-240a95.31 95.31 0 0 0-25.31 3.79 47.85 47.85 0 0 1-66.9 66.9A95.78 95.78 0 1 0 288 160z"
                ></path>
              </svg>

              <svg
                class="h-1 text-green-700"
                fill="none"
                @click="show = !show"
                :class="{ block: !show, hidden: show }"
                xmlns="http://www.w3.org/2000/svg"
                viewbox="0 0 640 512"
              >
                <path
                  fill="currentColor"
                  d="M320 400c-75.85 0-137.25-58.71-142.9-133.11L72.2 185.82c-13.79 17.3-26.48 35.59-36.72 55.59a32.35 32.35 0 0 0 0 29.19C89.71 376.41 197.07 448 320 448c26.91 0 52.87-4 77.89-10.46L346 397.39a144.13 144.13 0 0 1-26 2.61zm313.82 58.1l-110.55-85.44a331.25 331.25 0 0 0 81.25-102.07 32.35 32.35 0 0 0 0-29.19C550.29 135.59 442.93 64 320 64a308.15 308.15 0 0 0-147.32 37.7L45.46 3.37A16 16 0 0 0 23 6.18L3.37 31.45A16 16 0 0 0 6.18 53.9l588.36 454.73a16 16 0 0 0 22.46-2.81l19.64-25.27a16 16 0 0 0-2.82-22.45zm-183.72-142l-39.3-30.38A94.75 94.75 0 0 0 416 256a94.76 94.76 0 0 0-121.31-92.21A47.65 47.65 0 0 1 304 192a46.64 46.64 0 0 1-1.54 10l-73.61-56.89A142.31 142.31 0 0 1 320 112a143.92 143.92 0 0 1 144 144c0 21.63-5.29 41.79-13.9 60.11z"
                ></path>
              </svg>
            </div>
          </div>
          <div class="text-white">
            <input
              type="checkbox"
              class="accent-[#22c55e] underline hover:underline-offset-4 my-6"
              checked="checked"
            />
            Remember Me
          </div>
          <div class="flex">
            <div class="text-black text-sm">
              <button
                @click.prevent="authenticate()"
                class="
                  hover:border-blue-700
                  bg-green-600
                  font-bold
                  py-2
                  px-4
                  rounded
                "
              >
                Sign In
              </button>
            </div>
            <div class="">
              <a href="#" class="px-20 text-green-600 underline text-sm">
                Forgot Password?
              </a>
            </div>
          </div>

          <div class="text-white my-6 mx-20 text-sm">
            <h4>Sign In With Services</h4>
          </div>

          <div class="text-white">
            <!--<googleLogo class="w-5 h-5"/> -->
            <button type="submit" class="px-10 border-2 rounded-l my-2">
              Google
            </button>
            <button type="submit" class="px-10 border-2 rounded-l mx-8">
              Facebook
            </button>
          </div>
          <div class="m-2"></div>
          <div
            class="
              text-white
              border-2 border-[#141414]
              w-80
              hover:border-blue-700
              border-solid-blue
              p-2
              text-sm
            "
          >
            <p class="text-white text-sm">
              Don't have an account yet?
              <a class="text-green-400 underline pl-3 text-sm" href="#"
                >Become a member</a
              >
            </p>
          </div>
        </form>
      </div>
    </div>
  </header>
</template>

<script setup>
import { reactive } from "vue";
const state = reactive({
  userName: "",
  password: "",
  userNameError: false,
  passwordError: false,
});

function authenticate() {
  if (state.userName === "") {
    state.userNameError = true;
    return;
  }
  if (state.password === "") {
    state.passwordError = true;
    return; 
  }
  console.log(state.userName, state.password);
  //route  to home page
}
</script>
