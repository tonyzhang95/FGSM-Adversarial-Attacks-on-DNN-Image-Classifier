**Adversarial Attacks on Deep Neural Networks**

**Overview**

Train a Deep Neural Network image classifier on the MNIST dataset, then create adversarial perturbation attacks on the model. Finally, retrain the model to defend against adversarial perturbations.

**Dataset**

 The MNIST dataset contains 28X28 grayscale images of hand-drawn digits from 0-9, along with the associated labels. See the sample Python code available here: https://colab.research.google.com/github/tensorflow/docs/blob/master/site/en/tutorials/quickstart/beginner.ipynb#scrollTo=h3IKyzTCDNGo

**Details**

**Baseline DNN** is a 2-layer DNN for MNIST digit classification. The DNN has a 784 (28x28) dimensional input, a 10-dimensional output and one hidden layer with 300 hidden neurons and ReLU activations. 

**FGSM based untargeted attacks:** FGSM based untargeted attacks on the baseline DNN. 

**FGSM based targeted attacks:** FGSM based targeted attacks aiming for the next category of the labels (1->2, 3->4, etc).

**Adversarial Retraining against Untargeted FGSM Attacks:** To defend against adversarial perturbations, we adversarially perturbs each image in the training set using FGSM based untargeted attacks. Then we retrain a new DNN with both original training set and the  adversarially perturbed images. 