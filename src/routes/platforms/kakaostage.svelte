<script>
    import PlatformInfo from "../../components/platform/platform-info.svelte";
    import Heatmap from "../../components/platform/heatmap.svelte"
    import GenreTable from "../../components/platform/genreTable.svelte";
    import MonopolyTable from "../../components/platform/monopolyTable.svelte";
    import UploadPeriodTable from "../../components/platform/uploadPeriodTable.svelte";
    import KeywordsTagsTable from "../../components/platform/keywordsTagsTable.svelte";

    import KakaostageData from "../../jsondata/kakaostage.json"
</script>

<PlatformInfo platformInfoData={KakaostageData.platformInfoData}/>
<Heatmap heatmapData={KakaostageData.heatmapData} platformPricings={KakaostageData.platformInfoData.platformPricings} platformGenres={KakaostageData.platformInfoData.platformGenres}/>
<GenreTable genreData={KakaostageData.genreData}/>
<MonopolyTable monopolyData={KakaostageData.monopolyData}/>
<UploadPeriodTable weeklyUploadCountData={KakaostageData.weeklyUploadCountData}/>
<KeywordsTagsTable keywordsTagsData={KakaostageData.keywordsTagsData}/>