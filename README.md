# Neighbourhood-Component-Analysis

Four methods to implementing NCA which is often used for metric learning and dimension reduction.

* Methods:
  * Two-layer for loop
  * Matrix operation acceleration
  * Gradient expression
  * SciPy.optimize implementation

## Code Architecture

* nca_naive.py  Implementation using two nested for loops to calculate the gradient but very slow.
* nca_matrix.py Uses matrix operations for acceleration, but still has one for loop; slightly faster, but consumes more memory.
* nca_fast.py   Uses another form of gradient representation, full matrix operation, no for loop; very fast, less memory footprint.
* nca_scipy.py  Uses nca_fast.py method + scipy.optimize optimization package; includes gradient descent and coordinate descent.
* example.py    Uses the MNIST dataset for testing.
* usage.py      Demonstrates how to use it; since all four implementations are encapsulated into the NCA class and implement the fit, fit_transform, and transform methods similar to PCA, it is very easy to use.

## 方法

* 两层for循环
* 矩阵操作加速
* 另一种梯度表达形式
* scipy.optimize实现

## Result Images

* The first 9 images are the results on MNIST, with the number of classes selected from 2 to 9. Since the original image has 784 dimensions, PCA is first used to reduce the dimensionality to 100 dimensions, and then NCA is used to reduce the dimensionality to 2 dimensions.
* The next 3 images are the results obtained by directly using NCA on the digits (provided by NumPy), breast_cancer and iris datasets to reduce the dimensionality to 2 dimensions.

  <div>
    <table>
     <tr>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_2_digits.jpg"></td>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_3_digits.jpg"></td>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_4_digits.jpg"></td>
     </tr>
     <tr>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_5_digits.jpg"></td>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_6_digits.jpg"></td>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_7_digits.jpg"></td>
     </tr>
     <tr>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_8_digits.jpg"></td>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_9_digits.jpg"></td>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/mnist_with_10_digits.jpg"></td>
     </tr>
     <tr>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/digits_np.jpg"></td>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/breast_cancer.jpg"></td>
      <td><img src = "https://github.com/lamthienphuc/Dimesionality-Reduction/pics/iris.jpg"></td>
     </tr>

    </table>
  </div>
