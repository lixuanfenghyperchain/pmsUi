<style lang="less" scoped>
    @import 'finance-info.less';
</style>

<style lang="less">
    @import 'common.less';
</style>

<template>
    <Tabs>
        <TabPane label="财务信息" icon="ios-home">
            <div>
                <Row>
                    <Col span="24">
                    <Card>
                        <div slot="title">
                            <b>财务信息表单</b>
                            <small style="color: red;">(注意：事业单位没有的信息可不填写)</small>
                            <ButtonGroup style="float: right;">
                                <Button type="primary" size="small" @click="handleSubmit()">保存</Button>
                                <Button type="ghost" size="small" style="margin-left: 8px">重置</Button>
                            </ButtonGroup>
                        </div>

                        <Form :label-width="120" inline>
                            <Row>
                                <!-- justify: 水平对齐方式 可选值为start、end、center、space-around、space-between
                                    align: 垂直对齐方式 可选值为top、middle、bottom -->
                                <Col span="8" justify="center" align="middle"><div class="header-col"><small>职工人数</small></div></Col>
                                <Col span="8" justify="center" align="middle"><div class="header-col"><small>上年度</small></div></Col>
                                <Col span="8" justify="center" align="middle"><div class="header-col"><small>本年度</small></div></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">1.参加养老保险职工人数</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 人 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 人 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">2.财务人员</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 人 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 人 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">其中：中级以上财务人员</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 人 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 人 </small></Col>
                            </Row>
                            <Row>
                                <Col span="8" justify="center" align="middle"><div class="header-col"><small>项目</small></div></Col>
                                <Col span="8" justify="center" align="middle"><div class="header-col"><small>上年度</small></div></Col>
                                <Col span="8" justify="center" align="middle"><div class="header-col"><small>本年一月至</small><Input class="bg-blue" size="small" style="width: 45px;"></Input><small>累计</small></div></Col>
                            </Row>
                            <!--　1　-->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">1.资产总额</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <!-- 2 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">2.负债总额</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <!-- 3 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">3.销售收入</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <!-- 4 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">4.实现利润</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 5 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">5.企业提取技术开发费用</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">其中：（1） 购置新技术</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（2） 科技人员人工支出</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（3） 研究开发费用</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（4） 研究开发性固定资产购置</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（5） 其他研究支出费用</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 6 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">6.产值</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 7 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">7.应发职工工资</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 8 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">8.实发职工工资</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 9 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">9.实收资本</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（1） 国家资本</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（2） 集体资本</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（3） 法人资本</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（4） 个人资本</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（5） 外商资本</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 10 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">10.资本公积</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 11 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">10.盈余公积</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 12 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">12.缴纳各项税金情况</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（1） 年初未缴各项税金</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（2） 本年应缴各项税金</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（3） 本年已缴各项税金</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（4） 年末未缴各项税金</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（5） 减免税金</small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input class="bg-blue" size="small"></Input><small> 万元 </small></Col>
                            </Row>

                            <!-- 13 -->
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">13.缴纳各种保险情况</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <!--<Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（1） 年初未缴各项社会保险</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（2） 本年应缴各项社会保险</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（3） 本年已缴各项社会保险</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>
                            <Row class-name="row-margin">
                                <Col span="8"><small style="width: 220px; margin: 5px; height: 24px;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;（4） 年末未缴各项社会保险</small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                                <Col span="8" justify="center" align="middle"><Input size="small"></Input><small> 万元 </small></Col>
                            </Row>-->
                            <Row class-name="row-margin">
                                <template v-for="item in formItem">
                                    <Col v-if="item.type == 'text-box'" span="8" justify="center" align="middle">
                                        <template v-for="tag in item.content">
                                            <small v-if="tag.tag == 'small'">{{tag.text}}</small>
                                            <Input v-else-if="tag.tag == 'input'" size="small"></Input>
                                        </template>
                                    </Col>
                                    <Col v-else-if="item.type == 'header-row'" span="8">
                                        <small style="width: 220px; margin: 5px; height: 24px;"><small v-if="item.content[0].tab">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</small>{{item.content[0].text}}</small>
                                    </Col>
                                    <Col v-else-if="item.type == 'header-col'" span="8" justify="center" align="middle">
                                        <div class="header-col">
                                            <template v-for="tag in item.content">
                                                <small v-if="tag.tag == 'small'">{{tag.text}}</small>
                                                <Input v-else-if="tag.tag == 'input'" size="small" :class="tag.class" :style="tag.style"></Input>
                                            </template>
                                        </div>
                                    </Col>
                                </template>
                            </Row>
                        </Form>
                    </Card>
                    </Col>
                </Row>
            </div>
        </TabPane>
        <TabPane label="年度财务指标基本数据" icon="ios-paper-outline">
            <div>
                <Row>
                    <Col>
                        <Card>
                            <div slot="title">
                                <b>年度财务指标基本数据</b>
                                <small style="color: red;">(填报数据应已经审计的财务报告为准，还未审计的年度已真实准确的财务报表为准，如果是新成立的公司没有的某年度可以全部填写为"0")</small>
                                <Button type="primary" size="small" @click="showModel = true" style="margin-left: 8px; float: right;">录入数据</Button>
                                <Modal v-model="showModel" title="录入数据" width="900px" @on-ok="ok" @on-cancel="cancel" ok-text="保存" cancel-text="关闭">
                                    <div slot="header">
                                        <b>年度财务指标基本数据</b>
                                        <small style="color: red;">（填报数据应以经审计的财务报告为准，还未审计的年度以真实准确的财务报表为准，如果是新成立的公司没有的某年度可以全部填写为"0"）</small>
                                    </div>
                                    <Form :label-width="150" inline>
                                        <Row class-name="row-margin">
                                            <Col span="8">
                                                <FormItem label="指标年度:">
                                                    <Select size="small" class="short bg-blue">
                                                        <Option value="2016">2016</Option>
                                                        <Option value="2017">2017</Option>
                                                    </Select>
                                                </FormItem>
                                            </Col>
                                        </Row>
                                        <Row class-name="row-margin">
                                            <Col span="7" justify="center" align="middle"><FormItem label="注册资金:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="资产总额:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="负债总额:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                        </Row>
                                        <Row class-name="row-margin">
                                            <Col span="7" justify="center" align="middle"><FormItem label="营业收入:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="利润总额:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="经营活动现金流入:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                        </Row>
                                        <Row class-name="row-margin">
                                            <Col span="7" justify="center" align="middle"><FormItem label="经营活动现金流出:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="经营活动现金净流量:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="资产负债率:"><Input size="small" class="short bg-gray"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> % </label></Col>
                                        </Row>
                                        <Row class-name="row-margin">
                                            <Col span="7" justify="center" align="middle"><FormItem label="资产总额利润率:"><Input size="small" class="short bg-gray"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> % </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="流动比率:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> % </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="速动比率:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> % </label></Col>
                                        </Row>
                                        <Row class-name="row-margin">
                                            <Col span="7" justify="center" align="middle"><FormItem label="应发职工工资:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="实发职工工资:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="营业收入利润率:"><Input size="small" class="short bg-gray"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> % </label></Col>
                                        </Row>
                                        <Row class-name="row-margin">
                                            <Col span="7" justify="center" align="middle"><FormItem label="应收账款周转率:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> % </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="期初未交税金:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="应交税金:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                        </Row>
                                        <Row class-name="row-margin">
                                            <Col span="7" justify="center" align="middle"><FormItem label="已交税金:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="企业研发投入:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="年初未缴各种社会保险:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                        </Row>
                                        <Row class-name="row-margin">
                                            <Col span="7" justify="center" align="middle"><FormItem label="本年应缴各种社会保险:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="本年已缴各种社会保险:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                            <Col span="7" justify="center" align="middle"><FormItem label="年末未缴各种社会保险:"><Input size="small" class="short bg-blue"></Input></FormItem></Col>
                                            <Col span="1"><label class="ivu-form-item-label"> 万元 </label></Col>
                                        </Row>
                                        <hr style="height: 0; border-top: 1px solid orange; margin-top: 6px;">
                                        <b style="color: red;">注意:</b>
                                        <Row class-name="row-margin" style="color: red;">
                                            <Col span="8" align="top">1.资产负债率(%)=负债总额/资产总额。</Col>
                                            <Col span="8" align="top">2.资产总额利润率(%)=利润总额/资产总额。</Col>
                                            <Col span="8" align="top">3.流动比率(%)=流动资产/流动负债。</Col>
                                        </Row>
                                        <Row class-name="row-margin" style="color: red;">
                                            <Col span="8" align="top">4.速动比率(%)=(流动资产-存货-待摊费用)/流动负债。</Col>
                                            <Col span="8" align="top">5.营业收入利润率(%)=利润总额/营业收入。</Col>
                                            <Col span="8" align="top">6.应收账款周转率(%)=营业收入/平均应收账款。</Col>
                                        </Row>
                                    </Form>
                                </Modal>
                            </div>
                            <Row type="flex" justify="center" class="advanced-router">
                                <Table :columns="indexColumns" :data="indexData" style="width: 100%;"></Table>
                            </Row>
                        </Card>
                    </Col>
                </Row>
            </div>
        </TabPane>
    </Tabs>
</template>
<script>
  export default {
    data () {
      return {
        showModel: false,
        formItem: [
            /* tag: 标签类型    class: 标签类属性    style: 标签样式     text: 标签内容  model: 绑定属性     tab: 是否前置空格(相当与一个tab长度的空格) */
            // { type: 'header-col', content: [{ tag: 'small', class: '', style: '', text: '本年一月至', model: '' }, { tag: 'input', class: 'bg-blue', style: 'width: 45px;', text: '', model: '' }, { tag: 'small', class: '', style: '', text: '累计', model: '' }] },
            // { type: 'header-row', content: [{ tag: '', class: '', style: '', tab: true, text: '（4） 个人资本', model: '' }] },
            // { type: 'text-box', content: [{ tag: 'input', class: '', style: '', text: '', model: '' }, { tag: 'small', class: '', style: '', text: ' 万元 ', model: '' }] }

        ],
        indexColumns: [
            { title: '指标年度', key: 'ndzb', align: 'center' },
            { title: '注册资金', key: 'zczj', align: 'center' },
            { title: '资产总额', key: 'zcze', align: 'center' },
            { title: '负债总额', key: 'fzze', align: 'center' },
            { title: '营业收入', key: 'yysr', align: 'center' },
            { title: '利润总额', key: 'lrze', align: 'center' },
            { title: '操作', key: 'operation', align: 'center',
                /* 通过给 columns 数据的项，设置一个函数 render，可以自定义渲染当前列，包括渲染自定义组件，它基于 Vue 的 Render 函数。
render 函数传入两个参数，第一个是 h，第二个是对象，包含 row、column 和 index，分别指当前单元格数据，当前列数据，当前是第几行。 */
                render: (h, params) => {
                    return h('div', [
                        h('Button', {
                            props: {
                                type: 'primary',
                                size: 'small'
                            },
                            style: {
                                marginRight: '5px'
                            },
                            on: {
                                click: () => {
                                    console.log(params.row);
                                    this.$Notice.open({
                                        title: '你将要修改第'+ (params.index + 1) +'行数据！',
                                        desc: params.row.id,
                                        duration: 3
                                    });
                                }
                            }
                        }, '修改信息')
                    ]);
                }
            }
          ],
        indexData: []
      };
    },
    methods: {
      handleSubmit () {
        this.$ajax({
          method: 'post',
          url: '/api/drummer/8bd17859',
          data: this.formItem
        }).then(response=>{
          let _data=response.data;
          alert("hello," + _data.username);
        }).catch(function(err){
          this.$Message.error('保存失败');
        }.bind(this));

      },
      ok () {
          this.$Message.info("click ok");
      },
      cancel () {
          this.$Message.warning('click cancel');
      }
    },
    mounted () {
        /* 访问服务器文件，应该把 json文件放在最外层的static文件夹，这个文件夹是vue-cli内置服务器向外暴露的静态文件夹
         * 一定要用get的请求方式，post就会404 */
        this.$ajax.get('/static/unit-info/table_data.json').then(response => {
            this.indexData = response.data;
        })
    }
  };
</script>

