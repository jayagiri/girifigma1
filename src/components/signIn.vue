<template>
  <header class="">
    <div class="bg-black h-screen w-full px-8 py-6">
      <div class="h-32"></div>
      <h1 class="text-white font-bold text-5xl">Sign In</h1>
      <div class=" py-10">
        <form>
          <div class="text-white border-2 w-40 hover:border-blue-700  p-1 bg-[#141414]">
            <input type="text" placeholder="Username" required />
          </div>
          <div class="text-white border-2 w-40  hover:border-blue-700  p-1 bg-[#141414]">
            <input type="text" placeholder="Password" required />
          </div>
          <div class="text-white">
            <input type="checkbox" class="accent-[#22c55e] underline hover:underline-offset-4" checked="checked"     /> Remember Me
          </div>
          <div class="text-white">
            <button type="submit" class="hover:border-blue-700">Sign In</button>
            <a href="#"> Forgot Password? </a>
          </div>

          <div>
            <h4>Sign In With Services</h4>
          </div>

          <div class="text-white">
            <button type="submit">Google</button>
            <button type="submit">Facebook</button>
          </div>
        </form>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "signIn",
};
</script>
