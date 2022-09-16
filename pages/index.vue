<template>
  <div class="relative max-w-4xl px-6 pt-12 pb-24 mx-auto space-y-8">
    <header
      class="relative overflow-hidden rounded-tr rounded-bl bg-gradient-to-br from-slate-900 to-slate-700 shadow-primary-600 rounded-tl-3xl rounded-br-3xl"
    >
      <div class="md:flex md:justify-between">
        <h1 class="px-8 py-6 text-4xl font-extrabold text-white">
          {{ title }}
        </h1>
        <div class="flex items-center justify-end p-4 space-x-2">
          <NuxtLink
            to="/contact"
            target="_blank"
            class="p-1 text-primary-200 hover:text-primary-400"
          >
          <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px"
          width="64" height="64"
          viewBox="0 0 64 64"
          style=" fill:#000000;"><linearGradient id="KsXfRWqbBCH2nOp40Xinpa_rLvjylyopRJT_gr1" x1="28" x2="28" y1="12.352" y2="53.263" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#6dc7ff"></stop><stop offset="1" stop-color="#e6abff"></stop></linearGradient><ellipse cx="28" cy="41.5" fill="url(#KsXfRWqbBCH2nOp40Xinpa_rLvjylyopRJT_gr1)" rx="9" ry="3.5"></ellipse><linearGradient id="KsXfRWqbBCH2nOp40Xinpb_rLvjylyopRJT_gr2" x1="28" x2="28" y1="12.352" y2="53.263" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#6dc7ff"></stop><stop offset="1" stop-color="#e6abff"></stop></linearGradient><ellipse cx="28" cy="29" fill="url(#KsXfRWqbBCH2nOp40Xinpb_rLvjylyopRJT_gr2)" rx="4" ry="5"></ellipse><linearGradient id="KsXfRWqbBCH2nOp40Xinpc_rLvjylyopRJT_gr3" x1="50" x2="50" y1="12.352" y2="53.263" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#6dc7ff"></stop><stop offset="1" stop-color="#e6abff"></stop></linearGradient><path fill="url(#KsXfRWqbBCH2nOp40Xinpc_rLvjylyopRJT_gr3)" d="M48.22,54H46V10h2.22c3.192,0,5.78,2.588,5.78,5.78v32.44C54,51.412,51.412,54,48.22,54z"></path><linearGradient id="KsXfRWqbBCH2nOp40Xinpd_rLvjylyopRJT_gr4" x1="32" x2="32" y1="7.505" y2="43.825" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#1a6dff"></stop><stop offset="1" stop-color="#c822ff"></stop></linearGradient><path fill="url(#KsXfRWqbBCH2nOp40Xinpd_rLvjylyopRJT_gr4)" d="M47.923,9H16.077C12.168,9,9,12.168,9,16.077v31.846C9,51.832,12.168,55,16.077,55h31.846 C51.832,55,55,51.832,55,47.923V16.077C55,12.168,51.832,9,47.923,9z M53,16.077V20h-6v-9h0.923C50.727,11,53,13.273,53,16.077z M47,33h6v9h-6V33z M47,31v-9h6v9H47z M11,47.923V16.077C11,13.273,13.273,11,16.077,11H45v42H16.077 C13.273,53,11,50.727,11,47.923z M47.923,53H47v-9h6v3.923C53,50.727,50.727,53,47.923,53z"></path><linearGradient id="KsXfRWqbBCH2nOp40Xinpe_rLvjylyopRJT_gr5" x1="28" x2="28" y1="7.505" y2="43.825" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#1a6dff"></stop><stop offset="1" stop-color="#c822ff"></stop></linearGradient><path fill="url(#KsXfRWqbBCH2nOp40Xinpe_rLvjylyopRJT_gr5)" d="M28,46c-7.72,0-14-6.28-14-14s6.28-14,14-14s14,6.28,14,14S35.72,46,28,46z M28,20 c-6.617,0-12,5.383-12,12s5.383,12,12,12s12-5.383,12-12S34.617,20,28,20z"></path><linearGradient id="KsXfRWqbBCH2nOp40Xinpf_rLvjylyopRJT_gr6" x1="28" x2="28" y1="7.505" y2="43.825" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#1a6dff"></stop><stop offset="1" stop-color="#c822ff"></stop></linearGradient><path fill="url(#KsXfRWqbBCH2nOp40Xinpf_rLvjylyopRJT_gr6)" d="M28,35c-2.757,0-5-2.691-5-6s2.243-6,5-6s5,2.691,5,6S30.757,35,28,35z M28,25 c-1.654,0-3,1.794-3,4s1.346,4,3,4s3-1.794,3-4S29.654,25,28,25z"></path><linearGradient id="KsXfRWqbBCH2nOp40Xinpg_rLvjylyopRJT_gr7" x1="28" x2="28" y1="7.505" y2="43.825" gradientUnits="userSpaceOnUse"><stop offset="0" stop-color="#1a6dff"></stop><stop offset="1" stop-color="#c822ff"></stop></linearGradient><path fill="url(#KsXfRWqbBCH2nOp40Xinpg_rLvjylyopRJT_gr7)" d="M37.449,41.835C33.709,39.368,29.924,39,28,39s-5.709,0.368-9.449,2.835l-1.102-1.67 C21.626,37.411,25.853,37,28,37s6.374,0.411,10.551,3.165L37.449,41.835z"></path>
          </svg>
          </NuxtLink>
          <NuxtLink
            to="/blog"
            target="_blank"
            class="p-1 text-primary-200 hover:text-primary-400"
          >
          <svg xmlns="http://www.w3.org/2000/svg"
               class="text-yellow-400  h-16 w-16" fill="none"
               viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round"
                  stroke-width="2"
                  d="M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21
                     12a9 9 0 11-18 0 9 9 0 0118 0z" />
          </svg>
          </NuxtLink>
          <NuxtLink
            to="https://github.com/bryantgillespie/nuxt3-directus-starter"
            target="_blank"
            class="p-1 text-primary-200 hover:text-primary-400"
          >
            <svg
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
              fill="currentColor"
              class="w-8 h-8"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
              ></path>
            </svg>
          </NuxtLink>
          <ExamplesDarkModeToggle
            class="text-primary-200 hover:text-primary-400"
          />
        </div>
      </div>
      <div
        class="w-full h-4 bg-gradient-to-r from-primary-700 via-primary-600 to-pink-600"
      />
    </header>

    <div>
      <VAlert type="warning">
        <strong>Warning:</strong>
        Nuxt 3 is currently still in Release Candiate so I wouldn't recommend it
        for production use because of possible breaking changes.
      </VAlert>
      <ExamplesLogos />
    </div>

    <div
      id="examples"
      class="relative flex-1 divide-y-2 divide-gray-200 dark:divide-gray-800"
    >
      <h2
        class="pb-6 text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-primary-700 to-pink-600"
      >
        Examples of Functionality
      </h2>
      <ExamplesContent id="content" class="py-12" />
      <ExamplesAuth id="authentication" class="py-12" />
      <ExamplesApiRoutes id="api" class="py-12" />
    </div>
    <div
      id="components"
      class="relative flex-1 divide-y-2 divide-gray-200 dark:divide-gray-800"
    >
      <h2
        class="pb-6 text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-primary-700 to-pink-600"
      >
        Demo of Components
      </h2>
      <ExamplesComponents />
    </div>
    <footer
      class="relative rounded-tr rounded-bl md:flex md:justify-between bg-gray-50 dark:bg-gray-800 rounded-tl-3xl rounded-br-3xl"
    >
      <div class="p-8">
        <h1 class="text-4xl font-extrabold dark:text-white">
          {{ title }}
        </h1>
        <div class="mt-4 text-gray-700 dark:text-gray-200">
          <p>Created by Bryant Gillespie</p>
          <NuxtLink to="https://twitter.com/bryantgillespie" target="_blank"
            >@bryantgillespie</NuxtLink
          >
        </div>
      </div>

      <div class="flex items-center justify-end p-4 space-x-2">
        <NuxtLink
          to="https://github.com/bryantgillespie/nuxt3-directus-starter"
          target="_blank"
          class="p-1 dark:text-primary-200 dark:hover:text-primary-400 text-primary-700 hover:text-primary-900"
        >
          <svg
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
            fill="currentColor"
            class="w-8 h-8"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
            ></path>
          </svg>
        </NuxtLink>
        <ExamplesDarkModeToggle
          class="dark:text-primary-200 dark:hover:text-primary-400 text-primary-700 hover:text-primary-900"
        />
      </div>
    </footer>
  </div>
</template>

<script setup>
const title = 'Directus & Nuxt 3 Starter'
useMeta({
  title: title,
})
</script>
