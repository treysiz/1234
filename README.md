import turtle
import random

# 设置画布大小
turtle.setup(width=800, height=600)

# 定义烟花函数
def fireworks():
    # 随机设置颜色和大小
    turtle.color(random.choice(['red', 'orange', 'yellow', 'green', 'blue', 'purple']))
    size = random.randint(10, 20)

    # 绘制烟花爆炸的圆形
    turtle.begin_fill()
    turtle.circle(size)
    turtle.end_fill()

    # 绘制烟花的火花
    for i in range(30):
        turtle.penup()
        turtle.goto(0, size)
        turtle.setheading(0)
        turtle.right(i * 12)
        turtle.pendown()
        turtle.forward(random.randint(10, 30))
        turtle.dot(random.randint(5, 10))

    # 隐藏海龟画笔，清空画布
    turtle.hideturtle()
    turtle.clear()

# 循环绘制烟花
while True:
    fireworks()
