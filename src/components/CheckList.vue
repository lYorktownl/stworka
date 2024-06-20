<template>
    <div class="main">
        <div class="progress-container">
            <svg class="progress-circle">
                <circle cx="50" cy="50" r="30" class="progress-bg" />
                <circle cx="50" cy="50" r="30" class="progress-bar" />
            </svg>
            <div class="progress-text">
                <span id="progress-text">0/7</span>
            </div>
        </div>
        <div class="text-content">
            <label>Чеклист</label>
            <h3 class="text-counter">Выполнено: 0 из 7 действий</h3>
            <p class="title">Следующее действие: Созвониться с клиентом до 23.05.24 12:00</p>
        </div>
        <button class="open-btn">Открыть чеклист</button>
    </div>
</template>
<script>
export default {
    setup () {
        return {}
    }
}
</script>
<style scoped>
/* :root {
    --progress-percentage: 10;  Устанавливаем процент заполнения вручную 
} */
.main {
    display: inline-flex;
    align-items: center;
    background-color: #3579F5;
    color: #ffff;
    border-radius: 10px;
    font-weight: 400;
}
.progress-container {
    position: relative;
    width: 100px;
    height: 100px;
}

.progress-circle {
    width: 100px;
    height: 100px;
    transform: rotate(-90deg);
}

.progress-circle circle {
    fill: none;
}

.progress-bg {
    stroke: rgba(255, 255, 255, 0.5);
    stroke-width: 1;
}

.progress-bar {
    stroke: white;
    stroke-width: 2;
    stroke-linecap: round;
    stroke-dasharray: 188.4; /* Длина окружности круга с радиусом 30 (2 * π * 30) */
    stroke-dashoffset: calc(188.4 - (188.4 * 2 / 100)); /* устанавливаем значени в процентах текущее 2 */
    transition: stroke-dashoffset 1s;
}

.progress-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 20px;
    text-anchor: middle;
}
.text-content {
    display: flex;
    flex-direction: column;
    margin-top: 12px;
    margin-bottom: 15px;
}

.text-counter {
    font-size: 15px;
    font-weight: 600;
    line-height: 20px;
    text-align: left;
    margin: 4px 0;
}

.title {
    font-size: 12px;
    line-height: 18px;
    text-align: left;
    margin: 0;
}
.open-btn {
    color: #4777ED;
    background-color: #F4F8FF;
    border-radius: 6px;
    font-size: 14px;
    line-height: 20px;
    text-align: left;
    border: none;
    padding: 10px 25px;
    margin: 26px 18px 25px 68px;
    cursor: pointer;
}
h1 {
    margin-top: 15px;
    font-size: 20px;
    font-weight: 400;
    line-height: 30px;
    text-align: center;

}
label {
    background-color: #2364DB;
    border-radius: 40px;
    width: 76px;
    height: 18px;
    font-size: 12px;
    line-height: 18px;
    text-align: center;
    padding: 0px 10px 0px 10px;

}
</style>
