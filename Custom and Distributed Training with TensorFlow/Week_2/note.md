in 1024 data row
with batch_size = 64

in model.fit with 20 epoch does it iterate over 1024 data 20 times or 64 data row 20 times?


In the context of machine learning, particularly with deep learning frameworks like TensorFlow and Keras, the training process involves iterating over batches of data rather than individual data points. The batch size is the number of data points used in each iteration of the training process.

In your scenario:

You have 1024 data rows in total.
You've set the batch size to 64.
You're training for 20 epochs.
During each epoch, the training process will iterate through the entire dataset in batches. Since your batch size is 64, it means that each iteration (step) will involve processing 64 data rows. After processing 1024/64 = 16 such batches (or steps), you will have covered the entire dataset once, completing one epoch.

Since you're training for 20 epochs, this means the training process will repeat this entire cycle (16 steps, covering the entire dataset) 20 times. Each epoch processes the data in batches, not individual data points.

So, to answer your question, the model will iterate over 64 data rows at a time for 20 epochs, not over the entire 1024 data rows in each epoch.

Google:
An epoch consists of one full cycle through the training data. This is usually many steps. As an example, if you have 2,000 images and use a batch size of 10 an epoch consists of 2,000 images / (10 images / step) = 200 steps.