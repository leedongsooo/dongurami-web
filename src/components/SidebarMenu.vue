<template>
    <div class="sidebar">
        <!-- <div class="sidebar-header">
            <img src="@/assets/dongurami_logo.png" alt="Dongurami Logo" class="logo" />
            <h1 class="title">동구라미</h1>
        </div> -->
        <div class="profile">
            <img src="@/assets/flag_logo.jpeg" alt="FLAG Logo" class="profile-img" />
            <div class="profile-info">
                <h2>FLAG</h2>
                <p>학술</p>
            </div>
        </div>
        <nav>
            <ul>
                <li class="active">
                    <i class="icon home"></i>
                    <p>홈 (회원관리)</p>
                </li>
                <li>
                    <i class="icon mail"></i>
                    <p>동아리 소개/모집</p>
                </li>
                <li>
                    <i class="icon clipboard"></i>
                    <p>공지사항</p>
                </li>
            </ul>
        </nav>
        <div class="empty"></div>
        <div class="line1"></div>
        <div class="footer">
            <a href="#">이용약관</a>
            <div class="line2"></div>
            <a href="#">로그아웃</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SidebarMenu'
};

</script>

<style scoped>
@import url('https://webfontworld.github.io/goodchoice/Jalnan.css');

.sidebar {
    width: 202px;
    height: 600px;
    color: #000;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    box-sizing: border-box;
    border-radius: 16px;
}

.sidebar-header {
    display: flex;
    align-items: center;
    margin: 35px 0px 0px 25px;
    height: 35px;
}

.logo {
    width: 17px;
    height: 17px;
    padding: 5px;
    transform: scaleX(-1);
}

.title {
    color: #FFC700;
    font-family: "Jalnan";
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 14px; /* 100% */
}

.profile {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
}

.profile-img {
    width: 60px;
    height: 60px;
    flex-shrink: 0;
    border-radius: 50%;
    margin: 35px 0px 15px 25px;
    box-shadow: 0px 0px 4px 0px rgba(0, 0, 0, 0.25);
}

.profile-info h2 {
    color: #000;
    font-family: Pretendard;
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 10px; /* 100% */
    letter-spacing: -0.4px;
    margin: 35px 0px 12px 12px;
}

.profile-info p {
    color: #000;
    font-family: Pretendard;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 6px; /* 100% */
    letter-spacing: -0.3px;
    margin: 0px 0px 12px 12px;
}

nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

nav li {
    display: flex;
    align-items: center;
    align-content: center;
    cursor: pointer;
    margin: 0px 0px 0px 0px;
    height: 55px;
}

li > p{
    font-size: 15px;
    font-family: Pretendard;
    width: 135px;
}

nav li:hover {
    background-color: #fff;
}

nav .icon {
    width: 20px;
    height: 20px;
    margin: 0px 10px 3.5px 30px;
}

.home {
    background: url('@/assets/home.svg') no-repeat center center;
}

.mail {
    background: url('@/assets/mail.svg') no-repeat center center;
}

.clipboard {
    background: url('@/assets/clipboard.svg') no-repeat center center;
}

.empty{
    height: 200px;
}

.line1{
    width: 100%;
    height: 1px;
    background-color: #686868;
}

.footer {
    display: flex;
    justify-content: center;
    height: 60px;
    font-size: 12px;
    align-items: center;
}

.footer a {
    color: #686868;
    text-decoration: none;
}

.line2 {
    width: 1px;
    height: 13px;
    background-color: #686868;
    margin: 0px 20px 0px 20px;
}

.footer a:hover {
    text-decoration: underline;
}
</style>