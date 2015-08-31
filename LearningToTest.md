Learning to Test - Accelerating C Compiler Testing
---
*update:2015-08-30 under_construction*  
[1.Introduction](#1) [2.Features](#2) [3.Data](#3) [4.Contributors](#4)
###<h2 id="1"> Introduction </h2>
We propose the idea of learning to test, meaning to learn from previous test cases that trigger bugs and use the learned model to prioritize new test cases. Based on this idea, to accelerate C compiler testing, we propose LET, a learning-to-test approach, which utilizes the characteristics of existing test programs triggering bugs to schedule the execution order of new test programs. In particular, our approach first trains a prediction model from existing test programs to model the characteristics of test programs that trigger bugs. Then based on the prediction model, our approach schedules the execution order of new test programs through clustering. That is, through an offline learning process and an online scheduling process, the proposed approach determines an execution order of test programs with the aim of accelerating testing. We present an overview of LET as follows.
![](./image/pro.png)
###<h2 id="2"> Features </h2>
The features that we used are described in a file, which can be downloaded from the following link.  
[DownlaodLink](./file/l2t.features.pdf)  
###<h2 id="3"> Data </h2>
The experiment data in our study can be downloaded from the following link.   
[DownlaodLink](./file/l2t.results.xlsx)  

###<h2 id="3"> Contributors </h2>
Contributors to the implementation of LET are:   
Junjie Chen   
Wenxiang Hu   
Yanwei Bai   