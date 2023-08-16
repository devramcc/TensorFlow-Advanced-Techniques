https://community.deeplearning.ai/t/tf-at-course-1-lecture-notes/51563

Question:
614/614 [==============================] - 0s 135us/sample - loss: 0.1321 - y1_output_loss: 0.0687 - y2_output_loss: 0.0646 - y1_output_root_mean_squared_error: 0.2594 - y1_output_accuracy: 0.0000e+00 - y2_output_root_mean_squared_error: 0.2545 - y2_output_accuracy: 0.0000e+00 - val_loss: 0.6905 - val_y1_output_loss: 0.2577 - val_y2_output_loss: 0.4418 - val_y1_output_root_mean_squared_error: 0.5151 - val_y1_output_accuracy: 0.0000e+00 - val_y2_output_root_mean_squared_error: 0.6520 - val_y2_output_accuracy: 0.0000e+00

what is the accuracy on y1 and y2?

Answer:
In the provided output, it seems that the accuracy for both 'y1_output' and 'y2_output' is reported as zero (0.0000e+00). This indicates that accuracy was not computed or tracked for these outputs during training. It's possible that you are using regression tasks (such as predicting numerical values) for 'y1_output' and 'y2_output', which makes sense since you are using the root mean squared error (RMSE) as the primary metric.

Accuracy is typically used for classification tasks, where you predict discrete classes, rather than continuous values. In your case, since you are using RMSE as the metric, it suggests that you are working with regression tasks, and accuracy is not applicable.

If you are interested in evaluating the performance of your model on classification tasks, you should use appropriate metrics like accuracy, precision, recall, F1-score, etc. However, for regression tasks, it's more common to use metrics like RMSE, Mean Absolute Error (MAE), etc., to measure the deviation of predicted continuous values from the actual values.