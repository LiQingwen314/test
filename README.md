```vue
<template>
    <div class="test">
        <el-table :data="tableDataOfTabPane1.data" :border="true" size="small"  :row-class-name="handleTableCellClass2">
            <el-table-column prop="date" label="Date"/>
            <el-table-column prop="name" label="Name"/>
            <el-table-column prop="address" label="Address" />
        </el-table>
    </div>
</template>
<script lang="ts">
import {defineComponent, onMounted, ref, reactive, getCurrentInstance, computed} from 'vue'
export default defineComponent({
    setup(){
        let tableDataOfTabPane1 = reactive({
            data:[{
                date: '2016-05-03',
                name: 'Tom',
                address: 'No. 189, Grove St, Los Angeles',
            },
            {
                date: '2016-05-02',
                name: 'Tom',
                address: 'No. 189, Grove St, Los Angeles',
            },
            {
                date: '2016-05-04',
                name: 'Tom',
                address: 'No. 189, Grove St, Los Angeles',
            },
            {
                date: '2016-05-01',
                name: 'Tom',
                address: 'No. 189, Grove St, Los Angeles',
            }]})
        const handleTableCellClass2 = ({row})=>{
            console.log(888)
            console.log(row)
        }
        return{
            tableDataOfTabPane1,handleTableCellClass2
        }
    }
})
</script>
```
