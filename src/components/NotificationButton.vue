<template>
    <div class="notification-button vibration">
        <span>새로운 알림</span>
        <div class="icon-wrapper">
            <i class="icon alram"></i>
            <span class="red-dot"></span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'NotificationButton'
};
</script>

<style scoped>
.notification-button {
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 16px;
    background: #353549;
    box-shadow: 0px 0px 4px 0px rgba(0, 0, 0, 0.08);
    color: #fff;
    padding: 10px 20px;
    border-radius: 20px;
    font-size: 16px;
    font-style: normal;
    width: 202px;
    height: 45px;
    cursor: pointer;
    /* Adjust the width as necessary */
}

.icon-wrapper {
    position: relative;
    display: flex;
    align-items: center;
    margin: 0px 0px 0px 10px;
}

.alram {
    width: 24px;
    height: 24px;
    background: url('@/assets/alram.svg') no-repeat center center;
    background-size: contain;
}

.red-dot {
    width: 6px;
    height: 6px;
    background-color: red;
    border-radius: 50%;
    position: absolute;
    top: 0;
    right: -3px;
}

.notification-button.vibration:hover{
    animation: vibration .1s infinite;
}

@keyframes vibration {
    from {
        transform: rotate(1deg);
    }
    to {
        transform: rotate(-1deg);
    }
}
</style>