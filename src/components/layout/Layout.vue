<template>
    <div>
        <layout-header></layout-header>
        <router-view></router-view>
        <layout-footer>
            <icp-info></icp-info>
        </layout-footer>
    </div>
</template>
<script>
    import LayoutHeader from "./LayoutHeader";
    import LayoutFooter from "./LayoutFooter";
    import IcpInfo from "./IcpInfo";
    export default {
        name: 'Layout',
        components: {
            IcpInfo,
            LayoutHeader,
            LayoutFooter,
        },
    }
</script>
