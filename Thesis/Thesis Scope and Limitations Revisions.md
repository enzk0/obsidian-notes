sir [@Jordan](https://www.facebook.com/messages/t/631883661), here are the specifics hehe. murag lengthy gyud sha sir hahah Specific Issues/Topics - initial experimentation (training and eval of RNN, LSTM, GRU, Transformer) already consumed 100+hrs - training time of RDDLGN is longer than expected - current implementation of RDDLGN yields slow learning (still working on this) - possibility that RDDGLN might not perform well - realized that the evaluation of GRU also provides contributions in RNN research aside from RDDLGN - evaluated transformer even though it was beyond our scope (we would like your advice on this) - unknown timeline for final defense - lengthy experimentation process, and so mag ask mi na maybe kami ang last presenter hehe

Good afternoon Sir [@Jordan Canete](https://www.facebook.com/messages/t/631883661), We would like to inform you about our planned changes to the research process due to resource and financial issues related to our project. We intend to remove RDDLGN 256K from the models to train and evaluate and will only train RDDLGN 64K due to constraints, in time, resources, and finances due to length training and evaluation required by the RDDLGN architecture. As it stands now, at worst, we expect to spend at most, 1600 compute hours to train and evaluate RDDLGN 64K. Because of this, we also intend to cut down the number of max epochs from 1000 to 250 to cut down in training and evaluation time and make the project feasible. Moreover, based on our initial experiments and results, we have observed marginal improvement start at epoch 150 an onwards and because of this, we believe that this adjustment is justifiable.

What changed in our research so far:
- Included Transformer in models to be evaluated. All models evaluated are:
	- RNN
	- LSTM
	- GRU
	- Transformer
	- RDDLGN(64k)
- Removed RDDLGN(256k) as a model to be evaluated due to time constraints and limited resources.
- In training RDDLGN(64k), the methodology changed to:
	- from 1000 epochs to 250 epochs
	- from 546-4k(?) batch size to 2k-4k(?) batch size
- All model trainings are done in Google Colab instead of personal hardware. This is to complete the training in a faster rate, promote collaboration for training between researchers