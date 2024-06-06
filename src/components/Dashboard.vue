<template>
    <div id="Dashboard" class="Dashboard">
        <h1>소속 동아리 회원 정보</h1>
        <!-- 스프레트시트 URL 입력 -->
        <input v-model="sheetUrl" placeholder="Enter Google Sheets URL" @change="fetchSheetData" />
        <!-- 링크 제출 시 나타는 테이블 -->
        <div v-if="sheetData.length">
            <table>
                <thead>
                    <tr>
                        <th v-for="(header, index) in sheetData[0]" :key="index">{{ header }}</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(row, rowIndex) in sheetData.slice(1)" :key="rowIndex">
                        <td v-for="(cell, cellIndex) in row" :key="cellIndex">{{ cell }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'Dashboard',
    data() {
        return {
            sheetUrl: '',
            sheetData: [],
        };
    },
    methods: {
        async fetchSheetData() {
            const sheetId = this.extractSheetId(this.sheetUrl);
            if (sheetId) {
                const apiKey = 'AIzaSyCgARDETVZFsr3mu58W7gQyKdCX0HP0SLI';  // 여기서 API 키를 입력하세요.
                const range = 'Sheet1!A1:D999'; // 필요한 범위를 지정하세요.
                const url = `https://sheets.googleapis.com/v4/spreadsheets/${sheetId}/values/${range}?key=${apiKey}`;
                try {
                    const response = await axios.get(url);
                    this.sheetData = response.data.values;
                } catch (error) {
                    console.error('Error fetching sheet data:', error);
                }
            }
        },
        extractSheetId(url) {
            const regex = /\/spreadsheets\/d\/([a-zA-Z0-9-_]+)/;
            const match = url.match(regex);
            return match ? match[1] : null;
        },
    },
};
</script>

<style>
.Dashboard{
    width: 886px;
    background: #fff;
    border-radius: 8px;
}

.Dashboard h1{
    text-align: center;
}

.Dashboard div{
    align-content: center;
}

.Dashboard input{
    width: 880px;
    margin: 30px 0px 30px 0px;
}

table {
    width: 886px;
    border-collapse: collapse;
    align-items: center;
}

th,
td {
    border: 1px solid #ccc;
    padding: 8px;
    text-align: left;
}

th {
    background-color: #f2f2f2;
}
</style>