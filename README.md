# SVM_radial_kernel
This project involves the implementation of efficient and effective RBF SVC on MNIST data set. The MNIST data comprises of digital images of several digits ranging from 0 to 9. Each image is 28 x 28 pixels. Thus, the data set has 10 levels of classes.

Let $\mathbf{x}$ and $ \mathbf{x'}$ be two feature vectors, then their RBF kernel is:

$K(\mathbf{x}, \mathbf{x'}) = \exp\left(-\frac{\|\mathbf{x} - \mathbf{x'}\|^2}{2\sigma^2}\right)$

$\textstyle\|\mathbf{x} - \mathbf{x'}\|^2$ is can be considered as the Euclidean distance between the two feature vectors.

This equation can be simplified:

$K(\mathbf{x}, \mathbf{x'}) = \exp(-\gamma\|\mathbf{x} - \mathbf{x'}\|^2)$,     $\ \ \gamma > 0$

Where $\textstyle\gamma = \tfrac{1}{2\sigma^2}$

RBF SVC seems to work better on a scaled dataset, hence, the train and test sets were scaled between zero and one by dividing through by 255 (which is the maximum value in the dataset)

Gamma is a parameter of the radial basis function kernel, a small gamma in RBF means high standard deviation around each point and vice-versa.

On the other hand, the cost is a parameter of the SVM. Cost determines how much penalty is given to data point on the wrong side of the hyperplane. A Low cost simply implies a smooth decision surface. inversely, a high cost aims at correctly classifying all the training set, which might lead to a complex model.
