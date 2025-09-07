🧪 Práctica de Laboratorio: Simulación de Espectros IR con LAMMPS
📋 Descripción General
Esta práctica permite simular y analizar espectros de infrarrojo (IR) de moléculas de agua utilizando dinámica molecular con LAMMPS y el software PySimple Spectrometer para el procesamiento de datos.

📁 Archivos de la Práctica
1. water_dynamics.lmp - Script principal de LAMMPS
Función: Contiene toda la configuración para la simulación de dinámica molecular.

Características principales:

Configuración de potenciales de fuerza (TIP3P para agua)

Barrido angular para análisis de energía vs ángulo H-O-H

Barrido de distancia para análisis de energía vs longitud de enlace

Cálculo de VACF (Función de Autocorrelación de Velocidad) para espectros IR

Cálculo de MSD (Desplazamiento Cuadrático Medio) para análisis de difusión

Generación de múltiples archivos de datos para análisis

2. h2o.data - Estructura molecular del agua
Función: Define la geometría y parámetros de la molécula de agua.

Contenido:

Coordenadas atómicas (Oxígeno y dos Hidrógenos)

Masas atómicas

Definición de enlaces y ángulos

Parámetros de la caja de simulación

📊 Archivos de Resultados Generados
🔍 Análisis Energético:
angulo_energia.dat/txt/csv - Energía potencial vs ángulo H-O-H

distancia_energia.dat/txt/csv - Energía potencial vs distancia de enlace

📈 Análisis Dinámico:
vacf_total.txt - Función de Autocorrelación de Velocidad (para espectro IR)

msd_total.txt - Desplazamiento Cuadrático Medio (para difusión)

dynamics_data.txt - Datos combinados de dinámica molecular

🚀 Procedimiento de Ejecución
1. Preparación del entorno:
bash
mkdir practica_ir_lammps
cd practica_ir_lammps
# Copiar los archivos water_dynamics.lmp y h2o.data aquí
mkdir resultados  # Para los archivos de salida
2. Ejecución de LAMMPS:
bash
lmp -in water_dynamics.lmp
3. Análisis de resultados:
Los archivos generados en la carpeta resultados/ pueden analizarse con:

PySimple Spectrometer (para espectros IR)

Excel, Python, o cualquier software de análisis de datos

🧠 Conceptos Clave Aprendidos
Potenciales de fuerza para simulaciones moleculares

Relación entre estructura molecular y energía

Función de Autocorrelación de Velocidad (VACF) para espectroscopía IR

Desplazamiento Cuadrático Medio (MSD) para estudio de difusión

Análisis de modos vibracionales moleculares

⏱️ Tiempos Estimados
Simulación LAMMPS: 15-45 minutos (dependiendo del hardware)

Análisis de resultados: 30-60 minutos

Interpretación y reporte: 30-45 minutos

🔧 Requisitos del Sistema
LAMMPS instalado (versión reciente)

Python 3.x con NumPy, SciPy, Matplotlib (para análisis adicional)

PySimple Spectrometer (proporcionado por el docente)

4GB+ RAM recomendado para simulaciones fluidas

📝 Notas Importantes
Los archivos se generan en formato múltiple (.dat, .txt, .csv) para flexibilidad de análisis

El ángulo de equilibrio del agua es aproximadamente 104.5°

La longitud de enlace O-H de equilibrio es aproximadamente 0.9572 Å

Los resultados de VACF pueden transformarse a espectros IR mediante Transformada de Fourier

🆘 Soporte y Ayuda
Si encuentras problemas con:

La instalación de LAMMPS

La ejecución de los scripts

El análisis de los resultados

Contacta al docente para asistencia personalizada.