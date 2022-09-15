<template>
  <div class="relative max-w-4xl px-6 pt-12 pb-24 mx-auto space-y-8">
    <header
      class="relative overflow-hidden rounded-tr rounded-bl bg-gradient-to-br from-slate-900 to-slate-700 shadow-primary-600 rounded-tl-3xl rounded-br-3xl">
      <div class="md:flex md:justify-between">
        <h1 class="px-8 py-6 text-4xl font-extrabold text-white">
          {{ title }}
        </h1>
        <div class="flex items-center justify-end p-4 space-x-2">
          <NuxtLink to="/blog" target="_blank" class="p-1 text-primary-200 hover:text-primary-400">
            <svg xmlns="http://www.w3.org/2000/svg" class="text-yellow-400  h-16 w-16" fill="none" viewBox="0 0 24 24"
              stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21
                     12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </NuxtLink>
          <NuxtLink to="https://github.com/bryantgillespie/nuxt3-directus-starter" target="_blank"
            class="p-1 text-primary-200 hover:text-primary-400">
            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-8 h-8">
              <path fill-rule="evenodd" clip-rule="evenodd"
                d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z">
              </path>
            </svg>
          </NuxtLink>
          <ExamplesDarkModeToggle class="text-primary-200 hover:text-primary-400" />
        </div>
      </div>
      <div class="w-full h-4 bg-gradient-to-r from-primary-700 via-primary-600 to-pink-600" />
    </header>
    <div class="">
      <!-- <p class="text-primary-600">{{categories}}</p>
      <br>
      <p class="text-primary-600">{{pages}}</p> -->
      <TabGroup>
        <TabList class="flex space-x-1 rounded-xl bg-blue-900/20 p-1">
          <Tab v-for="category in pages" as="template" :key="category" v-slot="{ selected }">
            <button :class="[
              'w-full rounded-lg py-2.5 text-sm font-medium leading-5 text-blue-700',
              'ring-white ring-opacity-60 ring-offset-2 ring-offset-blue-400 focus:outline-none focus:ring-2',
              selected
                ? 'bg-white shadow'
                : 'text-blue-100 hover:bg-white/[0.12] hover:text-white',
            ]">
              {{ category.name }}
            </button>
          </Tab>
        </TabList>

        <TabPanels class="mt-2">
          <TabPanel v-for="category in pages" as="template" :key="category" :class="[
            'rounded-xl bg-white p-3',
            'ring-white ring-opacity-60 ring-offset-2 ring-offset-blue-400 focus:outline-none focus:ring-2',
          ]">
            <ul>
              <li v-for="post in category.articles" :key="post.id" class="relative rounded-md p-3 hover:bg-gray-100">
                <ExamplesPageCard
                  :path="`/${post.id}`"
                  :image="fileUrl(post.cover_image)"
                  :title="post.title"
                  :description="`/${post.author.last_name}`"
                />
                <h3 class="text-sm font-medium leading-5">
                  {{ post.title }}
                </h3>
                <ul class="mt-1 flex space-x-1 text-xs font-normal leading-4 text-gray-500">
                  <li>{{ post.author.last_name }}</li>
                </ul>

                <!-- <a href="{{ post.author.last_name }}" :class="[
                  'absolute inset-0 rounded-md',
                  'ring-blue-400 focus:z-10 focus:outline-none focus:ring-2',
                ]" /> -->
              </li>
            </ul>
          </TabPanel>
        </TabPanels>
      </TabGroup>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from '@headlessui/vue'
const title = 'Blog Page'
useMeta({
  title: title,
})
const categories = ref({
  Recent: [
    {
      id: 1,
      title: 'Does drinking coffee make you smarter?',
      date: '5h ago',
      commentCount: 5,
      shareCount: 2,
    },
    {
      id: 2,
      title: "So you've bought coffee... now what?",
      date: '2h ago',
      commentCount: 3,
      shareCount: 2,
    },
  ],
  Popular: [
    {
      id: 1,
      title: 'Is tech making coffee better or worse?',
      date: 'Jan 7',
      commentCount: 29,
      shareCount: 16,
    },
    {
      id: 2,
      title: 'The most innovative things happening in coffee',
      date: 'Mar 19',
      commentCount: 24,
      shareCount: 12,
    },
  ],
  Trending: [
    {
      id: 1,
      title: 'Ask Me Anything: 10 answers to your questions about coffee',
      date: '2d ago',
      commentCount: 9,
      shareCount: 5,
    },
    {
      id: 2,
      title: "The worst advice we've ever heard about coffee",
      date: '4d ago',
      commentCount: 1,
      shareCount: 2,
    },
  ],
})

const { $directus } = useNuxtApp()
const { fileUrl } = useFiles()

const pages = ref([])
const loading = ref(false)

async function fetchPages() {
  // loading.value = true
  // try {
  const { data } = await $directus.items('news_categories').readByQuery({
    fields: ["*", "articles.id", "articles.title", "articles.author.avatar", "articles.author.last_name", "articles.cover_image"],
    filter: {
      status: { _eq: 'published' },
    },
    limit: 5,
  })
  pages.value = data
  // } catch (e) {
  // console.error(e)
  // } finally {
  // loading.value = false
}

fetchPages()

</script>
