<h1>VGGNet (VGG16)</h1>
<h3>Why?</h3>
VGGNet was born out of the need to reduce the # of parameters in the CONV layers and improve on training time.
<br><br>

<h3>What?</h3>
There are multiple variants of VGGNet (VGG16, VGG19, etc.) which differ only in the total number of layers in the network. The structural details of a VGG16 network have been shown below.
<br><br>

<h2>Architecture</h2>
<p align=center>
<img src="https://miro.medium.com/max/700/1*HzxRI1qHXjiVXla-_NiMBA.png"> </img>
<img src="https://miro.medium.com/max/700/1*1gA7d9svzp_jRHPsyy63Iw.png"> </img><br>
</p>
        

<strong>Input shape : 224 x 224 x 3</strong> (224 by 224 color image)
```python
INPUT_SHAPE = (227, 227, 3)
model = Sequential()
```
<strong>&lt;1st Convolutional Layer&gt;</strong><br>
[kernel_size, strides?](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Conv2D)
```python
model.add( Conv2D(input_shape= INPUT_SHAPE, filters=64, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
```

<strong>&lt;2nd Convolutional Layer & Max Pooling&gt;</strong><br>
```python
model.add( Conv2D(filters=64, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
model.add( MaxPooling2D(pool_size=(2,2), strides=(2,2)) )
```

<strong>&lt;3rd Convolutional Layer&gt;</strong><br>
```python
model.add( Conv2D(filters=128, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
```

<strong>&lt;4th Convolutional Layer & Max Pooling&gt;</strong><br>
```python
model.add( Conv2D(filters=128, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
model.add( MaxPooling2D(pool_size=(2,2), strides=(2,2)) )
```

<strong>&lt;5th Convolutional Layer&gt;</strong><br>
```python
model.add( Conv2D(filters=256, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
```

<strong>&lt;6th Convolutional Layer&gt;</strong><br>
```python
model.add( Conv2D(filters=256, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
```

<strong>&lt;7th Convolutional Layer & Max Pooling&gt;</strong><br>
```python
model.add( Conv2D(filters=256, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
model.add( MaxPooling2D(pool_size=(2,2), strides=(2,2)) )
```

<strong>&lt;8th Convolutional Layer&gt;</strong><br>
```python
model.add( Conv2D(filters=512, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
```

<strong>&lt;9th Convolutional Layer&gt;</strong><br>
```python
model.add( Conv2D(filters=512, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
```

<strong>&lt;10th Convolutional Layer & Max Pooling&gt;</strong><br>
```python
model.add( Conv2D(filters=512, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
model.add( MaxPooling2D(pool_size=(2,2), strides=(2,2)) )
```

<strong>&lt;11th Convolutional Layer&gt;</strong><br>
```python
model.add( Conv2D(filters=512, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
```

<strong>&lt;12th Convolutional Layer&gt;</strong><br>
```python
model.add( Conv2D(filters=512, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
```

<strong>&lt;13th Convolutional Layer & Max Pooling&gt;</strong><br>
```python
model.add( Conv2D(filters=512, kernel_size=(3,3), strides = (1, 1), padding="same") )
model.add( Activation('relu') )
model.add( MaxPooling2D(pool_size=(2,2), strides=(2,2)) )
```

<img src="https://i.stack.imgur.com/dtybe.png" style="width:50px;height:60px;"></img>




&lt;English Resources&gt;<br>
<ul>
        <li><a href="https://towardsdatascience.com/the-w3h-of-alexnet-vggnet-resnet-and-inception-7baaaecccc96#_=_">Definition</a></li>
</ul>
