# Automatic_photo_correction
- 我个人喜欢写东西的时候把中间结果存成文件。。。
- 这样的话我可以把工作分成一段一段的。。。不容易弄混。。。如果不习惯的话可以把它改成一个文件。

---

- 我。。。。。代码丢了一半？?????
- 
- 已哭晕在厕所。。。 = = 以后项目一做完就传到GitHub吧。。。
- 
- 谁让我手贱以为保存了，就把原版删了。。。留下来的都是中间测试的时候用的。。。
- 
- 没有批量文件的传入传出。。有些细节也不一样。。。。
- 
- 最近要考试没时间重写了。。。传仅存的半份中间文档吧。。。。。
- 
- ---
- 我是用Face_recognition探测到面部数据。
- 然后根据眼睛和鼻子的位置计算倾斜角度。
- 最后根据倾斜角度，旋转并裁剪图片。。。
- （裁剪图片的时候，opencv-python好像没有copy的函数了。我记得我最后直接用矩阵操作的x[:] = y[:]实现的。而不是现在文件里的for循环，for循环特别慢）。
- landmark.py 里是将rootDit文件夹中的所有图片用Face_recognition探测到的面部数据，并保存在val.txt文件中。
- rotate_degree里是读取val.txt（这部分没有）里的数据，并计算出对应的需要旋转的角度。
- 这个文件里的有点问题，计算角度的时候不需要加绝对值的。因为角度是有正负的。。我的最终版改了。。这里面没改。
- 文件里的数据,不是读取的，，是我在测试的时候用的。。。
- 需要注意的是左眼右眼的对应位置的数据不是对称的，需要对应下角标。
- 这个文件里还是用for循环实现的，，，我当时最新的里面是用map解决的下角标不对称。
- 最后rotate_and_cut里面是根据得到的旋转角对图片进行旋转，然后裁剪的。。。
- 同样文件里的数据不是最新的，因为图片的像素不同，人脸在图片中的比例也不一样，所以怎样
- 才能裁剪成适合的尺寸，当时调整了好久。。。然而。。。
- 并且读取文件夹的那部分也没有了。。。。。
- 提取前景部分也灭有了

---

凑合看吧。。。有时间看看再把这个补全。。。

这差不多是我做的第一个小项目，虽然不大。但是让我对图像的认识深刻了不少。

face_recognition的人脸检测好像不能用gpu。。。所以速度不是很快。

但是效果非常非常棒！
