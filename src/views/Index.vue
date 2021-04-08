<template>
    <div class="layout">
        <Layout>
            <Header style="padding: 0px">
                <HeaderComponent></HeaderComponent>
            </Header>
            <Layout>
                <Sider hide-trigger>
                    <keep-alive>
                        <Menu></Menu>
                    </keep-alive>
                </Sider>
                <Content class="layout-container">
                    <router-view class="router-content"></router-view>
                    <Footer><FooterComponent></FooterComponent></Footer>
                </Content>

            </Layout>
        </Layout>
    </div>
</template>
<script>
    import Menu from '../components/Menu'
    import HeaderComponent from '../components/Header'
    import FooterComponent from '../components/Footer'

    export default {
        name: 'index',
        methods: {

        },
        components: {
            Menu,
            HeaderComponent,
            FooterComponent
        },
        mounted() {
        }
    }
</script>
<style scoped>
    .layout {
      height: 100vh;
    }
    .layout .ivu-layout {
      height: 100%;
    }
    .layout-container {
      height: 100%;
    }
    .router-content {
        margin: 20px;
        text-align: left;
    }
</style>
