# Contoh-website-less
Cara nya mudah 😁🤏🗿
import turtle
import time

# Setup
t = turtle.Turtle()
s = turtle.Screen()
s.bgcolor('#fff0f5')        # Latar pink lembut
t.pencolor('#ff69b4')       # Warna garis love
t.pensize(2)
t.speed(2)                  # Biar kelihatan prosesnya

# Fungsi gambar love
def draw_love(size):
    t.penup()
    t.goto(0, -size / 2)    # Posisi agar love tetap di tengah
    t.setheading(0)
    t.pendown()
    
    t.begin_fill()
    t.left(140)
    t.forward(size)
    t.circle(-size/2, 200)
    t.left(120)
    t.circle(-size/2, 200)
    t.forward(size)
    t.right(140)
    t.end_fill()

# Gambar love berlapis-lapis
t.fillcolor('')  # Tanpa isi warna, biar kayak kabel
for i in range(220):
    draw_love(20 + i * 20)  # Ukuran makin besar
    time.sleep(0.1)         # Delay biar keren efeknya

# Klik untuk keluar
s.exitonclick()
