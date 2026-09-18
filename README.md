# Bioinformatic Portfolio 
**Miguel Prior Membrives** | Estudiante de 4º de Biología (Universidad de Córdoba)
Proyectos de análisis transcriptómico (scRNA-seq) y bioinformática estructural (AlphaFold) desarrollados en Python y R.

## Proyectos Incluidos

### 1. [Single-Cell RNA-seq Analysis (Seurat)](./01_SingleCell_Transcriptomics/)
# Single-Cell RNA-seq Analysis of 3k PBMCs

Este proyecto realiza un análisis transcriptómico a nivel de célula única procesando una matriz de conteos mediante el paquete **Seurat** en R.

## Flujo de Trabajo
1. **Control de Calidad (QC):** Filtrado de células basándose en el conteo total de moléculas y limitando el ARN mitocondrial a <5% para descartar células apoptóticas.
2. **Preprocesamiento:** Normalización Logarítmica e identificación de los 2000 genes altamente variables (features).
3. **Reducción de Dimensionalidad:** Escalado de datos y análisis PCA. Selección de las primeras 10 componentes principales justificadas mediante `ElbowPlot`.
4. **Clustering y Visualización:** Agrupamiento de células (resolución 0.5) y proyección espacial bidimensional mediante **UMAP**.
5. **Anotación Inmunológica:** Identificación de marcadores diferenciales por clúster (`FindAllMarkers`) y asignación de linajes biológicos (Linfocitos T CD4/CD8, Células B, Monocitos CD14+, Células NK, Células Dendríticas y Plaquetas).

## Archivos
* `analisis_seurat.R`: Script completo con el pipeline algorítmico de Seurat.
* Carpeta `graficas/`: Archivos PDF con los FeaturePlots, métricas de control de calidad (QC) y el UMAP final anotado con las poblaciones celulares.

### 2. [Genotype-Phenotype Pipeline (AlphaFold & ColabFold)](./02_Structural_AlphaFold/)
Predicción y alineamiento estructural del factor de transcripción p53 humano bajo el impacto de la mutación patogénica R175H.
* **Herramientas:** Python, Biopython, APIs (UniProt, EBI), ColabFold, py3Dmol.
* **Técnicas:** Extracción de secuencias FASTA, mutagénesis in silico, inferencia estructural mediante Deep Learning y superposición 3D espacial minimizando la desviación RMSD del núcleo estructurado.

---
*Proyectos ejecutados localmente y en entornos Cloud (Google Colab).*
