#Instalacion#

1.-Para instalar el componente primero tenemos que descargar el proyecto comprimido en ZIP, en el apartado de code.
![image](https://github.com/user-attachments/assets/a516d4c3-21af-4aba-ae08-b680273398be)

2.-Una vez descargado el proyecto, abrimos NetBeans y en la pestaña File seleccionamos import proyect y después from ZIP.
![image](https://github.com/user-attachments/assets/6e31a907-05e9-4ad5-876b-8d0c4bbd9305)

3.-Se nos abrirá esta ventana y en ZIP File: damos click en browse para buscar nuestro archivo
![image](https://github.com/user-attachments/assets/de72a28c-646a-463b-9158-cc6061345950)

4.-Después de haberlo importado, damos click derecho sobre el proyecto y seleccionamos Clean and Build
esto lo que va hacer es crear un archivo .jar
![image](https://github.com/user-attachments/assets/822d1dde-8bd3-4efb-b18f-750fec7678a8)

5.-Nos generará un archivo .JAR y en el apartado de output podremos ver donde se guardó(en caso 
de que no aparezca lo puedes buscar en netbeans proyects)
![image](https://github.com/user-attachments/assets/374fdfba-5b44-4a53-bd08-8f5ec254f093)

6.-En NetBeans, ahora nos dirigimos a la pestaña de Tools y seleccionamos Palette y después Swing/AWT Components
![image](https://github.com/user-attachments/assets/1219d7b2-7a89-4116-8229-b00002351454)

7.-Nos abrirá una ventana nueva y en ella seleccionamos Add from JAR… para buscar el componente. Aqui
buscamos el archivo .jar
![image](https://github.com/user-attachments/assets/1e553d8e-3516-46ee-953a-8767ab59d424)

8.-Agregamos el de inicioo y luego click en next
![image](https://github.com/user-attachments/assets/e35cb144-9020-4a3c-a46a-1495093098fd)

9.-Después seleccionamos el apartado en el queremos que aparezca y damos click en Finish
![image](https://github.com/user-attachments/assets/ee2e2f2a-f7a2-43d8-8a16-f39a99dd66f1)

10.- deberíamos ser capaces de ver el componente en el apartado de Pallete al crear un nuevo JForm.
![image](https://github.com/user-attachments/assets/88dc5349-8287-4eeb-96e7-84c5d69fa6b0)

Explicacion de los metodos 
crecion de un panel personlizado 
CLASE PANEL
1.-constructor Panel(): Define que el panel no sea opaco (setOpaque(false)) 
para permitir que se vean los bordes redondeados y evitar que el fondo del panel se rellene automáticamente.

2.-setRoundTopLeft(int roundTopLeft), setRoundTopRight(int roundTopRight), 
setRoundBottomLeft(int roundBottomLeft), setRoundBottomRight(int roundBottomRight): Son métodos para ajustar el radio de redondeo de cada esquina del panel (en píxeles). Llaman a repaint() para actualizar la interfaz tras cualquier cambio en los radios de redondeo.

3.-paintComponent(Graphics grphcs): Sobrescribe el método de JPanel para personalizar el dibujo del componente. 
Aquí se crea una instancia de Graphics2D y se define el antialiasing para bordes suaves. Se establece el 
color de fondo y se crea una forma (Area) que representa el panel con esquinas redondeadas. 
Las formas de cada esquina se obtienen de los métodos
createRoundTopLeft, createRoundTopRight, createRoundBottomLeft y createRoundBottomRight.

 4.-createRoundTopLeft(), createRoundTopRight(), createRoundBottomLeft(), createRoundBottomRight():
 Cada uno crea una Shape que representa una esquina redondeada del panel. 
 Se basa en RoundRectangle2D y Rectangle2D para definir el redondeo y ajustar el área de cada esquina.

 5.-Esta clase es la que nos va ayudar a que los paneles(cuadros de dialogo tengan buna forma)
 y ya dentro de los frame es donde se implementa.

 OTRO METOD A TENER EN CUENTA
 Metodo para que una ventana desapareza en un cierto tiempo
 -guardado.setModal(false);: Configura el cuadro de diálogo
 guardado para que no sea modal, es decir, para que permita la interacción con otras ventanas mientras está visible.
 -guardado.setVisible(true);: Muestra el cuadro de diálogo guardado en la pantalla.
-guardado.setLocationRelativeTo(null);: Centra el cuadro de diálogo en la pantalla.
-javax.swing.Timer timer = new javax.swing.Timer(1500, new java.awt.event.ActionListener() { ... });: 
Aquí se crea un temporizador (Timer) que ejecutará una acción después de 1500 milisegundos (1.5 segundos).
El ActionListener asociado define la acción a ejecutar cuando se alcance ese tiempo.
-@Override public void actionPerformed(java.awt.event.ActionEvent e) { guardado.dispose(); }: 
Sobrescribe el método actionPerformed del ActionListener.
Cuando el temporizador finaliza (luego de 1.5 segundos), se llama a guardado.dispose();, que cierra el cuadro de diálogo.
-timer.setRepeats(false);: Configura el temporizador para que no se repita automáticamente después de ejecutar la acción la primera vez.
timer.start();: Inicia el temporizador, activando la cuenta de 1.5 segundos para cerrar el cuadro de diálogo.



Explicacion del componente
https://github.com/user-attachments/assets/468cade0-4eb2-43b2-973b-e73134ec6d7b

