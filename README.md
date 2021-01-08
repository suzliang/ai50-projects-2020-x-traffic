I ran multiple tests and changed the number of convolutional and pooling layers, as well as the sizes of the filters of the convolutional layers and of the pooling layers. Increasing the numbers and sizes of the filters convolutional layers significantly increased processing time, which is costly for larger sets of data and did not work well. Decreasing dropout rate increased accuracy, but may lead to overfitting. 


Both convolutional and pooling layers
    Numbers
        Greater numbers increased processing time and increased accuracy. 
            Original convolutional, pooling: 17-18ms/step. Max accuracy = 0.9416 after epoch 10/10. Test accuracy = 0.9682.
            +1 convolutional, +1 pooling: 20ms/step. Max accuracy = 0.9605 after epoch 10/10. Test accuracy = 0.9654.

Convolutional layers
    Numbers
        Greater numbers of convolutional layers significantly increased processing time and accuracy.
            Original convolutional, pooling: 17-18ms/step. Max accuracy = 0.9416 after epoch 10/10. Test accuracy = 0.9682.
            +1 convolutional layer (with increased units): 30 ms/step. Max accuracy = 0.9715 after epoch 10/10. Test accuracy = 0.9735.
            +1 units (with increased size from 64 to 128): 22-24ms/step. Max accuracy = 0.9540 after epoch 10/10. Test accuracy = 0.9607.
    Sizes
        Greater sizes of filters of convolutional layers increased processing time and increased accuracy.
            Original convolutional, pooling: 17-18ms/step. Max accuracy = 0.9416 after epoch 10/10. Test accuracy = 0.9682.
            +1 size (with increased size from (3,3) to (5,5)): 27-29ms/step. Max accuracy = 0.9102 after epoch 10/10. Test accuracy = 0.9401.

Pooling layers
    Numbers
        A greater number of pooling layers decreased processing time and decreased accuracy.
            Original convolutional, pooling: 17-18ms/step. Max accuracy = 0.9416 after epoch 10/10. Test accuracy = 0.9682.
            +1 pooling: 15-16 ms/step. Max accuracy = 0.7984 after epoch 10/10. Test accuracy = 0.8802.
    Sizes
        A greater size of pooling layers (from (2,2) to (3,3)) decreased processing time and decreased accuracy.
            Original convolutional, pooling: 17-18ms/step. Max accuracy = 0.9416 after epoch 10/10. Test accuracy = 0.9682.
            +1 size: 15-16 ms/step. Max accuracy = 0.9258 after epoch 10/10. Test accuracy = 0.9398.

Hidden layers
    Numbers
    Sizes

Dropout
    Lower dropout rate did not change processing time and increased accuracy.
        Original dropout = 0.4: 17-18ms/step. Max accuracy = 0.9416 after epoch 10/10. Test accuracy = 0.9682.
        Changed dropout = 0.2: 17-18 ms/step. Max accuracy = 0.9755 after epoch 10/10. Test accuracy = 0.9760.