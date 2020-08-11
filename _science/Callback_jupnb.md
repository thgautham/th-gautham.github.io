---
title: "Callbacks"
toc: true
toc_sticky: true
---

Callback is used to customize the behavior of Keras model during training, evaluation or inference. When training a DL model, if we wish to stop the training once a certain accuracy reaches the desired threshold. This helps in arriving at optimal model weights and avoiding over use of trianing time and resources. 

### Setup
First, import tensorflow and keras.
```python
import tensorflow as tf
from tensorflow import keras
```
### Implement
Implement the classback class to stop training when accuract reaches __95%__.
```python
class myCallback(tf.keras.callbacks.Callback):
    def on_epoch_end(self, epoch, logs = {}):
        if(logs.get('accuracy')> 0.95):
            print("\n Reached 95% accuracy so cancelling training!")
            self.model.stop_training = True
```
### Instantiate.
```python
callbacks = myCallback()
```
We can pass a list of callbacks(as the keyword argument `callbacks`) to the following model methods:
- `keras.Model.fit()`
- `keras.Model.evaluate()`
- `keras.Model.predict()`
For our example, we use it on the `model.fit()`

```python

model.fit(x_train, y_train, epochs = 10, callbacks = [callbacks])
```
### Running the callback() on Handwriting recognition
```
import tensorflow as tf

class myCallback(tf.keras.callbacks.Callback):
    def on_epoch_end(self, epoch, logs = {}):
        if(logs.get('accuracy')> 0.95):
            print("\n Reached 95% accuracy so cancelling training!")
            self.model.stop_training = True

mnist = tf.keras.datasets.mnist

(x_train, y_train),  (x_test, y_test) = mnist.load_data()
x_train, x_test = x_train / 255.0, x_test / 255.0

callbacks = myCallback()

model = tf.keras.models.Sequential([
    tf.keras.layers.Flatten(input_shape= (28,28)),
    tf.keras.layers.Dense(512, activation=tf.nn.relu),
    tf.keras.layers.Dense(10, activation= tf.nn.softmax)
])
model.compile(optimizer= 'adam',
              loss = 'sparse_catgeorical_crossentropy',
              metrics = ['accuracy'])
model.fit(x_train, y_train, epochs = 10, callbacks = [callbacks])
```
