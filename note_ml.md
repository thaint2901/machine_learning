## Regularization (9.4)

**Khái quát**
Là một kỹ thuật nhằm giảm overfitting.
Có nhiều loại regularization như *Dropout*, *Data Augmentation*, *Early Stopping*, *Weight Decay*.

## Weight Initialization (10.1 DL4CV1)

**Khái quát**
Mô tả các phương pháp khởi tạo trọng số(w) trước khi đưa vào mạng.

### 1. Uniform Distribution (Phân phối đều)

```python
W = np.random.uniform(low=-0.05, high=0.05, size=(64, 32))
```

Tạo các giá trị phân phối đều trong khoảng min, max (có các xác xuất xuất hiện như nhau).

### 2. Normal Distribution (Phân phối chuẩn)

Là phân phối với kỳ vọng (mean) $\mu$ và phương sai $\sigma^2$.
Hàm phân phối mật độ xác xuất:
$$p(x) = \frac{1}{\sqrt{2 \pi \sigma^2}}\exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)$$

```python
W = np.random.normal(0.0, 0.5, size=(64, 32))
```

> Các phương pháp khởi tạo trọng số **W** đều dựa trên lý thuyết từ hai phân phối trên.

**Định nghĩa các tham số:**

* $F_{in}$: Số lượng inputs của layer.
* $F_{out}$: Số lượng outputs của layer.

### 3. Glorot/Xavier Uniform and Normal

#### Uniform

```python
F_in = 64
F_out = 32
limit = np.sqrt(3 / float(F_in))
W = np.random.uniform(low=-limit, high=limit, size=(F_in, F_out))
```

#### Normal

```python
F_in = 64
F_out = 32
limit = np.sqrt(1 / float(F_in))
W = np.random.normal(0.0, limit, size=(F_in, F_out))
```

***Là phương pháp khởi tạo mặc định của keras và là phương pháp phổ biến nhất.***

### 4. He Uniform and Normal

#### Uniform

```python
F_in = 64
F_out = 32
limit = np.sqrt(6 / float(F_in)
W = np.random.uniform(low=-limit, high=limit, size=(F_in, F_out))
```

#### Normal

```python
F_in = 64
F_out = 32
limit = np.sqrt(2 / float(F_in))
W = np.random.normal(0.0, limit, size=(F_in, F_out))
```

> Không có cái nào thực sự tốt hơn cái nào, cần phải tự kiểm thử và đánh giá

## [mAP (mean Average Precision) for Object Detection](https://medium.com/@jonathan_hui/map-mean-average-precision-for-object-detection-45c121a31173)

