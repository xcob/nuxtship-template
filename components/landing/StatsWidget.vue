<script setup>
const features = [
  {
    title: "Bring Your Own Framework",
    description:
      "Build your site using Vue, web components, or just plain ol' HTML + JavaScript.",
    icon: "blob-1",
  },
  {
    title: "100% Static HTML, No JS",
    description:
      "Nuxt renders your entire page to static HTML, removing all JavaScript from your final build by default.",
    icon: "blob-3",
  },
  {
    title: "On-Demand Components",
    description:
      "Need some JS? Nuxt can automatically hydrate interactive components when they become visible on the page.  ",
    icon: "blob-5",
  },
  {
    title: "Broad Integration",
    description:
      "Nuxt supports TypeScript, Scoped CSS, CSS Modules, Sass, Tailwind, Markdown, MDX, and any other npm packages.",
    icon: "blob-7",
  },
  {
    title: "SEO Enabled",
    description:
      "Automatic sitemaps, RSS feeds, pagination and collections take the pain out of SEO and syndication. It just works!",
    icon: "blob-8",
  },
  {
    title: "Community",
    description:
      "Nuxt is an open source project powered by hundreds of contributors making thousands of individual contributions.",
    icon: "blob-9",
  },
];
</script>

<template>

<div class="flex flex-col justify-center items-center h-[100vh] pt-4">
<div class="min-w-[375px] md:min-w-[700px] xl:min-w-[800px] mt-3 grid grid-cols-1 gap-5 md:grid-cols-2 lg:grid-cols-3 2xl:grid-cols-3 3xl:grid-cols-6">
    <div v-for="item of features" class="flex gap-4 items-start">
        <div class="relative flex flex-grow !flex-row flex-col items-center rounded-[10px] rounded-[10px] border-[1px] border-gray-200 bg-white bg-clip-border shadow-md shadow-[#F3F3F3] dark:border-[#ffffff33] dark:!bg-navy-800 dark:text-white dark:shadow-none">
            <div class="ml-[18px] flex h-[90px] w-auto flex-row items-center">
            <div class="rounded-full bg-lightPrimary p-3 dark:bg-navy-700">
                <span class="flex items-center text-brand-500 dark:text-white">
                <svg
                    stroke="currentColor"
                    fill="#4e79fa"
                    stroke-width="0"
                    viewBox="0 0 24 24"
                    class="h-7 w-7"
                    height="1em"
                    width="1em"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path fill="#4e79fa30" d="M0 0h24v24H0z"></path>
                    <path d="M4 9h4v11H4zM16 13h4v7h-4zM10 4h4v16h-4z"></path>
                </svg>
                </span>
            </div>
            </div>
            <div class="h-50 ml-4 flex w-auto flex-col justify-center">
            <p class="font-dm text-sm font-medium text-gray-600">{{ item.title }}</p>
            <h4 class="text-xl font-bold text-navy-700 dark:text-white"> {{ item.description }}</h4>
            </div>
        </div>
  </div>
  </div>
  </div>
</template>
