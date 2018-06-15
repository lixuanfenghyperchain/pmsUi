<template>
    <div id="finance-form">
        <table class="table-first">
            <thead>
                <tr>
                    <th> 职工人数 </th> <th> 上年度 </th> <th> 本年度 </th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td> 1.参加养老保险职工人数 </td> <td> <input class="center" type="text" /> 人 </td> <td> <input class="center" type="text" /> 人 </td>
                </tr>
                <tr>
                    <td> 2.财务人员 </td> <td> <input class="center" type="text" /> 人 </td> <td> <input class="center" type="text" /> 人 </td>
                </tr>
                <tr>
                    <td> 其中：中级以上财务人员 </td> <td> <input class="center" type="text" /> 人 </td> <td> <input class="center" type="text" /> 人 </td>
                </tr>
            </tbody>
        </table>
        <table class="table table-bordered table-hover">
            <thead>
                <tr class="table-info">
                    <td>姓名</td> <td>性别</td> <td>岗位</td>
                </tr>
            </thead>
            <tbody>
                <tr v-for="row in table_data">
                    <td>{{row.name}}</td> <td><input type="text" v-model="row.sex" /></td> <td><input type="text" v-model="row.work" /></td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    name: "finance-form",
    components: {

    },
    data () {
        return {
            table_data: [
                { name: 'Aresn', sex: '男', work: '前端开发' },
                { name: 'Lison', sex: '男', work: '前端开发' },
                { name: 'lisa', sex: '女', work: '程序员鼓励师' }
            ]
        }
    }
}
</script>

<style scoped>
    .table-first {
        width: 800px;
    }
    .table-first th {
        background: #DAE4ED;
        text-align: center;
    }
    .center {
        width: 40%;
        margin: 2px 18px 2px 25%;
    }
</style>