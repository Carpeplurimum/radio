const rdsDisplay = document.getElementById('rds-display');
const stationInfo = document.getElementById('station-info');
const powerBtn = document.getElementById('power-btn');
const tuneUpBtn = document.getElementById('tune-up-btn');
const tuneDownBtn = document.getElementById('tune-down-btn');
const colorBtn = document.getElementById('color-btn');

const stations = [
    { frequency: '98.5', name: 'Estación 1' },
    { frequency: '101.2', name: 'Estación 2' },
    { frequency: '104.7', name: 'Estación 3' },
    { frequency: '107.3', name: 'Estación 4' }
];

let currentStationIndex = 0;
let isPoweredOn = false;

function updateRDS() {
    if (isPoweredOn) {
        stationInfo.textContent = `FM ${stations[currentStationIndex].frequency} - ${stations[currentStationIndex].name}`;
    } else {
        stationInfo.textContent = 'Apagado';
    }
}

powerBtn.addEventListener('click', () => {
    isPoweredOn = !isPoweredOn;
    updateRDS();
});

tuneUpBtn.addEventListener('click', () => {
    if (isPoweredOn) {
        currentStationIndex = (currentStationIndex + 1) % stations.length;
        updateRDS();
    }
});

tuneDownBtn.addEventListener('click', () => {
    if (isPoweredOn) {
        currentStationIndex = (currentStationIndex - 1 + stations.length) % stations.length;
        updateRDS();
    }
});

colorBtn.addEventListener('click', () => {
    const colors = ['#0f0', '#00f', '#f00', '#ff0', '#0ff', '#f0f'];
    const randomColor = colors[Math.floor(Math.random() * colors.length)];
    rdsDisplay.style.color = randomColor;
});

updateRDS();
