<style scoped>
    #finance-info {
        padding: 5px;
        font-size: 12px;
    }
    .header {
        background: #DAE4ED;
        margin: 0 5px;
        padding: 5px 0;
        text-align: center;
    }
</style>

<template>
    <div id="finance-info">
        <!-- 财务信息 -->
        <Form :model="formItem" :label-width="80" class="">
            <Row>
                <Col span="7" class-name="header">职工人数</Col>
                <Col span="7" class-name="header">上年度</Col>
                <Col span="7" class-name="header">本年度</Col>
            </Row>
            <Row>
                <Col span="7">职工人数</Col>
                <Col span="7" push="0"><Input v-model="formItem.input"></Input></Col>
                <Col span="7" push="0"><Input v-model="formItem.input"></Input></Col>
            </Row><!--
            <FormItem label="Input">
                <Input v-model="formItem.input" placeholder=""></Input>
            </FormItem>
            <FormItem label="Select">
                <Select v-model="formItem.select">
                    <Option value="beijing">New York</Option>
                    <Option value="shanghai">London</Option>
                    <Option value="shenzhen">Sydney</Option>
                </Select>
            </FormItem>
            <FormItem label="DatePicker">
                <Row>
                    <Col span="11">
                        <DatePicker type="date" placeholder="Select date" v-model="formItem.date"></DatePicker>
                    </Col>
                    <Col span="2" style="text-align: center">-</Col>
                    <Col span="11">
                        <TimePicker type="time" placeholder="Select time" v-model="formItem.time"></TimePicker>
                    </Col>
                </Row>
            </FormItem>
            <FormItem label="Radio">
                <RadioGroup v-model="formItem.radio">
                    <Radio label="male">Male</Radio>
                    <Radio label="female">Female</Radio>
                </RadioGroup>
            </FormItem>
            <FormItem label="Checkbox">
                <CheckboxGroup v-model="formItem.checkbox">
                    <Checkbox label="Eat"></Checkbox>
                    <Checkbox label="Sleep"></Checkbox>
                    <Checkbox label="Run"></Checkbox>
                    <Checkbox label="Movie"></Checkbox>
                </CheckboxGroup>
            </FormItem>
            <FormItem label="Switch">
                <i-switch v-model="formItem.switch" size="large">
                    <span slot="open">On</span>
                    <span slot="close">Off</span>
                </i-switch>
            </FormItem>
            <FormItem label="Slider">
                <Slider v-model="formItem.slider" range></Slider>
            </FormItem>
            <FormItem label="Text">
                <Input v-model="formItem.textarea" type="textarea" :autosize="{minRows: 2,maxRows: 5}" placeholder="Enter something..."></Input>
            </FormItem>
            <FormItem>
                <Button type="primary">Submit</Button>
                <Button type="ghost" style="margin-left: 8px">Cancel</Button>
            </FormItem>-->
        </Form>
        <!-- 年度财务指标基本数据 -->

    </div>
</template>

<script>
    export default {
        data () {
            return {
                formItem: {
                    input: '',
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
        name: "finance-info",
        components: {}
    }
</script>
