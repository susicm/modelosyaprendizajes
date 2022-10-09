Modelos y aprendizajes JUNIO22
<html>
  <head>
       </head>
  <body>
  <div id="cabecera">
      <h1 style="color:  Navy">MODELOS Y APRENDIZAJES</h1>	
    <h2 style="color:  Navy">Desarrollo modelos aprendizaje supervisado Breast Cancer Wisconsin (Diagnostic) Data Set  </h2>
  </div>
          <p>Por: Susana Caraguay <br> Profesor: Rafael Nogales <br> Fuente de datos: <a href=https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)>Breast Cancer Wisconsin (Diagnostic) Data Set </a> <br> Dataset: wdbc.data</p>
  <h4 style="color: Navy">OBJETIVO</h4>
	   <p>Encontrar el modelo de predicción mas adecuado para diagnóstico de cáncer (M maligno B Benigno)</p>
  <h4 style="color: Navy">PREPROCESAMIENTO DE INFORMACIÓN</h4>
<ol>
  <li>Al abrir el archivo pude obervar que consta con 569 registros.</li>
  <li>Realicé la limpieza de la información, no se encontraron valores nulos.</li>
<li>Realicé el mapeo para variable categórica diagnosis M=1 B=0.</li>
<li>Separe la variable objetivo(y) diagnosis del resto de variables.</li>
<li>Mediante la matriz de correlación identifiqué algunas variables con alta correlación.</li>
<li>Eliminé aquellas cuya correlación mayor o igual a 0.88</li>
<li> Entre las variables de alta correlación se encuentran: 'perimeter_mean','radius_mean','area_mean','radius_worst','perimeter_worst','area_worst',
'area_mean','radius_se','perimeter_se','area_se','concave points_worst','compactness_worst','texture_mean',
'concavity_mean','concave points_mean','compactness_mean','concavity_worst','texture_worst'.</li>
</ol>

<h4 style="color: Navy">MODELOS EMPLEADOS</h4>
<p>Los modelos utilizados corresponden a aprendizaje supervisado.</p>
<ul>
  <li>MODELO 1: DecisionTreeClassifier: <br>  &nbsp;&nbsp;1.1 con valores por defecto:	   &nbsp;      Accurancy:0.95 &nbsp;  	Falsos negativos: 6 <br>
          &nbsp;&nbsp;1.2 con (max_depth=3)  &nbsp;
        Accurancy:0.88  &nbsp;
	Falsos negativos: 8 </li>
  <li>MODELO 2:  SGDClassifier: &nbsp;&nbsp;
	Accurancy:0.92 &nbsp;
	Falsos negativos: 9.</li>
<li>MODELO 3: Regresión logística &nbsp;&nbsp;
        Accurancy:0.92  &nbsp;
	Falsos negativos: 6 </li>
<li>MODELO 4: Support Vector: &nbsp;&nbsp;
        Accurancy:0.94  &nbsp;
	Falsos negativos: 7.</li>
<li>MODELO 5: KNeighborsClassifier (n_neighbors=5): &nbsp;&nbsp;
        Accurancy:0.92  &nbsp;
	Falsos negativos: 7</li>
<li>MODELO 6: RandomForestClassifier (max_depth=5): &nbsp;&nbsp;
        Accurancy:0.94  &nbsp;
	Falsos negativos: 5</li>
</ul>
<h4 style="color:  Navy">CONCLUSIÓN</h4>
<li>El mejor modelo, con base al análisis realizado en el presente ejercicio es el RandomForestClassifier ya que
tiene mejor precisión y menor número de falsos negativos en la matriz de concurrencia de test.<br></li>
      
   </body>
</html>
