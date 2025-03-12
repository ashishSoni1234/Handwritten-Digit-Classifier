Developed a deep learning model for handwritten digit classification using TensorFlow and Keras.

Achieved 97.64% accuracy on the MNIST dataset.

Implemented a multi-layer perceptron (MLP) architecture with ReLU and softmax activation.

Used sparse categorical cross-entropy loss and Adam optimizer for model training.

Visualized training performance with Matplotlib.

Applied Scikit-learn metrics for evaluating model accuracy.

Gained hands-on experience in deep learning model development and optimization.
 #now explaining
 1.we are loading mnist dataset from keras and diving it into training and testing data , training data contain 60k images of (28*28)px and testing data contain 10k images of (28*28) px
2.after this before giving input to ANN . we have to normalize the input by divinding it by 255 to take all pixel value in (0-1) range ,noramilization is used to train model faster , imrove accurecy, to avoid vanishing graident and exploding gradient problem
3. vanishing graidnet problem :- in backpropgation ,if gradient become too small,weight updation is neglible or not at all, this become stop learning  is called vanishing grident problem 
4. exploding gradient:-in backgrpagtion , if gadient become too large, it leads to huge weight update  after which model fail to converge 
5.model=sequental(): means layer are added one  after another , output of one layer become input for another layer 
6. activation  fucntion:-An activation function is a mathematical function used in a neural network to determine whether a neuron should be activated or not. It introduces non-linearity into the model, allowing the network to learn complex patterns.
relu:- f(x)=max(0,x) mostly used in hidden layer , it solve vanishing grident problem 
softmax:- mainly used in ouput layer  and multiclass problem, it gives diffrenrt probablity value and we have to choose maximum prob
7.sparse_catagoricla_crossentropy:-mainly used in multiclass problem ,formuala , loss=-log(p), where p=predicted value by softmax(maximum probablity)
catagorical-crossentropy:-learn form yt and learn formula
optimizer :-learn adam optimizer 
 general structure of ANN ;-
input:- we  have to provide 28*28=784 input  to 128 neurons  of hidden layer which uses relu as activation fucntion 
then 10 neuron output which will give the 10 diffent probablity  on applying softmax it will give highest  prob  which is out digit
y=x*w+b-> A=relu(y)-> y'=w*a+b-> B=softmax(y')->loss=B and actual output ,after loss we have to optimised our weight and bias by gradient descent algorithm 
