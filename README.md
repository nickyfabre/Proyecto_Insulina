## Caracterización Fisicoquímica y Estructural In Silico de la Insulina Humana

#### Nombres de los integrantes:

Agustín Hernán Brest Nicole Fabre Barbero Julieta Bayarri Alboronoz Josefina Herrera

¿Cuál es la correlacion del perfil de aminoacidos con la hidrofobicidad de la insulina?

Obtener y verificar la secuencia de la proteína: Descargar la secuencia de aminoácidos de la insulina humana (UniProt ID: P01308) en formato FASTA.

Caracterizar las propiedades fisicoquímicas fundamentales: Calcular y presentar métricas clave como el peso molecular, el punto isoeléctrico (pI) y el índice de hidropatía (GRAVY) para la insulina.

Analizar la composición de aminoácidos y su impacto: Determinar la composición porcentual de los aminoácidos individuales y la distribución de grupos químicos (cargados, polares, no polares), y correlacionarla con el perfil de hidropatía de la proteína.

Estimar la estructura secundaria: Predecir y cuantificar las proporciones de las diferentes estructuras secundarias (hélice alfa, lámina beta, giros y regiones desordenadas) presentes en la insulina.

Modelar el comportamiento de carga en función del pH: Generar la curva teórica de carga neta de la insulina en un rango de pH, identificando su punto isoeléctrico y las cargas a pH fisiológico.

#### iii. Datos utilizados: proteína, organismo, identificador y fuente.

Datos de Uniprot: Nombre: INS\_Human Organismo: Homo sapiens Identificador: P01308 Fuente: Uniprot Fecha de consulta: 29/9/26

### iv. Herramientas y metodología: qué hicieron y con qué parámetros relevantes.

Este proyecto se desarrolló en un entorno de Google Colab, utilizando el lenguaje de programación Python 3\. Se emplearon diversas librerías especializadas en bioinformática y visualización de datos para la caracterización in silico de la insulina humana (UniProt ID: P01308).

1. **Carga y Verificación de la Secuencia:**

Herramientas: Librerías `urllib.request` (para conexión HTTP) y `Biopython`. Metodología: La secuencia de aminoácidos de la insulina humana se obtuvo directamente de la base de datos **UniProt** (Universal Protein Resource) a través de su API REST, utilizando el ID de acceso P01308. La secuencia descargada en formato FASTA fue posteriormente parseada e inspeccionada con Bio.SeqIO para verificar su integridad y longitud.

2. **Cálculo de Propiedades Fisicoquímicas**:

Herramientas: Biopython (Bio.SeqUtils.ProtParam.ProteinAnalysis) y Pandas (para almacenamiento de datos). Metodología: Se calcularon propiedades fisicoquímicas fundamentales a partir de la secuencia de aminoácidos, incluyendo: peso molecular, punto isoeléctrico (pI) y el índice de hidropatía promedio (GRAVY). Los resultados fueron presentados en la salida y guardados en un archivo CSV.

3. **Análisis del Perfil de Hidropatía (Kyte-Doolittle):**

Herramientas: Biopython (escalas de hidropatía), Matplotlib y Seaborn (para visualización). Metodología: Se generó el perfil de hidropatía utilizando la escala de Kyte-Doolittle. Se aplicó una ventana móvil (parámetro de 9 aminoácidos) para suavizar la curva y se identificaron regiones hidrofóbicas (puntuaciones \> 0\) e hidrofílicas (puntuaciones \< 0\) a lo largo de la secuencia. El perfil resultante se visualizó gráficamente y se guardó como imagen PNG.

4. **Composición de Aminoácidos y Grupos Químicos:**

Herramientas: Biopython (Bio.SeqUtils.ProtParam.ProteinAnalysis), Matplotlib y Seaborn, Pandas. Metodología: Se determinó la frecuencia porcentual de cada aminoácido individual en la secuencia. Adicionalmente, los aminoácidos se agruparon en categorías según su carga eléctrica (positiva, negativa) y polaridad (polares sin carga, no polares). Estos datos se visualizaron mediante gráficos de barras y se guardaron en un archivo CSV.

5. **Estimación de la Estructura Secundaria:**

Herramientas: Biopython (Bio.SeqUtils.ProtParam.ProteinAnalysis), Matplotlib y Seaborn, Pandas. Metodología: Se estimó la fracción porcentual de las estructuras secundarias principales (hélice alfa, lámina beta y giros/bucles) presentes en la proteína. Los resultados se representaron en un gráfico de dona y se almacenaron en un archivo CSV.

6. **Determinación del Punto Isoeléctrico y Curva de Carga:**

Herramientas: Biopython (Bio.SeqUtils.ProtParam.ProteinAnalysis), NumPy, Matplotlib y Seaborn, Pandas. Metodología: Se calculó el punto isoeléctrico (pI) teórico de la insulina. Se generó una curva de titulación teórica que muestra la carga neta de la proteína en función del pH. Esta curva, junto con las cargas netas a pHs específicos (2.0, 7.4 y 12.0), se visualizó gráficamente y los datos se guardaron en un archivo CSV.

### v. Resultados principales: una tabla, figura o resumen breve.

\!\[Texto alternativo\](ruta-o-url-de-la-imagen.png)

### vi. Conclusión breve y limitaciones del análisis.

&nbsp;

### vii. Reproducibilidad: pasos para volver a ejecutar el análisis o repetir la consulta.

### Estructura del proyecto:

proyecto-bioinfo-rsg-apellidos/ \---README.md \---data/ \--------sequence.fasta \---scripts/ \--------análisis.py (usar uno o varios scripts) \---results/ \--------resultados.txt (o tabla de resumen) \---figures/ \--------figuras.png (si existe) \---docs/ \--------notas.md (opcional)
