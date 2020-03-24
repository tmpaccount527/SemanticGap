# This project contains the code and data for a manuscript submitted to IEEE Transactions on Industiral Informatics. We build a GCN to close the semantic gap beween customers and engineering teams in smart manufacturing.


1. Some explanation :
	use mask to indicate samples used in the train/val/test set , set the corresponding index to 1

2. Files changed in order to suit this project:

	models.py:
		class GCN--->function _accuracy()
		change self.pred from tf.argmax to tf.nn.top_k in order to get top-5 evaluations in our project

	train.py 
		comment original evaluation part(which only consider top1), use new evaluation metrics(top-5 evalutation)
	
3.  requirement: Python 2.7 or 3.6; Tensorflow >= 1.4.0

new dataset name is 'laptop_cpu' ,'laptop_hd','laptop_gpu','laptop_screen','laptop_ram'

use the following command to get result:
python train.py laptop_cpu
python train.py laptop_hd
python train.py laptop_gpu
python train.py laptop_screen
python train.py laptop_ram

!!Note: please check train.py first, a code block is for command line and another is for run in spyder. Check before run it!

-----------Instructions for new dataset:
1. prepare file in folder ./data and ./data/corpus, for example, dataset name is laptop_cpu
prepare file laptop_cpu.txt under folder ./data and ./data/corpus
./data/laptop_cpu.txt
./data/corpus/laptop_cpu.txt

2. run the command accordingly
