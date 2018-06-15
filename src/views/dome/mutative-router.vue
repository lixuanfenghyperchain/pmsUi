<style lang="less">
    @import './advanced-router.less';
</style>

<template>

    <Tabs>
        <TabPane label="首页" icon="ios-home">
            <div>
                <Row>
                    <Col span="24">
                    <Card style="height: 450px">
                        <p slot="title">

                            地方科研基础条件和能力建设
                        </p>
                        <Form :model="formItem" :label-width="120" inline>

                            <FormItem label="计划类别:">
                                <Input v-model="formItem.input1" disabled style="width: 220px" ></Input>
                            </FormItem>
                            <FormItem label="申报单位:">
                                <Input v-model="formItem.input2" disabled style="width: 220px" ></Input>
                            </FormItem>
                            <FormItem label="项目负责人:">
                                <Input v-model="formItem.input3" disabled style="width: 220px" ></Input>
                            </FormItem>
                            <FormItem label="初审单位类型:">
                                <Select v-model="formItem.input4"  style="width: 220px">
                                    <Option value="beijing">政务机构</Option>
                                    <Option value="shanghai">各科技局</Option>
                                    <Option value="shenzhen">高等院校</Option>
                                </Select>
                            </FormItem>
                            <FormItem label="初审单位名称:">
                                <Input v-model="formItem.input5" style="width: 220px" ></Input>
                            </FormItem>
                            <FormItem label="初审财政部门名称:">
                                <Input v-model="formItem.input6" style="width: 220px" ></Input>
                            </FormItem>
                            <FormItem label="主管部门:">
                                <Input v-model="formItem.input7" style="width: 220px" ></Input>
                            </FormItem>
                            <FormItem label="申报日期:">

                                <DatePicker type="date" placeholder="Select date" v-model="formItem.input8" style="width: 220px" ></DatePicker>


                            </FormItem>
                            <FormItem label="项目起止日期:">
                                <Input v-model="formItem.input9" style="width: 220px" ></Input>
                            </FormItem>
                            <FormItem >
                                <Button type="primary"  @click="handleSubmit()">保存</Button>
                                <Button type="ghost" style="margin-left: 8px">重置</Button>
                            </FormItem>
                        </Form>
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
            formItem: {
              input1: '地方科研基础条件和能力建设',
              input2: '北京志鸿中科科技有限公司',
              input3: '汪铁伦',
              select: '',
              radio: 'male',
              checkbox: [],
              switch: true,
              date: '',
              time: '',
              slider: [20, 50],
              textarea: ''
            }
          }
        },
        methods: {
          handleSubmit () {
            this.$ajax({
              method: 'post',
              url: '/api/drummer/8bd17859',
              data: {
                code: '1234567',
                username: 'Joyce'
              }
            }).then(response=>{
              let _data=response.data;
              alert("hello," + _data.username);
            }).catch(function(err){
              this.$Message.error('保存失败');
            }.bind(this));

          }
        }
      };
</script>

