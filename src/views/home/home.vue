<template>
  <div class="h-screen w-screen bg-raisinBlack overflow-hidden">
    <div class="h-full grid container grid-cols-2 mx-auto items-center">
      <div class="text-snow">
        <div class="uppercase font-bold text-[100px]">Nuran</div>
        <div class="uppercase font-bold text-[100px]">Jafarov</div>
        <div class="text-2xl">Full Stack Developer | Mechatronics Engineer</div>
      </div>
      <div class="text-snow text-right">
        <div class="grid grid-rows-3 gap-y-3 text-xl">
          <div>
            <a
              ref="email"
              class="mr-2 align-middle"
              data-name="nuran.jafarov"
              data-domain="gmail"
              data-tld="com"
              @click.prevent="sendEmail"
            >
              Email
            </a>
            <i class="fas fa-envelope align-middle text-center"></i>
          </div>
          <div>
            <a
              class="mr-2 align-middle"
              href="https://www.linkedin.com/in/nuran-jafarov/"
              target="_blank"
            >
              Linkedin
            </a>
            <i class="fab fa-linkedin align-middle text-center text-2xl"></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const email = ref();

function sendEmail() {
  const dataset = email.value.dataset;
  window.location.href = `mailto:${dataset.name}@${dataset.domain}.${dataset.tld}`;
}
</script>
