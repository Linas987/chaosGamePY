import random
import math

class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def midpoint_to(self, a):
        return Point.midpoint(self, a)

    @staticmethod
    def midpoint(a, b):
        return Point(
            round((a.x + b.x) / 2),
            round((a.y + b.y) / 2)
        )

def pixel(point, index):
    print(point.x, point.y)

A = Point(200, 85)
B = Point(66, 315)
C = Point(333, 315)

vertices = [A, B, C]

def pick_vertex():
    return vertices[random.randint(0, len(vertices) - 1)]

def get_new_point(old_point):
    return old_point.midpoint_to(pick_vertex())

def play_game(iterations):
    start_vertex = pick_vertex()
    current_dot = start_vertex
    for i in range(iterations):
        current_dot = get_new_point(current_dot)
        pixel(current_dot, i)

def place_number(x):
    play_game(x)
