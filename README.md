# TimeGAN Implementation
We implement TimeGAN for five large-cap stocks. TimeGAN consists of four neural networks: an embedder network to create a low-dimensional representation to learn relationships among features, a generator to create synthetic time series, a discriminator to identify the real and fake time series, and a recovery network to map the low-dimensional representation back to the ambient space. To aid in learning the temporal structure of the data, the true data is periodically used to perform supervised learning at each time step. The four networks are trained jointly using the traditional mini-max game, the reconstruction loss, and the supervised loss. With the resulting synthetic data, we show that it fails to retain all the properties of stock returns, and consequently, TimeGAN may not provide an avenue for data augmentation when the amount of data is not already large. 
