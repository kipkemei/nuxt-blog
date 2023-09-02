<template>
  <div>
    <p class="text-black text-2xl py-1 font-semibold">
      Sang Dennis
    </p>
    <p class="py-2">
      Hi! My name is Sang Dennis, a Tech enthusiast, problem solver and software engineer.
    </p>
    <div class="my-3 space-x-3 pb-3">
      <NuxtLink
        to="https://github.com/kipkemei"
        target="_blank"
        class="p-2 bg-gray-300 rounded-md"
        aria-label="Github"
      >
        <Icon name="fa:github" size="1em" />
      </NuxtLink>
      <NuxtLink
        to="https://www.linkedin.com/in/sangdennis/"
        target="_blank"
        class="p-2 bg-gray-300 rounded-md"
        aria-label="LinkedIn"
      >
        <Icon name="fa:linkedin-square" size="1em" />
      </NuxtLink>
      <NuxtLink
        to="https://twitter.com/dennis_sang"
        target="_blank"
        class="p-2 bg-gray-300 rounded-md"
        aria-label="Twitter"
      >
        <Icon name="fa:twitter-square" size="1em" />
      </NuxtLink>
      <NuxtLink
        to="https://stackoverflow.com"
        target="_blank"
        class="p-2 bg-gray-300 rounded-md"
        aria-label="StackOverflow"
      >
        <Icon name="fa:stack-overflow" size="1em" />
      </NuxtLink>
    </div>
  </div>
</template>
