📘 Libro de Capital y Socios - Evolución de Participaciones
Aplicación web independiente (Single Page Application) diseñada para gestionar la evolución del capital social y las cuotas de participación en cooperativas o sociedades. Desarrollada con la imagen corporativa del Centro de Negocios Sercotec Temuco.

Esta herramienta permite simular cierres anuales, calcular el valor cuota (V.C.), distribuir remanentes y gestionar la entrada y salida de socios de forma cronológica.

🚀 Características Principales
📊 Gestión Financiera Anual
Apertura de Años: Creación de periodos fiscales consecutivos.

Parámetros Flexibles: Configuración por año de:

Monto de aportes de capital.

Emisión de nuevas cuotas vs. Solo aumento de capital.

Distribución de Remanentes (Pérdidas/Ganancias).

Cálculo Automático: Determinación del Valor Cuota basado en el patrimonio neto y cuotas en circulación.

👥 Gestión de Socios
Base de Datos Local: Registro de socios con nombre, RUT y fecha de incorporación.

Movimientos:

Ingreso de nuevos socios (calculado al valor cuota del año).

Aportes extraordinarios individuales.

Retiro de socios: Cálculo de salida y congelamiento de participación histórica.

Alertas Normativas: Advertencia visual automática si un socio supera el 20% de las cuotas totales (cumplimiento normativo común en cooperativas).

🛠 Utilidades
Persistencia de Datos: Utiliza localStorage para guardar el trabajo automáticamente en el navegador.

Exportación: Generación de reportes en formato CSV compatible con Excel.

Interfaz Responsiva: Diseño adaptado a móviles y escritorio utilizando Bootstrap 5.

⚙️ Lógica de Cálculo (Motor Financiero)
El núcleo del sistema (recalculateAllLogic) funciona recalculando toda la historia cronológicamente cada vez que se realiza un cambio. Esto asegura la integridad de los datos históricos.

Valor Cuota Base: Se calcula dividiendo el Capital Total del año anterior por el Total de Cuotas del año anterior.

Distribución de Remanentes: Los remanentes acumulados se dividen equitativamente entre los socios elegibles (antiguos y activos).

Aportes de Capital:

Modalidad Capital: El dinero se suma al capital del socio, pero sus cuotas se mantienen (aumenta el valor de cada cuota).

Modalidad Cuotas: El dinero aportado se divide por el Valor Cuota Base, generando nuevas cuotas para el socio.

🔧 Instalación y Uso
Este proyecto no requiere instalación de dependencias ni servidores (Node.js, Python, etc.). Es una solución Client-Side pura.

Opción A: Ejecutar localmente
Clona este repositorio o descarga el archivo .zip.

Ubica el archivo index.html.

Haz doble clic para abrirlo en tu navegador web favorito (Chrome, Edge, Firefox).

Opción B: Despliegue en GitHub Pages
Sube el archivo index.html a la raíz de tu repositorio.

Ve a Settings > Pages.

Selecciona la rama main y guarda. Tu calculadora estará disponible online en segundos.

📂 Estructura del Código
El proyecto reside en un único archivo (index.html) para facilitar la portabilidad, pero está estructurado internamente de la siguiente manera:

CSS: Estilos personalizados (:root variables) y Bootstrap 5 vía CDN.

HTML: Estructura semántica con modales para formularios.

JavaScript:

appData: Objeto principal de estado.

recalculateAllLogic(): Algoritmo principal de re-cálculo.

renderYearView(): Manipulación del DOM para mostrar datos.

saveData() / loadData(): Manejo de LocalStorage.

⚠️ Aviso Legal
Consideración: Los resultados generados por esta herramienta son estimativos y de carácter ilustrativo/pedagógico. No representan una contabilidad oficial ni legalmente vinculante. Se recomienda la revisión por parte de un contador auditor para balances oficiales.
