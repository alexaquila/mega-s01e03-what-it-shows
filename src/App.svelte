<script>
const pages=import.meta.glob('./routes/kb/**/+page.svx',{eager:true});
const path=window.location.pathname.replace(/\/$/,'')||'/kb';
const mod=pages[`./routes${path}/+page.svx`]??pages['./routes/kb/incidents/4471-review/+page.svx'];
const Page=mod.default;
</script>
<Page {...mod.metadata} />
