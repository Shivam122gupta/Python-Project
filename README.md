# Python-Project
Fake News Generator
import tkinter as tk
import random

list_1 = [
    "Shahrukh Khan",
    "Virat Kholi",
    "Nirmala Sithraman",
    "A Mumbai Cat",
    "A Group of Monkeys",
    "Prime Minister Modi"
]

list_2 = [
    "launches",
    "cancels",
    "dances with",
    "eats",
    "declares war on",
    "orders"
]

list_3 = [
    "at Red Fort",
    "in a Mumbai local train",
    "a plate of samosa",
    "at Ganga Ghat",
    "during an IPL match"
]


def generate_sentence():
    subject = random.choice(list_1)
    verb = random.choice(list_2)
    obj = random.choice(list_3)
    result = f"{subject} {verb} {obj}."
    label_result.config(text=result)


root = tk.Tk()
root.title("Funny Sentence Generator")
root.geometry("500x200")
root.config(bg="lightyellow")

label_title = tk.Label(root, text="Click to Generate a Funny Sentence", font=("Arial", 14, "bold"), bg="lightyellow")
label_title.pack(pady=10)

btn_generate = tk.Button(root, text="Generate Sentence", command=generate_sentence, font=("Arial", 12), bg="orange")
btn_generate.pack(pady=10)

label_result = tk.Label(root, text="", font=("Arial", 12), wraplength=400, bg="lightyellow")
label_result.pack(pady=10)

root.mainloop()
