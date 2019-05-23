# Correción de márgens en Reporte PDF

## Forma Normal sin Cambios

### Imagen página 1
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_764.png)
### Imagen página 2
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_765.png)

[Report_Normal][Report_Normal]
 https://github.com/ControlWebManager/Margin_Report/blob/master/Quotation%20_%20Order%20(41).pdf
 
## Replicacion del Error

- La hoja del reporte se dividen en tres secciones, HEADER ,  PAGE/CONTENT , FOOTER
- Cada sección trabaja con plantillas XML totalmente diferentes, luego se unen para formar una sola estructura HTML
- Seguidamente se ejecuta método específico con python que realiza la parametrización final y se ejecuta un programa llamado WKHTMLTOPDF
- Este programa es el encargado de tranformar el contenido HTML a PDF.
- La división mencionada en el item 1, el programa WKHTMLTOPDF es el encargado de manipular y realizar el PDF con los datos enviado desde python lo que dificulta a primera intancia, encontrar solución por las tantas herramientas y lenguajes de programación implicados

Explicado lo anterior, aqui tenemos el error:

Al cambiar la dimensión del logo, el  HEADER se redimensiona, y pierde la proporción inicial que le da el programa WKHTMLTOPDF, y sobre-escribe el contenido del HEADER en la seccion PAGE/CONTENT

### Imagen página 1
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_769.png)
### Imagen página 2
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_768.png)

[Reporte con error][Reporte con error]
 https://github.com/ControlWebManager/Margin_Report/blob/master/Quotation%20_%20Order%20(39).pdf
     
## Solución del Error , Versión 1.0

- Mantener el máximo height de la imagen en 90px (logo de la empresa)
- No realizar ms cambios

### Imagen 
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_770.png)

[Solución del Error]Solución del Error]
 https://github.com/ControlWebManager/Margin_Report/blob/master/Quotation%20_%20Order%20(35).pdf
 
## Solución del Error , Tipo 2.2

- De cambiar la dimensión del logo superior a a 90px se debe modificar los parámetros margen superior y espaciado del encabezado que se encuentra en la opciones de Formato de Papel

### Imagen 1
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_772.png)

### Imagen 2
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_771.png)

[Solución del Error][Solución del Errorr]
 https://github.com/ControlWebManager/Margin_Report/blob/master/Quotation%20_%20Order%20(44).pdf
 
---------------------
---------------------

