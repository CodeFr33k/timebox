<template>
    <Day 
        :records="records"
        :day="day"
    ></Day>
</template>

<script lang="ts">
import Record from 'caml-js/Record';
import Day from './Day.vue';
import {
    Component,
    Vue,
} from 'vue-property-decorator';

@Component({
    components: { Day },
})
export default class extends Vue {
    records: Record[] = []; 
    day = 1; 
    created() {
        const record = new Record;
        record.userData.push({
            key: 'day label',
            value: '1',
        });
        this.records.push(record);
    }
};
</script>

