<template>
  <section id="projects" class="py-20 px-6 bg-gray-50">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-3xl font-semibold text-gray-900 text-center mb-12">作品展示</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="bg-white border border-gray-200 rounded-lg overflow-hidden shadow-sm hover:shadow-md transition"
        >
          <img :src="project.image" :alt="project.title" class="w-full h-48 object-cover" />
          <div class="p-4">
            <h3 class="text-lg font-bold text-gray-800 mb-2">{{ project.title }}</h3>
            <p class="text-sm text-gray-600 mb-4">{{ project.description }}</p>
            <a
              v-if="project.link"
              :href="project.link"
              target="_blank"
              class="text-blue-600 text-sm font-medium hover:underline"
            >
              查看專案 →
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: "Vue 部落格平台",
    description:
      "使用 Vue 3 + Firebase 開發的個人部落格平台，支援 Markdown 編輯、用戶登入與文章分類管理。重點為資料同步與 Firebase 安全性設計。",
    image: "https://via.placeholder.com/400x250",
    link: "#",
  },
  {
    title: "Tailwind 商品頁面",
    description:
      "採用 Vue 3 + Tailwind CSS 建構的電商商品展示頁，包含篩選器、響應式設計與 hover 動畫效果。著重在 UI 元件重用與整體簡約排版。",
    image: "https://via.placeholder.com/400x250",
    link: "#",
  },
  {
    title: "SPA 天氣查詢站",
    description:
      "結合 Vue + Axios 與 OpenWeather API 製作的單頁應用程式，可即時查詢天氣並顯示圖示與氣溫。核心重點為 API 資料處理與條件渲染。",
    image: "https://via.placeholder.com/400x250",
    link: "#",
  },
]
</script>
