<template>
  <section
    class="container mx-auto py-20"
    aria-labelledby="testimonial-heading"
  >
    <div class="max-w-5xl mx-auto px-4">
      <div class="bg-[#BFAFF2] rounded-3xl p-12">
        <div class="max-w-3xl">
          <h2 id="testimonial-heading" class="sr-only">
            Customer Testimonials
          </h2>
          <blockquote>
            <p class="text-2xl mb-8 leading-relaxed text-black">
              "Wallet is a great product! All of my most important information
              is there - credit cards, transit cards, boarding passes, tickets,
              and more. And I don't need to worry because it's all in one place!
              thanks!"
            </p>
            <footer class="flex items-center gap-4">
              <img
                src="/images/profile.png"
                alt="Johnny Owens profile picture"
                class="w-12 h-12 rounded-full"
                loading="lazy"
                width="48"
                height="48"
              />
              <div>
                <cite class="font-semibold text-black not-italic"
                  >Johnny Owens</cite
                >
                <div
                  class="flex gap-1 text-black"
                  aria-label="5 out of 5 stars rating"
                >
                  <svg
                    v-for="i in 5"
                    :key="i"
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                    role="img"
                    aria-hidden="true"
                  >
                    <path
                      d="M8 1L10.163 5.279L15 6.017L11.5 9.389L12.326 14L8 11.838L3.674 14L4.5 9.389L1 6.017L5.837 5.279L8 1Z"
                      fill="currentColor"
                    />
                  </svg>
                </div>
              </div>
            </footer>
          </blockquote>
        </div>
      </div>
    </div>
  </section>
</template>
