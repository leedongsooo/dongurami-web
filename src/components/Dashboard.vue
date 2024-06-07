<template>
    <div id="Dashboard" class="Dashboard">
        <p>소속 동아리 회원 정보</p>
        <!-- 스프레트시트 URL 입력 -->
        <input v-model="sheetUrl" placeholder="Enter Google Sheets URL" @change="fetchSheetData" />
        <!-- 링크 제출 시 나타는 테이블 -->
        <div v-if="sheetData.length" class="memberlist">
            <table>
                <tbody>
                    <tr v-for="(row, rowIndex) in sheetData" :key="rowIndex">
                        <td v-for="(cell, cellIndex) in row" :key="cellIndex">{{ cell }}</td>
                        <td class="Expulsion" onclick="Expulsion()">퇴출</td>
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
    align-items: center;
    align-content: center;
    text-align: center;
}

.Dashboard p {
    color: #000;
    font-family: Pretendard;
    font-size: 18px;
    font-style: normal;
    font-weight: 600;
    line-height: 18px; /* 100% */
    letter-spacing: -0.9px;
}

.Dashboard h1{
    text-align: center;
}

.Dashboard div{
    align-items: center;
}

.Dashboard input{
    width: 880px;
    margin: 30px 0px 30px 0px;
    align-content: center;
}

table {
    width: 734px;
    border-spacing: 0px 30px;
}

tr{
    background-color: #F0F2F5;
    border-radius: 8px;
}

th,
td {
    padding: 8px;
    text-align: left;
    height: 46px;
}

td:first-child,
th:first-child{
    border-radius: 2px 0px 0px 2px;
    padding-left: 20px;
}

td:last-child,
th:last-child{
    border-radius: 0px 2px 2px 0px;
    padding-right: 20px;
}

.Expulsion{
    background: #BF6F6F;
}

</style>