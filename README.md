# app/routes.py

from flask import render_template, redirect, url_for, flash
from app import app, db
from app.models import Actividad, Progreso

@app.route('/')
def index():
    return render_template('index.html')

@app.route('/actividad/<int:id>')
def actividad(id):
    actividad = Actividad.query.get_or_404(id)
    return render_template('actividad.html', actividad=actividad)

@app.route('/registrar_progreso', methods=['POST'])
def registrar_progreso():
    # Código para registrar el progreso del estudiante
    pass
