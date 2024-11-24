## comparing the model storage formats size,infrence time, Accuracy


the goal is compare the ,keras ,h5 ,tflite ,onnx ,ot ,pth format.

- the dataset is cifar-10 with 10 RGB classes
- 50000 train samples and 10000 test samples
- used simple CNN deep learning model. 

### Model Summary

```plaintext
Layer (type)                 Output Shape              Param #
=================================================================
conv2d (Conv2D)                      │ (None, 30, 30, 32)          │             896 │
│ max_pooling2d (MaxPooling2D)      │ (None, 15, 15, 32)          │               0  |
│ conv2d_1 (Conv2D)                    │ (None, 13, 13, 64)          │          18,496 │
│ max_pooling2d_1 (MaxPooling2D)       │ (None, 6, 6, 64)            │               0 │
│ flatten (Flatten)                    │ (None, 2304)                │               0 │
│ dense (Dense)                        │ (None, 64)                  │         147,520 │
│ dense_1 (Dense)                      │ (None, 10)                  │             650 
=================================================================
Total params: 804,554
Trainable params: 804,554
Non-trainable params: 0
```

| FORMAT | SIZE | infrence_time | accuracy | test_time |
| ------ | ------ | ------ | ------ | ------ |
| keras | 1.95MB | 0.12 |
| h5 | 1.95MB |  0.12 | 0.1 | 5.61 |
| tflite | 0.64MB | 0.015 | 0.61 | 4.61 |
| onnx | 0.64MB | 0.001 | 0.61 | 2.63
| pt | 2MB | 0.015 | 0.66 | 9.52 | 
| Pth | 2MB | 0.029 | 0.66 | 10.23 | 


## License
MIT
