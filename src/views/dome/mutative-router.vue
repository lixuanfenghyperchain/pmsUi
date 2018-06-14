<style lang="less">
    @import './advanced-router.less';
</style>

<template>

    <Tabs>
        <TabPane label="首页" icon="ios-home">
            <div>
                <Row>
                    <Col span="24">
                    <Card>
                        <p slot="title">

                            地方科研基础条件和能力12
                        </p>
                        <Input v-model="value" placeholder="Enter something..." style="width: 300px"></Input>

                    </Card>
                    </Col>
                </Row>
            </div>
        </TabPane>
        <TabPane label="项目基本信息" icon="ios-paper-outline">标签二的内容</TabPane>
        <TabPane label="项目绩效目标" icon="ios-paper-outline">标签三的内容</TabPane>
    </Tabs>


</template>

    <script>
  export default {
    data () {
      return {
        value: ''
      }
    }
  }
</script>

