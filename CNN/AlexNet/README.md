<h1>AlexNet</h1>
<h3>Why?</h3>
AlexNet was born out of the need to improve the results of the ImageNet challenge. This was one of the first Deep convolutional networks to achieve considerable accuracy on the 2012 ImageNet LSVRC-2012 challenge with an accuracy of 84.7% as compared to the second-best with an accuracy of 73.8%. The idea of spatial correlation in an image frame was explored using convolutional layers and receptive fields.
<br><br>

<h3>What?</h3>
The network consists of 5 Convolutional (CONV) layers and 3 Fully Connected (FC) layers. The activation used is the Rectified Linear Unit (ReLU). The structural details of each layer in the network can be found in the table below.
<br><br>

<h2>Architecture</h2>
<p align=center>
<img src="https://miro.medium.com/max/700/1*bD_DMBtKwveuzIkQTwjKQQ.png"> </img>
<img src="https://miro.medium.com/max/700/1*vXBvV_Unz3JAxytc5iSeoQ.png"> </img>
<p>

<strong>Input shape : 227 x 227 x 3</strong> (227 by 227 color image)
```python
INPUT_SHAPE = (227, 227, 3)
model = Sequential()
```
<strong>&lt;1st Convolutional Layer&gt;</strong>
```python
model.add( Conv2D(filters=96, input_shape=(INPUT_SHAPE), kernel_size=(11,11), strides=(4,4), padding='valid') )
model.add( Activation('relu') )
```
<strong>&lt;Max Pooling&gt;</strong>
```python
model.add( MaxPooling2D(pool_size=(3,3), strides=(2,2), padding='valid') )
```
<strong>&lt;2nd Convolutional Layer&gt;</strong>
```python
model.add( Conv2D(filters=256, kernel_size=(5,5), strides=(1,1), padding='same') )
model.add( Activation('relu') )
```
<strong>&lt;Max Pooling&gt;</strong>
```python
model.add( MaxPooling2D(pool_size=(3,3), strides=(2,2), padding='valid') )
```
<strong>&lt;3rd Convolutional Layer&gt;</strong>
```python
model.add( Conv2D(filters=384, kernel_size=(3,3), strides=(1,1), padding='same') )
model.add( Activation('relu') )
```
<strong>&lt;4th Convolutional Layer&gt;</strong>
```python
model.add( Conv2D(filters=384, kernel_size=(3,3), strides=(1,1), padding='same') )
model.add( Activation('relu') )
```
<strong>&lt;5th Convolutional Layer&gt;</strong>
```python
model.add( Conv2D(filters=256, kernel_size=(3,3), strides=(1,1), padding='same') )
model.add( Activation('relu') )
```

```python
model.add( MaxPooling2D(pool_size=(3,3), strides=(2,2), padding='valid') )
```
<img src="https://i.stack.imgur.com/dtybe.png" style="width:50px;height:60px;"></img>

https://www.tensorflow.org/api_docs/python/tf/keras/layers/Conv2D


&lt;English Resources&gt;<br>
<ul>
        <li><a href="https://towardsdatascience.com/the-w3h-of-alexnet-vggnet-resnet-and-inception-7baaaecccc96#_=_">Definition</a></li>
</ul>
