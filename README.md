# Función para crear un nuevo segmento del cuerpo de la serpiente
    global puntaje
    segment = turtle.Turtle()
    turtle.colormode(255) 
    segment.speed(0)
    segment.shape('square')
    segment.color(random.choice(colores))
    segment.penup()
    cuerpo.append(segment)
    puntaje += 1
    print_text()
def food_collision():
    # Función para verificar la colisión con la comida y generar nueva comida
    if cabeza.distance(comida) < 20:
        x = random.randint(-280, 280)
        y = random.randint(-280, 280)
        comida.goto(x, y)
        create_segment()
def move_body():
    # Función para mover el cuerpo de la serpiente
    total_segments = len(cuerpo)
    for segment in range(total_segments - 1, 0, -1):
        x = cuerpo[segment - 1].xcor()
        y = cuerpo[segment - 1].ycor()
        cuerpo[segment].goto(x, y)
    if total_segments > 0:
        x = cabeza.xcor()
        y = cabeza.ycor()
        cuerpo[0].goto(x, y)
def border_collision():# En-busca-del-amor1
juego del gusanito
