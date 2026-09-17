# Simulación y Análisis Estadístico de Tiempos de Atención Hospitalaria

Trabajo práctico de la materia **Simulación**, desarrollado en Python utilizando técnicas de análisis y procesamiento de datos para estudiar los tiempos de atención de pacientes en un entorno hospitalario.

## Descripción

El proyecto analiza un conjunto de datos correspondiente a atenciones hospitalarias durante los primeros 13 días de noviembre de 2019.

El dataset contiene información relacionada con:

* Fecha de atención.
* Ingresos por medicación.
* Costos de laboratorio.
* Ingresos por consultas.
* Tipo de médico.
* Tipo de cobertura médica.
* Tipo de paciente.
* Hora de entrada al hospital.
* Hora de inicio de la consulta.
* Hora de finalización.
* Identificador del paciente.

El conjunto de datos utilizado contiene **29.998 registros y 11 variables**.

## Objetivos

El trabajo busca preparar y analizar los datos para estudiar el comportamiento de los tiempos de atención hospitalaria y obtener información que pueda ser utilizada posteriormente en el proceso de simulación.

Entre las tareas realizadas se encuentran:

* Exploración inicial del dataset.
* Análisis de las variables disponibles.
* Conversión y preparación de datos temporales.
* Cálculo del tiempo de consulta.
* Conversión de los tiempos a segundos y minutos.
* Segmentación de los datos según el tipo de médico.
* Análisis mediante histogramas y diagramas de caja.
* Análisis estadístico de la distribución de los tiempos de consulta.

## Tecnologías utilizadas

* **Python 3**
* **Jupyter Notebook / Google Colab**
* **Pandas** — manipulación y análisis de datos.
* **NumPy** — operaciones numéricas.
* **Matplotlib** — visualización de datos.
* **SciPy** — análisis estadístico.
* **Fitter** — ajuste y análisis de distribuciones de probabilidad.

## Análisis de los tiempos de consulta

A partir de los horarios de entrada, inicio y finalización de la consulta, se construyeron nuevas variables temporales para poder trabajar con los tiempos de atención.

El tiempo de consulta se calcula a partir de:

```text
Tiempo de consulta = Hora de finalización - Hora de inicio de consulta
```

Posteriormente, el resultado se expresa en segundos y minutos para facilitar el análisis estadístico.

También se realiza una separación de los registros según el tipo de médico:

* **ANCHOR** — médicos titulares.
* **LOCUM** — médicos sustitutos.
* **FLOATING** — médicos voluntarios.

## Estructura del proyecto

```text
.
├── TP4_Simulacion.ipynb
├── Datos/
│   └── hospital_data_sampleee.xlsx
└── README.md
```

> El archivo de datos debe encontrarse en la carpeta `Datos/` para ejecutar el notebook sin modificar las rutas de carga.

## Cómo ejecutar el proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/USUARIO/simulacion-analisis-tiempos-atencion-hospitalaria.git
cd simulacion-analisis-tiempos-atencion-hospitalaria
```

### 2. Instalar las dependencias

```bash
pip install pandas numpy matplotlib scipy fitter openpyxl
```

### 3. Ejecutar el notebook

Abrir:

```text
TP4_Simulacion.ipynb
```

El notebook puede ejecutarse utilizando **Jupyter Notebook**, **JupyterLab** o **Google Colab**.

## Contexto académico

Proyecto realizado como parte de los trabajos prácticos de la materia **Simulación** de la carrera **Ingeniería en Sistemas de Información**.

## Autor

**Elías Puddini**

Estudiante de Ingeniería en Sistemas de Información — UTN.
