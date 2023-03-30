<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>烟花</title>
	<style>
		canvas {
			background-color: black;
			display: block;
			margin: 0 auto;
			width: 100%;
			height: 100%;
			position: absolute;
			top: 0;
			left: 0;
			z-index: -1;
		}
	</style>
</head>
<body>
	<canvas id="canvas"></canvas>
	<script src="fireworks.js"></script>
	// 创建烟花对象
function Firework(x, y, vx, vy, ax, ay, color, size, lifespan) {
	this.x = x; // 烟花的 x 坐标
	this.y = y; // 烟花的 y 坐标
	this.vx = vx; // 烟花的 x 轴速度
	this.vy = vy; // 烟花的 y 轴速度
	this.ax = ax; // 烟花的 x 轴加速度
	this.ay = ay; // 烟花的 y 轴加速度
	this.color = color; // 烟花的颜色
	this.size = size; // 烟花的大小
	this.lifespan = lifespan; // 烟花的寿命
}

// 更新烟花位置和速度
Firework.prototype.update = function(dt) {
	this.vx += this.ax * dt;
	this.vy += this.ay * dt;
	this.x += this.vx * dt;
	this.y += this.vy * dt;
	this.lifespan -= dt;
};

// 绘制烟花
Firework.prototype.draw = function(ctx) {
	ctx.beginPath();
	ctx.arc(this.x, this.y, this.size, 0, 2 * Math.PI);
	ctx.fillStyle = this.color;
	ctx.fill();
};

// 创建烟花爆炸效果
function createExplosion(x, y, color) {
	for (var i = 0; i < 50; i++) {
		var angle = Math.random() * 2 * Math.PI;
		var speed = Math.random() * 300 + 100;
		var vx = speed * Math.cos(angle);
		var vy = speed * Math.sin(angle);
		var ax = 0;
		var ay = 1000;
		var size = Math.random() * 5 + 5;
		var lifespan = Math.random() * 1 + 1;
		var firework = new Firework(x, y, vx, vy, ax, ay, color, size, lifespan);
		fireworks.push(firework);
	}
}

// 绘制烟花画面
function drawFireworks(dt) {
	// 清空画布
	ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
	ctx.fillRect(0, 

</body>
</html>
