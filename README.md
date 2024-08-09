This file contains procedures for testing the energy consumption and inference time of different ML export formats. It is mainly divided into text classification and image classification tasks.


1.ML models for text classification： LSTM/XGboost/Random forest
2.ML models classification: CNN/xgboost/Random forest

（All test tasks were based on the macOS platform and used PowerMetrics to record CPU and GUP energy consumption information. Therefore, you need to grant the appropriate programme privileges in the terminal before testing.）

Because this test is based on the masOS environment, at the end of the test without an export format, please carry out the corresponding system cache cleanup.
macOS----sudo purge --------
CPU------torch.cuda.empty_cache()--------
GPU------sudo sync; sudo echo 3 > /proc/sys/vm/drop_caches）-----------

---Batch size setting---
For single inference and batch inference settings, please change the batch_size , while Pytorch format needs to change the batch size in the model training, and the rest can be changed in the corresponding inference program.
---Test sample----
For the test set sample size can be modified accordingly in X_test_sample.
