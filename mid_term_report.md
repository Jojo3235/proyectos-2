### Breve descripción: 
Se busca reconstruir las funciones continuas f y g (asociadas a la deriva y a la difusión respectivamente) a partir de las series temporales generadas bajo el contexto de el comportamiento de nanopartículas individuales (Single Particle Tracking (SPT)), las cuales están contaminadas por ruido, con la ayuda de el modelo de Langevin sobreamortiguado, debido a la propia naturaleza de estas partículas en entornos con un número de Reynolds muy bajo, pudiendo despreciar la acción de la inercia, generando un modelo más simple. Se evaluarán 2 modelos, uno basado en procesos gaussianos dispersos y otro con una parametrización de la SDE con redes neuronales y su posterior evaluación de los resultados obtenidos por ambos modelos.   

### Progreso

Fase 1: Fundamentos y Entorno.
- Entorno virtual: Completado (Tensorflow y torch funcionan con la GPU)
- Síntesis matemática: Completado (Teoría sobre el cálculo de Itô, Langevin sobreamortiguado y formalismo de titsias)

Fase 2: Motor de Simulación
- Módulo generate_data.py: empezado (Implementación de Euler-Maruyama, con la parametrización biofísica)
- Dataset de datos (spt_synthetic_dataset.csv): no empezado (se generará una vez se termine el módulo anterior)

Fase 3: Modelo SVGP
- Módulo svgp_estimator.py (SDEs bajo diferencias finitas, SVGP heterocedástico y calibraciones de inductores M): empezado (Lectura de la teoría de SDEs) 
- Curvas ELBO: no empezado

Fase 4: Modelo Neural SDE
- Módulo neural_sde.py con gradient clipping y estabilidad numérica: no empezado
  - MLPs para drift y difusión (torchsde)
  - Muestreo determinista BrownianInterval

Fase 5: Benchmark y Memoria
- Informe final del benchmark: no empezado
- Scripts reproducibles: empezado (de momento trabajando en la generación inicial de los datos)
- Benchmarking (run_benchmark.py): no empezado (aunque en la bibliografía que he leído la han ido introduciendo ya).