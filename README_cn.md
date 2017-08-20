# 深度学习与机器学习的学习路线

>对于一个刚刚进入深度学习和机器学习领域的新手，面对如此多的课程和资料，如何选择正确的课程和书籍开始深度学习之旅成了他们面临的头等难题。

>这是我们关于深度学习和机器学习资源的学习路线。

这个学习路线中包括一些评价很高的课程，书籍还有论文，通过学习它们，我们能够很快进入到机器学习和深度学习的领域中。也许一些课程或者书籍比较困难，但是它们真的值得我们认真去学习和阅读。

我将会继续往这个学习路线中添加内容，如果你有一些推荐的内容，比如一些新的课程和学习笔记，欢迎向这个github提出PR。
- - -

# 课程

# 给码农的实用深度学习, part 1 & 2
这门课程是为那些至少有一年编程经验和还记得高中数学的人设计的。在第一部分，将会学习如何搭建达到最高水准的模型，这并不需要大学水平的数学内容。在第二部分，将会学习最新的深度学习发展，如何阅读和实现学术论文，以及如何解决具有挑战性的，例如神经机器翻译等端到端的问题。

[part1 course site](http://course.fast.ai/)

[part2 course site](http://course.fast.ai/part2.html)

[github](https://github.com/fastai/courses)


## 深度学习专项课程(deep leanring.ai)
这个专项课程有5门课程组成，你将会学习到深度学习的基础，理解如何建立神经网络，学会如何成功的完成机器学习项目。这个专项课程非常流行，因为其是由吴恩达教授的，吴恩达此前在coursera上的课程，机器学习也非常流行。

[course site](https://www.coursera.org/specializations/deep-learning)

## CS 20SI:  TensorFlow 做深度学习研究 
这门课程将会覆盖在深度学习研究中使用tensorflow的基础和使用方式。我们致力于帮助学生理解tensorflow中的计算图，探索其提供的函数，学会如何建立最适合深度学习项目的结构化模型。通过这门课，学生将会学会如何用tensorflow建立不同复杂度的模型，从最简单的线性/logistic回归，到卷积神经网络，用LSTM建立循环神经网络来解决例如词嵌入，机器翻译，光学字符识别等任务。学生能够通过结构化模型和管理研究实验得到最好的体验。

[course site](https://web.stanford.edu/class/cs20si/)

[github](https://github.com/chiphuyen/stanford-tensorflow-tutorials)

[video list](https://www.youtube.com/watch?v=g-EvyKpZjmQ&index=1&list=PLSPPwKHXGS2110rEaNH7amFGmaD5hsObs)

## 数值线性代数
这门课程主要希望解决**我们如何能够以一个较快的速度、较高的准确率进行矩阵计算？**

这门课程在2017年 University of San Francisco 科学计算暑期项目中。

[github](https://github.com/fastai/numerical-linear-algebra)

[video list](https://www.youtube.com/playlist?list=PLtmWHNX-gukIc92m1K0P6bIOnZb-mg0hY)

## 机器学习基石-林轩田
这门课教授机器学习中最基本的理论算法和实用工具。在中文机器学习领域，这门课得到了很高的评价。

[course site](http://www.csie.ntu.edu.tw/~htlin/mooc/)

## 机器学习技法-林轩田
这门课是机器学习基石的后续课程，主要介绍机器学习算法的基础、设计和分析，还介绍一些机器学习的实际应用。

[course site](http://www.csie.ntu.edu.tw/~htlin/mooc/)

## 从数据中学习(Learning From Data)
这门课将对机器学习中的基本理论，算法以及应用做介绍。这门课会在理论与实际应用上做平衡，覆盖一些数学的推导和启发性算法。

[course site](http://work.caltech.edu/telecourse.html)

[video list](https://www.youtube.com/watch?v=mbyG85GZ0PI&list=PLD63A284B7615313A&index=1)

## 优达学城：深度学习
我们将会学习如何训练优化基本的神经网络，卷积神经网络和长短时间记忆网络。我们也会经由项目和作业介绍出TensorFlow中完全的学习系统，也会学习解决课程中出现的新的困难的问题，随着使用深度学习的方法解决这些复杂问题的同时，对复杂的人脑智能有更好的理解。

[course site](https://www.udacity.com/course/deep-learning--ud730)

[github](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/examples/udacity)


## cs229
这门课提供了机器学习和统计模式识别的广泛介绍，因为老师是斯坦福大学的教授吴恩达，所以这门课非常出名。

[course site](http://cs229.stanford.edu/)

## 机器学习中的神经网络
这门课让我们学习人工神经网络以及理解如何将其应用到机器学习中，比如语音识别，目标识别，图像分割，语言模型以及检测人体动作等等。除了强调基本算法，也会讲解实际使用中的技巧。

[course site](https://www.coursera.org/learn/neural-networks)

## cs231n：图像识别中的卷积神经网络
这门课会深入到卷积网络结构中的细节，主要是学习端到端的模型，特别是对于图像分类的任务。

[course site](http://cs231n.stanford.edu/index.html)

## cs224n：自然语言处理中的深度学习
这门课提供了将深度学习应用到自然语言处理中一个完整的介绍，在模型的部分，将会介绍词向量的表示，基于窗口的神经网络，循环神经网络，长短时记忆网络模型(LSTM)，递归神经网络，卷积神经网络，以及最近一些含有记忆成分的模型。通过课程内容和编程作业，学生能够学到基本的工程能力，能够用神经网络处理实际问题。

[course site](http://web.stanford.edu/class/cs224n/)

## Dave Silver 强化学习课程
开发 AlphaGo 的公司 DeepMind 的首席研究员 Dave Silver 的强化学习介绍课程。

[course site](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html)

[video list](https://www.youtube.com/watch?v=2pWv7GOvuf0&list=PLzuuYNsE1EZAXYR4FJ75jcJseBmo4KQ9-)

## cs294: 深度强化学习
由Berkeley大学教授 Sergey 开的深度强化学习课程。

[course site](http://rll.berkeley.edu/deeprlcourse/)

## 凸优化
这么课主要是让研究生水平的学生了解到优化问题的基础，增加算法性质的理解。主要针对的是凸优化问题，虽然也会介绍一些非凸优化问题，同时也会介绍优化算法在统计和机器学习中的应用。完成这门课程之后，学生能够学会如何解决一个优化问题。

[course site](http://www.stat.cmu.edu/~ryantibs/convexopt/)

## 统计机器学习
这门课将会结合理论知识和实际方法，帮助学生在自己的研究领域针对合适的方法开发出适用的工具，主要包括机器学习研究中很重要的统计理论，还包括非参数理论，统一性理论，最小最大估计以及浓度测量。

[course site](http://www.stat.cmu.edu/~larry/=sml/)

## 概率图模型
CMU教授 Eric Xing 的概率图模型介绍课程。

[course site](http://www.cs.cmu.edu/~epxing/Class/10708-14/lecture.html)

## MIT 5.S094：无人驾驶中的深度学习
这门课程介绍了如何应用深度学习算法开发无人驾驶汽车，并为初学者开放。虽然这门课是为机器学习的新手开发的课程，但是对一些高级研究者在深度学习应用和方法上也有一定帮助。

[course site](http://selfdrivingcars.mit.edu/)

## CSE 599G1: 深度学习系统
构建和优化深度学习系统的研究如今在学术界和工业界都是一个非常活跃的领域，但是现在却没有一门课程专门教授这些知识。这门课程就是为了填补这个空缺而设计的。我们将会学习到深度学习系统中的很多方面，包括深度学习基础，机器学习表示的编程模型，自动微分，内存优化，分配，分布式学习，硬件加速，主流的语言和模型部署。

这么课是由MXNet的主要开发者之一陈天奇在华盛顿大学开的课程，值得学习。

[course site](http://dlsys.cs.washington.edu/)

# 书

## 模式识别与机器学习

## 机器学习-周志华

## 机器学习-Yaser

## 数值优化
