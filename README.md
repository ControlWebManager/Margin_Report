# Correción de márgens en Reporte PDF

## Forma Normal sin Cambios

### Imagen página 1
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_764.png)
### Imagen página 2
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_765.png)

[Report_Normal][Report_Normal]
 https://github.com/ControlWebManager/Margin_Report/blob/master/Quotation%20_%20Order%20(41).pdf
 
## Replicacion del Error

1-. La hoja del reporte se dividen en tres secciones, HEADER ,  PAGE/CONTENT , FOOTER
2-. Cada sección trabaja con plantillas XML totalmente diferentes, luego se unen para formar una sola estructura HTML
3-. Luego se ejecuta método específico con python que realiza la parametrización final y se ejecuta un programa llamado WKHTMLTOPDF
4.- Este programa es el encargado de tranformar el contenido HTML a PDF. Aquí es donde se complica tody 
5.- La división mencionada en el item 1, el programa WKHTMLTOPDF es el encargado de manipular y realizar la modificación final del PDF

Explicado lo anterior:

Al cambiar la dimensión del logo, el  HEADER se redimensiona, y pierde la proporción inicial que le da el programa WKHTMLTOPDF, y sobresescribe el contenido del HEADER enla seccion PAGE/CONTENT

### Imagen página 1
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_764.png)
### Imagen página 2
![](https://github.com/ControlWebManager/Margin_Report/blob/master/Selecci%C3%B3n_765.png)

[Report_Normal][Report_Normal]
 https://github.com/ControlWebManager/Margin_Report/blob/master/Quotation%20_%20Order%20(41).pdf
     
     

---------------------
---------------------

