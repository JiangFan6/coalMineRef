
<template>
    <div class="enterpriseInfor-index commonLinks" data-pageindex="1" :data-link="linkCodeBox.breakFormation">

        <!--2.2中间正文-->
        <div class="coalMineInformation">
            <div class="inforSearch-form">
                <div class="inforSearch-form-stable">
                    <div class="inforSearch-form-row">
                        <Row>
                            <Col span="24" class="inforSearch-form-title">断层查询</Col>
                        </Row>
                        <Breadcrumb class="inforSearch-form-breadcrumb">
                            <span>当前位置：</span>
                            <Breadcrumb-item class="inforSearch-form-breadcrumb-item" href="/coalFormation">煤矿信息</Breadcrumb-item>
                            <Breadcrumb-item class="inforSearch-form-breadcrumb-item" href="/coalFormation">煤层地质信息</Breadcrumb-item>
                            <Breadcrumb-item class="inforSearch-form-breadcrumb-item">断层</Breadcrumb-item>
                        </Breadcrumb>
                    </div>
                    <div class="inforSearch-form-row coalMineInfor-public">
                        <Row>
                            <Col span="12">
                            <Input class="coalseamName">
                            <span slot="prepend">煤层名称</span>
                            </Input>
                            </Col>

                        </Row>
                    </div>
                </div>
                <!--更多条件公共组件-->
                <getMoreConditions></getMoreConditions>
                <staticAnalysis></staticAnalysis>

            </div>

        </div>
        <div class="coalMineInformation-body">
            <showDataList ></showDataList>
        </div>

    </div>

</template>

<script>
    import Vue from 'vue'
    import getMoreConditions from '../../../publicInforSearch/getMoreConditions.vue'
    import VDistpicker from 'v-distpicker'
    import showDataList from '../../../publicInforSearch/showDataList.vue'
    import {mapGetters} from 'vuex'
    import staticAnalysis from '../../../publicInforSearch/staticAnalysis.vue'


    export default{
        name: 'breakFormation',
        data () {
            return {
            }
        },
        components: {
            getMoreConditions,
            VDistpicker,
            showDataList,
            staticAnalysis
        },
        computed: {
                ...mapGetters({
                    listShow: 'listShow',
                    linkCodeBox:'linkCodeBox'

                })
    }
    }



</script>

<style scoped>

    @import "../../../../../assets/css/init-css.css";


</style>