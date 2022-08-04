<script>
    import MainPlatformInfo from "../components/platform/mainPlatformInfo.svelte";

    import MunpiaData from "../jsondata/munpia.json"
    import NovelpiaData from "../jsondata/novelpia.json"
    import KakaopageData from "../jsondata/kakaopage.json"
    import KakaostageData from "../jsondata/kakaostage.json"
    import NavernovelData from "../jsondata/navernovel.json"

</script>

<svelte:head>
    <title>웹소지지</title>
</svelte:head>
<div class="container px-3 py-2.5 mt-6 flex flex-col justify-center ">
    <MainPlatformInfo platformInfo={MunpiaData.platformInfoData} platformPageName="munpia"/>
    <MainPlatformInfo platformInfo={NovelpiaData.platformInfoData} platformPageName="novelpia"/>
    <MainPlatformInfo platformInfo={KakaopageData.platformInfoData} platformPageName="kakaopage"/>
    <MainPlatformInfo platformInfo={KakaostageData.platformInfoData} platformPageName="kakaostage"/>
    <MainPlatformInfo platformInfo={NavernovelData.platformInfoData} platformPageName="navernovel"/>
</div>