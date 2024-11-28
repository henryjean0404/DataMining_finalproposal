# Environment setting

實驗環境的部分，我們是使用anaconda去跑實驗，所以有附上environment.yaml和requirements.txt，兩種方式可以重現出我們做實驗的環境。主要是torch-geometric的版本，原作者使用的是2.3.1，但在我們安裝環境時，2.3.1會有一些bug，導致實驗無法順利進行，
所以我們改用2.0.1，就可以順利執行了。

# Run code

執行main.py
```
python main.py --dataset=amazon
```
dataset可以選擇amazon, dblp, lj, youtube，相關的檔案有附在dataset的資料夾中。

# 修改code

我們主要修改的部分在rewriter_core.py中的class GCN，我們有把所有修改過後的activation function和hidden layer的調整註解起來，也包含了原論文所使用的ReLU + one hidden layer的做法。
在執行前，先決定要做哪一個Neruel Network，把想要執行的那一行code的註解拿掉並且把上一輪執行的那一行註解起來就可以了。
(例:假設執行完ReLU + two hidden layer後，接下來要測試SiLU + one hidden layer，把ReLU + two hidden layer那一行註解並且把SiLU + one hidden layer那行的註解拿掉即可。)





  
