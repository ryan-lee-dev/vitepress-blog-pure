<template>
    <div class="site-footer">
        Copyright © 2025 <a class="vitepress" :href="website">{{ webTitle }}</a> | <span id="busuanzi_container_site_pv">Viewed: <span id="busuanzi_value_site_pv"></span></span><br />
        Powered by <a class="vitepress" target="_blank" href="//vitepress.vuejs.org/">VitePress</a>
        And  <a class="vitepress" target="_blank" href="//github.com/airene/vitepress-blog-pure">Vitepress-blog</a><br />
    <!-- Cloudflare Web Analytics --><script defer src='https://static.cloudflareinsights.com/beacon.min.js' data-cf-beacon='{"token": "9af526794ac6469ca82aa59c961b0c0b"}'></script><!-- End Cloudflare Web Analytics -->
    </div>
</template>
<script lang="ts" setup>
import { useData } from 'vitepress'

const { site, theme } = useData()
const website = theme.value.website
const webTitle = site.value.title
</script>

<style>
.site-footer {
    color: #888;
    text-align: center;
    font-size: 0.75rem;
    width: 100%;
    padding: 15px 0;
    overflow: auto;
}
.vitepress {
    color: var(--vp-c-text-1);
    font-weight: 700;
}
</style>
