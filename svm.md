## SVM

### 1. Thuật toán: [link](https://machinelearningcoban.com/2017/04/09/smv/#-nhac-lai-bai-toan-phan-chia-hai-classes)

Một tập dữ liệu gồm có: $x_1, x_2,..., x_n$.

Đường thẳng (d): $\mathbf{Y}=\mathbf{w}^T\mathbf{x} + b$

Gọi $x_i$, $x_j$ là hai điểm thuộc 2 class gần đường thẳng nhất. Nhiệm vụ là tìm hệ số đường thẳng (d) để cho khoảng cách này đều nhau và là lớn nhất (margin).

### 2. Loss Function (8.2.2 DL4CV1)

Xem phần ví dụ tại mục **A Multi-class SVM Loss Example.**