<template>
  <div class="w-full md:w-96 md:max-w-full mx-auto">
    <div class="p-6 border border-gray-300 sm:rounded-md">
      <form action="https://public.herotofu.com/v1/ca7e6ba0-3572-11ed-9de0-b73c4b901972" method="post">
        <label class="block mb-6">
          <span class="text-gray-700">Your name</span>
          <input
            type="text"
            name="name"
            class="
              block
              w-full
              mt-1
              border-gray-300
              rounded-md
              shadow-sm
              focus:border-indigo-300
              focus:ring
              focus:ring-indigo-200
              focus:ring-opacity-50
            "
            placeholder="Joe Bloggs"
          />
        </label>
        <label class="block mb-6">
          <span class="text-gray-700">Email address</span>
          <input
            name="email"
            type="email"
            class="
              block
              w-full
              mt-1
              border-gray-300
              rounded-md
              shadow-sm
              focus:border-indigo-300
              focus:ring
              focus:ring-indigo-200
              focus:ring-opacity-50
            "
            placeholder="joe.bloggs@example.com"
            required
          />
        </label>
        <label class="block mb-6">
          <span class="text-gray-700">Message</span>
          <textarea
            name="message"
            class="
              block
              w-full
              mt-1
              border-gray-300
              rounded-md
              shadow-sm
              focus:border-indigo-300
              focus:ring
              focus:ring-indigo-200
              focus:ring-opacity-50
            "
            rows="3"
            placeholder="Tell us what you're thinking about..."
          ></textarea>
        </label>
        <div class="mb-6">
          <button
            id="form-submit"
            type="submit"
            class="
              h-10
              px-5
              text-indigo-100
              bg-indigo-700
              rounded-lg
              transition-colors
              duration-150
              focus:shadow-outline
              hover:bg-indigo-800
            "
          >
            Contact Us
          </button>
        </div>
        <div>
          <div class="mt-2 text-gray-700 text-right text-xs">
            by
            <a href="https://herotofu.com" class="hover:underline" target="_blank"
              >HeroTofu</a
            >
          </div>
        </div>
      </form>
    </div>
  </div>
</template>
