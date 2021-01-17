# Unit14: Deep Learning/Recurrent Neural Networks

#### Overview
In each of the notebooks, the same process was followed.
1. Load in, prepare, and combine the data into a dataframe.
2. Build, fit, train, and compile the LSTM model
3. Evaluate the results


#### Closing Predictor
In the closing predictor version, the previous prices was used to determine the new price.
This model was extremely accurate, as would be expected due to the correlation of prices in short time frame windows

#### FNG Predictor
The fear and greed model used the FNG index to predict new prices, and was not nearly as accurate as the closing predictor model.
This is more esoteric, so the lack of a short-term correlation is accuracy is not surprising.  However, since it is known that
fear and greed drive the market, there is evidence that either the index is not accurate, it would perform better over a longer
time frame, requires significant lag, or all of the above.

#### Questions:

##### Which model has a lower loss?
The closing predictor has a much lower loss than the FNG predictor in every window range.
Using price to predict price is clearly a better option than using an arbitrary index.

##### Which model tracks the actual values better over time?
The closing predictor is a very good tracker, where FNG is generally unusable.

##### Which window size works best for the model?
The window size is inversely related to the quality of the model.  As window size decreases, the loss decreases, making the model
stronger.  For price predictions, as indicated above, this is logical.  Or as my former boss liked to say, "The best predictor of the
short-term future is the near-term past".
