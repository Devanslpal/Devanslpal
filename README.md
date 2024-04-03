- 👋 Hi, I’m @Devanslpal
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Devanslpal/Devanslpal is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->import tkinter as tk
from tkinter import messagebox

def show_color():
    color_name = color_entry.get().lower()
    try:
        color = colors[color_name]
        color_canvas.config(bg=color)
    except KeyError:
        messagebox.showerror("Error", "Invalid color name!")

# Dictionary mapping color names to hexadecimal color codes
colors = {
    "red": "#FF0000",
    "green": "#00FF00",
    "blue": "#0000FF",
    # Add more colors as needed
}

root = tk.Tk()
root.title("Color Viewer")

color_label = tk.Label(root, text="Enter a color name:")
color_label.pack()

color_entry = tk.Entry(root)
color_entry.pack()

show_button = tk.Button(root, text="Show Color", command=show_color)
show_button.pack()

color_canvas = tk.Canvas(root, width=100, height=50)
color_canvas.pack()

root.mainloop()

