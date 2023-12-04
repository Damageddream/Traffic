

Convolutional and pooling

I experimented with using the same setup for convolutional layers, pooling, and hidden layers as we did in the handwriting detection lecture, but the results were not much better than a coin flip. Adding just another layer of convolution + pooling with all the same parameters raised the accuracy to 95%. Then I raised the size of filters for the convolution layers to 5x5, but the accuracy dropped to a stunning 5%. I also tried 2x2 accuracy was 92% sa high but lower than 3x3, i tried for testing purpose 1x1 but as i thoguht it just looks at every pixel 1 by 1 so it does not find any meaningful patterns, 4x4 have accuracy lower than 3x3 and 2x2. Intresting obersvation, when I left 3x3 in first conv layer and changed it to 2x2 in second accuracy raised to 96%. Adding one more layer of convo + pooling, lower accuracy so I leave it with 2 layers of convo + pooling, with 3x3 and 2x2. 

Rasing number of filters, lowered accuracy in first layer to 90% but in first and second to 67%. Lowering filters in 1st layer to 25, destroyed model with only 8% accuracy. Lowering filters to 25 in both layers, changed accuracy to 79%, so not much but a lot better than only in 1 layer, so maybe holding similar fliters in every layer is way to go. Lowering filters to 30 dropped accuracy to 90% but raising to 35 dropped it to 88%. 33 gives better results than 32, so i leave it at that. Lowering pools sizes, just lowers accuracy. There are small pictures, so probably we don't want to shrink them much more.


Hidden Layers

Halving numbers of hidden layers, halved results could expect that. After rasing it to 230, accuracy in training was noticibly higher but accuracy at the end was similar to earlier results, maybe sign of overfitting. After raising it to 300, accuracy was similar to 124, but at 400 it started dropping. With more expremienting i leave it at 360, because it gave best results.


Dropout
lowering droput to 0.3 from 0.5 didn;t change much just lowerd accuracy a little bit. Dropout at 0.7 so higher, lowered accuracy more than 0.3. 0.5 gave best results so i leave it at that. With ovveral accuracy at average 96.5%