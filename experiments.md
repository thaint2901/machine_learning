# Experiments



# Classification

* Thay đổi weight initialization
* Sử dụng ELU thay thế ReLu > tăng vài % acc
* Sử dụng BatchNormalizetion sau Activate
* Sử dụng L2 weight decay với hệ số 0.0001 - 0.0005 > Tránh Overfitting
* Thay đổi learning rate tuỳ theo đồ thị loss
* Chọn optimizer: SGD (```learning_rate=1e-3, momentum=0.9, wd=0.0005```), Adam, RMSProp