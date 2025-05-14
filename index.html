import tkinter as tk
from tkinter import messagebox, ttk
import json
import os
import threading
import time
from datetime import datetime
import matplotlib.pyplot as plt

# Archivo para guardar datos
ARCHIVO = "habitos.json"
HISTORIAL = "historial.json"

# Cargar datos desde archivos
def cargar_datos():
    if os.path.exists(ARCHIVO):
        with open(ARCHIVO, "r") as file:
            return json.load(file)
    return {"habitos": [], "recordatorios": []}

def cargar_historial():
    if os.path.exists(HISTORIAL):
        with open(HISTORIAL, "r") as file:
            return json.load(file)
    return []

# Guardar datos
def guardar_datos():
    with open(ARCHIVO, "w") as file:
        json.dump(datos, file)

def guardar_historial():
    with open(HISTORIAL, "w") as file:
        json.dump(historial, file)

# Mostrar notificaciones
def verificar_recordatorios():
    while True:
        ahora = datetime.now().strftime("%H:%M")
        for recordatorio in datos["recordatorios"]:
            if recordatorio["hora"] == ahora:
                messagebox.showinfo("Recordatorio", f"¡Es hora de '{recordatorio['habito']}'!")
        time.sleep(60)

# Agregar hábito
def agregar_habito():
    habito = entrada_habito.get()
    if habito:
        datos["habitos"].append({"nombre": habito, "completado": False})
        entrada_habito.delete(0, tk.END)
        actualizar_lista()
        guardar_datos()

# Completar hábito
def completar_habito():
    seleccion = lista_habitos.curselection()
    if seleccion:
        indice = seleccion[0]
        habito = datos["habitos"][indice]
        habito["completado"] = not habito["completado"]
        if habito["completado"]:
            historial.append({
                "nombre": habito["nombre"],
                "fecha": datetime.now().strftime("%Y-%m-%d %H:%M:%S")
            })
            guardar_historial()
        actualizar_lista()
        actualizar_estadisticas()
        guardar_datos()

# Mostrar historial
def mostrar_historial():
    historial_window = tk.Toplevel(root)
    historial_window.title("Historial de Hábitos")
    historial_window.geometry("400x300")

    lista_historial = tk.Listbox(historial_window, width=50, height=15)
    lista_historial.pack(pady=10)

    for h in historial:
        lista_historial.insert(tk.END, f"{h['nombre']} - {h['fecha']}")

# Eliminar hábito
def eliminar_habito():
    seleccion = lista_habitos.curselection()
    if seleccion:
        indice = seleccion[0]
        del datos["habitos"][indice]
        actualizar_lista()
        actualizar_estadisticas()
        guardar_datos()

# Agregar recordatorio
def agregar_recordatorio():
    habito = entrada_habito.get()
    hora = entrada_hora.get()
    if habito and hora:
        datos["recordatorios"].append({"habito": habito, "hora": hora})
        entrada_habito.delete(0, tk.END)
        entrada_hora.delete(0, tk.END)
        actualizar_lista()
        guardar_datos()

# Eliminar recordatorio
def eliminar_recordatorio():
    seleccion = lista_recordatorios.curselection()
    if seleccion:
        indice = seleccion[0]
        del datos["recordatorios"][indice]
        actualizar_lista()
        guardar_datos()

# Mostrar lista de hábitos y recordatorios
def actualizar_lista():
    lista_habitos.delete(0, tk.END)
    lista_recordatorios.delete(0, tk.END)

    for habito in datos["habitos"]:
        estado = "✔" if habito["completado"] else "✘"
        lista_habitos.insert(tk.END, f"{estado} {habito['nombre']}")

    for recordatorio in datos["recordatorios"]:
        lista_recordatorios.insert(tk.END, f"{recordatorio['habito']} - {recordatorio['hora']}")

# Mostrar estadísticas de progreso
def actualizar_estadisticas():
    total = len(datos["habitos"])
    completados = sum(1 for h in datos["habitos"] if h["completado"])
    if total > 0:
        porcentaje = (completados / total) * 100
        etiqueta_estadisticas.config(text=f"Completados: {completados}/{total} ({porcentaje:.1f}%)")
    else:
        etiqueta_estadisticas.config(text="Sin datos")

# Mostrar gráfico de progreso
def mostrar_grafico():
    total = len(datos["habitos"])
    completados = sum(1 for h in datos["habitos"] if h["completado"])

    if total > 0:
        etiquetas = ["Completados", "Pendientes"]
        valores = [completados, total - completados]
        colores = ["#4CAF50", "#F44336"]

        plt.figure(figsize=(5, 5))
        plt.pie(valores, labels=etiquetas, colors=colores, autopct="%.1f%%")
        plt.title("Progreso de Hábitos")
        plt.show()

# Crear ventana
root = tk.Tk()
root.title("Gestor de Hábitos Mejorado")
root.geometry("400x550")

# Campos de entrada
entrada_habito = tk.Entry(root, width=30)
entrada_habito.pack(pady=5)
entrada_hora = tk.Entry(root, width=30)
entrada_hora.pack(pady=5)

# Botones
tk.Button(root, text="Agregar Hábito", command=agregar_habito).pack()
tk.Button(root, text="Completar Hábito", command=completar_habito).pack()
tk.Button(root, text="Eliminar Hábito", command=eliminar_habito).pack()
tk.Button(root, text="Agregar Recordatorio", command=agregar_recordatorio).pack()
tk.Button(root, text="Eliminar Recordatorio", command=eliminar_recordatorio).pack()
tk.Button(root, text="Mostrar Historial", command=mostrar_historial).pack()
tk.Button(root, text="Mostrar Gráfico", command=mostrar_grafico).pack()

# Listas
lista_habitos = tk.Listbox(root, width=40, height=6)
lista_habitos.pack()
lista_recordatorios = tk.Listbox(root, width=40, height=4)
lista_recordatorios.pack()

# Estadísticas
etiqueta_estadisticas = tk.Label(root, text="", font=("Arial", 12))
etiqueta_estadisticas.pack()

# Cargar datos
datos = cargar_datos()
historial = cargar_historial()
actualizar_lista()
actualizar_estadisticas()

# Hilo para notificaciones
verificador = threading.Thread(target=verificar_recordatorios, daemon=True)
verificador.start()

# Ejecutar
root.mainloop()
import tkinter as tk
from tkinter import messagebox, ttk
import json
import os
import threading
import time
from datetime import datetime
import matplotlib.pyplot as plt

# Archivo para guardar datos
ARCHIVO = "habitos.json"
HISTORIAL = "historial.json"

# Cargar datos desde archivos
def cargar_datos():
    if os.path.exists(ARCHIVO):
        with open(ARCHIVO, "r") as file:
            return json.load(file)
    return {"habitos": [], "recordatorios": []}

def cargar_historial():
    if os.path.exists(HISTORIAL):
        with open(HISTORIAL, "r") as file:
            return json.load(file)
    return []

# Guardar datos
def guardar_datos():
    with open(ARCHIVO, "w") as file:
        json.dump(datos, file)

def guardar_historial():
    with open(HISTORIAL, "w") as file:
        json.dump(historial, file)

# Mostrar notificaciones
def verificar_recordatorios():
    while True:
        ahora = datetime.now().strftime("%H:%M")
        for recordatorio in datos["recordatorios"]:
            if recordatorio["hora"] == ahora:
                messagebox.showinfo("Recordatorio", f"¡Es hora de '{recordatorio['habito']}'!")
        time.sleep(60)

# Agregar hábito
def agregar_habito():
    habito = entrada_habito.get()
    if habito:
        datos["habitos"].append({"nombre": habito, "completado": False})
        entrada_habito.delete(0, tk.END)
        actualizar_lista()
        guardar_datos()

# Completar hábito
def completar_habito():
    seleccion = lista_habitos.curselection()
    if seleccion:
        indice = seleccion[0]
        habito = datos["habitos"][indice]
        habito["completado"] = not habito["completado"]
        if habito["completado"]:
            historial.append({
                "nombre": habito["nombre"],
                "fecha": datetime.now().strftime("%Y-%m-%d %H:%M:%S")
            })
            guardar_historial()
        actualizar_lista()
        actualizar_estadisticas()
        guardar_datos()

# Mostrar historial
def mostrar_historial():
    historial_window = tk.Toplevel(root)
    historial_window.title("Historial de Hábitos")
    historial_window.geometry("400x300")

    lista_historial = tk.Listbox(historial_window, width=50, height=15)
    lista_historial.pack(pady=10)

    for h in historial:
        lista_historial.insert(tk.END, f"{h['nombre']} - {h['fecha']}")

# Eliminar hábito
def eliminar_habito():
    seleccion = lista_habitos.curselection()
    if seleccion:
        indice = seleccion[0]
        del datos["habitos"][indice]
        actualizar_lista()
        actualizar_estadisticas()
        guardar_datos()

# Agregar recordatorio
def agregar_recordatorio():
    habito = entrada_habito.get()
    hora = entrada_hora.get()
    if habito and hora:
        datos["recordatorios"].append({"habito": habito, "hora": hora})
        entrada_habito.delete(0, tk.END)
        entrada_hora.delete(0, tk.END)
        actualizar_lista()
        guardar_datos()

# Eliminar recordatorio
def eliminar_recordatorio():
    seleccion = lista_recordatorios.curselection()
    if seleccion:
        indice = seleccion[0]
        del datos["recordatorios"][indice]
        actualizar_lista()
        guardar_datos()

# Mostrar lista de hábitos y recordatorios
def actualizar_lista():
    lista_habitos.delete(0, tk.END)
    lista_recordatorios.delete(0, tk.END)

    for habito in datos["habitos"]:
        estado = "✔" if habito["completado"] else "✘"
        lista_habitos.insert(tk.END, f"{estado} {habito['nombre']}")

    for recordatorio in datos["recordatorios"]:
        lista_recordatorios.insert(tk.END, f"{recordatorio['habito']} - {recordatorio['hora']}")

# Mostrar estadísticas de progreso
def actualizar_estadisticas():
    total = len(datos["habitos"])
    completados = sum(1 for h in datos["habitos"] if h["completado"])
    if total > 0:
        porcentaje = (completados / total) * 100
        etiqueta_estadisticas.config(text=f"Completados: {completados}/{total} ({porcentaje:.1f}%)")
    else:
        etiqueta_estadisticas.config(text="Sin datos")

# Mostrar gráfico de progreso
def mostrar_grafico():
    total = len(datos["habitos"])
    completados = sum(1 for h in datos["habitos"] if h["completado"])

    if total > 0:
        etiquetas = ["Completados", "Pendientes"]
        valores = [completados, total - completados]
        colores = ["#4CAF50", "#F44336"]

        plt.figure(figsize=(5, 5))
        plt.pie(valores, labels=etiquetas, colors=colores, autopct="%.1f%%")
        plt.title("Progreso de Hábitos")
        plt.show()

# Crear ventana
root = tk.Tk()
root.title("Gestor de Hábitos Mejorado")
root.geometry("400x550")

# Campos de entrada
entrada_habito = tk.Entry(root, width=30)
entrada_habito.pack(pady=5)
entrada_hora = tk.Entry(root, width=30)
entrada_hora.pack(pady=5)

# Botones
tk.Button(root, text="Agregar Hábito", command=agregar_habito).pack()
tk.Button(root, text="Completar Hábito", command=completar_habito).pack()
tk.Button(root, text="Eliminar Hábito", command=eliminar_habito).pack()
tk.Button(root, text="Agregar Recordatorio", command=agregar_recordatorio).pack()
tk.Button(root, text="Eliminar Recordatorio", command=eliminar_recordatorio).pack()
tk.Button(root, text="Mostrar Historial", command=mostrar_historial).pack()
tk.Button(root, text="Mostrar Gráfico", command=mostrar_grafico).pack()

# Listas
lista_habitos = tk.Listbox(root, width=40, height=6)
lista_habitos.pack()
lista_recordatorios = tk.Listbox(root, width=40, height=4)
lista_recordatorios.pack()

# Estadísticas
etiqueta_estadisticas = tk.Label(root, text="", font=("Arial", 12))
etiqueta_estadisticas.pack()

# Cargar datos
datos = cargar_datos()
historial = cargar_historial()
actualizar_lista()
actualizar_estadisticas()

# Hilo para notificaciones
verificador = threading.Thread(target=verificar_recordatorios, daemon=True)
verificador.start()

# Ejecutar
root.mainloop()
import tkinter as tk
from tkinter import messagebox, ttk
import json
import os
import threading
import time
from datetime import datetime
import matplotlib.pyplot as plt

# Archivo para guardar datos
ARCHIVO = "habitos.json"
HISTORIAL = "historial.json"

# Cargar datos desde archivos
def cargar_datos():
    if os.path.exists(ARCHIVO):
        with open(ARCHIVO, "r") as file:
            return json.load(file)
    return {"habitos": [], "recordatorios": []}

def cargar_historial():
    if os.path.exists(HISTORIAL):
        with open(HISTORIAL, "r") as file:
            return json.load(file)
    return []

# Guardar datos
def guardar_datos():
    with open(ARCHIVO, "w") as file:
        json.dump(datos, file)

def guardar_historial():
    with open(HISTORIAL, "w") as file:
        json.dump(historial, file)

# Mostrar notificaciones
def verificar_recordatorios():
    while True:
        ahora = datetime.now().strftime("%H:%M")
        for recordatorio in datos["recordatorios"]:
            if recordatorio["hora"] == ahora:
                messagebox.showinfo("Recordatorio", f"¡Es hora de '{recordatorio['habito']}'!")
        time.sleep(60)

# Agregar hábito
def agregar_habito():
    habito = entrada_habito.get()
    if habito:
        datos["habitos"].append({"nombre": habito, "completado": False})
        entrada_habito.delete(0, tk.END)
        actualizar_lista()
        guardar_datos()

# Completar hábito
def completar_habito():
    seleccion = lista_habitos.curselection()
    if seleccion:
        indice = seleccion[0]
        habito = datos["habitos"][indice]
        habito["completado"] = not habito["completado"]
        if habito["completado"]:
            historial.append({
                "nombre": habito["nombre"],
                "fecha": datetime.now().strftime("%Y-%m-%d %H:%M:%S")
            })
            guardar_historial()
        actualizar_lista()
        actualizar_estadisticas()
        guardar_datos()

# Mostrar historial
def mostrar_historial():
    historial_window = tk.Toplevel(root)
    historial_window.title("Historial de Hábitos")
    historial_window.geometry("400x300")

    lista_historial = tk.Listbox(historial_window, width=50, height=15)
    lista_historial.pack(pady=10)

    for h in historial:
        lista_historial.insert(tk.END, f"{h['nombre']} - {h['fecha']}")

# Eliminar hábito
def eliminar_habito():
    seleccion = lista_habitos.curselection()
    if seleccion:
        indice = seleccion[0]
        del datos["habitos"][indice]
        actualizar_lista()
        actualizar_estadisticas()
        guardar_datos()

# Agregar recordatorio
def agregar_recordatorio():
    habito = entrada_habito.get()
    hora = entrada_hora.get()
    if habito and hora:
        datos["recordatorios"].append({"habito": habito, "hora": hora})
        entrada_habito.delete(0, tk.END)
        entrada_hora.delete(0, tk.END)
        actualizar_lista()
        guardar_datos()

# Eliminar recordatorio
def eliminar_recordatorio():
    seleccion = lista_recordatorios.curselection()
    if seleccion:
        indice = seleccion[0]
        del datos["recordatorios"][indice]
        actualizar_lista()
        guardar_datos()

# Mostrar lista de hábitos y recordatorios
def actualizar_lista():
    lista_habitos.delete(0, tk.END)
    lista_recordatorios.delete(0, tk.END)

    for habito in datos["habitos"]:
        estado = "✔" if habito["completado"] else "✘"
        lista_habitos.insert(tk.END, f"{estado} {habito['nombre']}")

    for recordatorio in datos["recordatorios"]:
        lista_recordatorios.insert(tk.END, f"{recordatorio['habito']} - {recordatorio['hora']}")

# Mostrar estadísticas de progreso
def actualizar_estadisticas():
    total = len(datos["habitos"])
    completados = sum(1 for h in datos["habitos"] if h["completado"])
    if total > 0:
        porcentaje = (completados / total) * 100
        etiqueta_estadisticas.config(text=f"Completados: {completados}/{total} ({porcentaje:.1f}%)")
    else:
        etiqueta_estadisticas.config(text="Sin datos")

# Mostrar gráfico de progreso
def mostrar_grafico():
    total = len(datos["habitos"])
    completados = sum(1 for h in datos["habitos"] if h["completado"])

    if total > 0:
        etiquetas = ["Completados", "Pendientes"]
        valores = [completados, total - completados]
        colores = ["#4CAF50", "#F44336"]

        plt.figure(figsize=(5, 5))
        plt.pie(valores, labels=etiquetas, colors=colores, autopct="%.1f%%")
        plt.title("Progreso de Hábitos")
        plt.show()

# Crear ventana
root = tk.Tk()
root.title("Gestor de Hábitos Mejorado")
root.geometry("400x550")

# Campos de entrada
entrada_habito = tk.Entry(root, width=30)
entrada_habito.pack(pady=5)
entrada_hora = tk.Entry(root, width=30)
entrada_hora.pack(pady=5)

# Botones
tk.Button(root, text="Agregar Hábito", command=agregar_habito).pack()
tk.Button(root, text="Completar Hábito", command=completar_habito).pack()
tk.Button(root, text="Eliminar Hábito", command=eliminar_habito).pack()
tk.Button(root, text="Agregar Recordatorio", command=agregar_recordatorio).pack()
tk.Button(root, text="Eliminar Recordatorio", command=eliminar_recordatorio).pack()
tk.Button(root, text="Mostrar Historial", command=mostrar_historial).pack()
tk.Button(root, text="Mostrar Gráfico", command=mostrar_grafico).pack()

# Listas
lista_habitos = tk.Listbox(root, width=40, height=6)
lista_habitos.pack()
lista_recordatorios = tk.Listbox(root, width=40, height=4)
lista_recordatorios.pack()

# Estadísticas
etiqueta_estadisticas = tk.Label(root, text="", font=("Arial", 12))
etiqueta_estadisticas.pack()

# Cargar datos
datos = cargar_datos()
historial = cargar_historial()
actualizar_lista()
actualizar_estadisticas()

# Hilo para notificaciones
verificador = threading.Thread(target=verificar_recordatorios, daemon=True)
verificador.start()

# Ejecutar
root.mainloop()
