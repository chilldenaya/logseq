- Forward propagation: mencari nilai a dan y di tiap layernya
  ![image.png](../assets/image_1644738275638_0.png)
- nilai `w` digunakan secara sharing untuk setiap sequence, yang berbeda tiap sequence hanyalah `x`,`a`, dan `y`
-
- Loss function yang digunakan adalah cross entrophy
  ![image.png](../assets/image_1644738357904_0.png)
- Loss function dari keseluruhan sequence adalah jumlah dari loss masing2 bagian
-
- Lalu, dengan menggunakan loss function ini, kita bisa melakukan backpropagation through time yang berlawanan arah dengan forward propagation
- ![image.png](../assets/image_1644738484512_0.png)
-