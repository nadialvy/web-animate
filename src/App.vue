<template>
  <div id="animate-on-load" class="text-center mt-20">
    <h1 class="text-4xl font-bold mb-4">Selamat datang!</h1>
    <p class="text-lg">Tekan tombol di bawah ini untuk memulai.</p>
    <button
      class="mt-4 px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600 transition-colors duration-300"
    >
      Mulai
    </button>
  </div>

  <p class="text-center my-4">ini contoh yang salah kidss</p>
  <div
    class="w-40 h-40 bg-slate-700 mx-auto rounded-lg shadow-md hover:scale-50 hover:rotate-180 origin-top-left hover:bg-slate-400 transition-all"
  ></div>

  <p class="text-center my-4">ini contoh yang btul rill no fek</p>
  <div class="w-40 h-40 bg-blue-300 group mx-auto">
    <div
      class="w-40 h-40 bg-slate-700 mx-auto rounded-lg shadow-md hover:scale-50 group-hover:rotate-180 origin-top-left hover:bg-slate-400 transition-all"
    ></div>
  </div>

  <p class="text-center my-8">ini yang kepikiran aj ccc hyunk</p>
  <div class="relative w-40 h-40 mx-auto overflow-hidden border-violet-600">
    <div class="w-40 h-40 bg-blue-300 group mx-auto rounded-lg">
      <div class="w-40 h-40">
        <div
          class="z-1000 w-40 h-40 bg-slate-700 mx-auto rounded-lg shadow-md group-hover:translate-x-full transition-all"
        >
          <p class="text-white text-center mt-16 absolute left-0 right-0">
            Coba hover
          </p>
        </div>
      </div>
    </div>
  </div>

  <div class="w-40 h-40 bg-blue-300 group mx-auto rounded-lg my-10">
    <div
      class="w-40 h-40 bg-slate-700 mx-auto rounded-lg shadow-md group-hover:translate-x-full transition-all"
    ></div>
  </div>

  <div class="group w-40 h-40 mx-auto mb-10">
    <div class="w-40 h-40 bg-blue-300 mx-auto rounded-lg">
      <p class="text-center text-xl">Baaaa!!</p>
    </div>
    <div
      class="relative -top-40 w-40 h-40 bg-slate-700 mx-auto rounded-lg group-hover:translate-x-full transition-all"
    >
      <p class="text-center text-xl text-white">Ciluk</p>
    </div>
  </div>

  <div class="overflow-hidden group w-40 h-40 mx-auto mb-10 rounded-lg">
    <div class="w-40 h-40 bg-blue-300 mx-auto rounded-lg">
      <p class="text-center text-xl">Baaaa!!</p>
    </div>
    <div
      class="relative -top-40 w-40 h-40 bg-slate-700 mx-auto rounded-lg group-hover:translate-x-full transition-all ease-in duration-200"
    >
      <p class="text-center text-xl text-white">Ciluk</p>
    </div>
  </div>

  <p class="text-center">------------------------------</p>

  <div class="flex items-center justify-center">
    <div class="bg-slate-800 w-40 h-40 rounded-full my-20 flex justify-center items-center group hover:bg-yellow-200 hover:shadow-lg hover:shadow-yellow-100 transition-all" @mouseover="changeImage" @mouseleave="resetImage">
      <div class="bg-dark-red w-36 h-36 rounded-full flex items-center justify-center">
        <div class="bg-slate-800 w-32 h-32 rounded-full group-hover:bg-yellow-200 group-hover:shadow-lg hover:shadow-yellow-100 flex items-center justify-center transition-all">
          <img :src="imageSrc" alt="Gambar" class="w-1/2 items-center justify-center">
        </div>
      </div>
    </div>
  </div>

  <p class="text-center mb-10">------------------------------</p>

    <div class="group border border-violet-700">
      <img src="../public/sample.jpg" alt="Your Image" class="w-1/2 h-auto items-center justify-center">
      <div class="relative -top-16 left-0 right-0 bottom-0 bg-black opacity-90 w-1/2 h-16 items-center justify-center group-hover:opacity-0 transition-opacity duration-500">
        <p class="text-white text-center pt-4 text-xl font-semibold">Lorem Ipsum Anjasss</p>
      </div>
    </div>

</template>

<style scoped>
.animate-up {
  animation: animateUp 1s ease forwards;
}

@keyframes animateUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>

<script>
export default {
  data() {
    return {
      imageSrc: "../public/off.png"
    };
  },
  methods: {
    changeImage() {
      this.imageSrc = "../public/on.png";
    },
    resetImage() {
      this.imageSrc = "../public/off.png";
    }
  },
  mounted() {
    const animateOnLoad = document.getElementById("animate-on-load");
    animateOnLoad.classList.add("animate-up");
  },
};
</script>
