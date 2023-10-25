# Seminario Mundos Virtuales - Gr08  
## Respuestas a las preguntas propuestas:  

1. Translate, Rotate y localScale.  
   <br>
2. Se haría de la siguiente manera:  
    transform.Translate(transform.position * 2);  
    transform.Rotate(transform.up * 30);  
      
    No se obtendría el mismo resultado pues en las transformaciones en unity el orden importa.
    <br>

3. ![Img01](./img/MundosVirtualesGr08_img01.png)  
   <br>
4. ![Img02](./img/MundosVirtualesGr08_img02.png)  
   <br>
5. Cuanto menor sea, mayores se renderizan los objetos porque los planos de proyección serán más pequeños.  
   <br>
6. Es cierto ya que en el modo ortográfico se elimina la perspectiva, representando todos los objetos con tamaños proporcionales. Se puede acceder a esta vista desde el inspector haciendo click en la caja central del gizmo localizado en la esquina superior derecha.   
   <br>
7. camera.transform.rotation = Quaternion.Euler(0f, 30f * Mathf.Deg2Rad, 0f)  
   <br>
8. Se accede al atributo ‘projectionMatrix’ de la cámara que se quiere estudiar dentro de update (para así acceder a la matriz del último frame), el cual devolverá una Matrix4x4 con los datos pedidos (se puede mostrar esta por consola).  
   <br>
9. Se accede a ella de forma igual que en el caso anterior, la única diferencia siendo que la propia cámara tiene que ser de vista ortogonal.  
   <br>
10. Accediendo al atributo ‘localToWorldMatrix’ del Transform del GameObject que se pretende estudiar (el cual se debe guardar dentro de una Matrix4x4).  
    <br> 
11. Para acceder a la matriz del sistema de referencia de la vista, es decir, la cámara, se usa la función Camera.worldToCameraMatrix  
    <br>
12. 0.97428	0.00000	0.00000	0.00000  
    0.00000	1.73205	0.00000	0.00000  
    0.00000	0.00000	-1.00060 -0.60018  
    0.00000	0.00000	-1.00000 0.00000  
    <br>
13. 1.00000	0.00000	0.00000	0.00000  
    0.00000	1.00000	0.00000	0.00000  
    0.00000	0.00000	1.00000	0.00000  
    0.00000	0.00000	0.00000	1.00000  
    <br>
14. -0.38625 -0.72351 0.57214 -2.40000  
    0.00000	0.62027	0.78438	0.25798  
    -0.92239 0.30297 -0.23958 3.03000  
    0.00000	0.00000	0.00000	1.00000  
    <br>
15. Las coordenadas del sistema de referencia vienen dadas por la propia posición del objeto, cosa que podemos obtener si accedemos a transform.position y la rotación en transform.rotation.  