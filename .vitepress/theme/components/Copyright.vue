<template>
    
    <div class="site-footer">
        <!-- Cloudflare Web Analytics --><script defer src='https://static.cloudflareinsights.com/beacon.min.js' data-cf-beacon='{"token": "9af526794ac6469ca82aa59c961b0c0b"}'></script><!-- End Cloudflare Web Analytics -->
        Powered by <a class="vitepress" target="_blank" :href="vitepress">VitePress</a> |
        Theme by <a class="vitepress" target="_blank" :href="theme999">Vitepress-blog</a><br/>
        Copyright © 2025 <a class="vitepress" :href="website">{{ webTitle }}</a> | <script defer src="https://vercount.one/js"></script>Viewed: <span id="vercount_value_site_uv"></span> <br/>
    </div>
</template>
<script lang="ts" setup>
import { useData } from 'vitepress'

const { site, theme } = useData()
const website = theme.value.website
const webTitle = site.value.title
const vitepress = "https://vitepress.vuejs.org/"
const theme999 = "https://github.com/airene/vitepress-blog-pure/"
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
