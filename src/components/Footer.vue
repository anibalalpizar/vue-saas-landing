<template>
  <footer class="border-t border-[#404040] py-8" role="contentinfo">
    <div class="container mx-auto px-4">
      <div
        class="flex flex-col md:flex-row justify-between items-start md:items-center gap-6"
      >
        <div
          class="flex flex-col md:flex-row items-start md:items-center gap-6"
        >
          <span class="text-sm text-white">© Wallet 2022</span>
          <nav aria-label="Footer Navigation">
            <ul class="flex gap-6 text-sm">
              <li>
                <a
                  href="#"
                  class="text-white hover:text-gray-300 transition-colors"
                  >Privacy policy</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-white hover:text-gray-300 transition-colors"
                  >Cookies policy</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-white hover:text-gray-300 transition-colors"
                  >Terms of use</a
                >
              </li>
            </ul>
          </nav>
        </div>
        <div
          class="flex flex-col md:flex-row items-start md:items-center gap-4"
        >
          <span class="text-sm text-[#E5B93E]"
            >Updates right to your inbox</span
          >
          <form
            class="flex gap-2 w-full md:w-auto"
            aria-label="Newsletter Subscription"
          >
            <label class="sr-only" for="email-input">Email Address</label>
            <input
              type="email"
              id="email-input"
              placeholder="Email Address"
              class="bg-[#333333] text-white text-sm px-4 py-2 rounded focus:outline-none focus:ring-1 focus:ring-[#E5B93E] w-full md:w-auto"
              required
            />
            <button
              type="submit"
              class="bg-[#A490E5] hover:bg-[#9481D6] text-black text-sm px-4 py-2 rounded transition-colors"
              aria-label="Subscribe to newsletter"
            >
              Subscribe
            </button>
          </form>
        </div>
      </div>
    </div>
  </footer>
</template>
