# pull-request

一开始，master上什么都没有，除了这个README.md

新建feature/task特性分支，用于开发task功能。
--player1

新建feature/friend特性分支，用于开发friend功能。
--player2

下面介绍pull-request的用法

用到的工具下载（有windows版本和mac版本），https://desktop.github.com/

1、首先，fork需要开发的项目, 每个人在自己的名字下的项目中进行开发, 并不直接修改目标项目

![](image/fork.png)

github desktop里把自己名字下的项目clone下来

![](image/clone.png)

2、现在开始（新成员接入，开发者1），1号开发者开始开发一个新功能task。新建特性分支，feature/task（注意，这个分支是从自己的master上切出来的, 事先和主项目的master同步）

![](image/2.png)

3、task特性开发完成后，为了将代码合并到主项目，如下图，先commit代码，然后publish，最后提交pull-request请求(此处publish相当于push操作)

![](image/3.png)

4、pull-request操作时候，将本次提交内容的详细说明，填写到描述栏中（此处没有填入，这个需要避免），然后完成提交

![](image/4.png)

5、到这一步，开发者1的工作告一段落，此时开发者1需要找到相应的reviewer来对他的代码进行review，假设开发者1找到了reviewer1来看他的代码（新朋友加入，大家鼓掌欢迎...）,reviewer1打开工具，点击sync按钮，更新代码后，切换到feature/task分支下，此时看到pull-request按钮变成浏览状态，点击按钮进入pull-request详细页面

![](image/5.png)

6、下图为pull-request详细页面，由于开发者1这个家伙没有功能说明，reviewer1看代码很辛苦，要求开发者1提供开发说明

![](image/6.png)

7、开发者1收到吐槽后，及时提供了开发说明，供reviewer1查看

![](image/7.png)

8、reviewer1此时对task功能进行review，其中发现了一些问题，同时打上批注，让开发者1进行修改(reviewer看代码其实应该在eclipse等开发工具中查看，比较方便，发现问题点击files changed按钮，找到对应的文件，提交修改意见)

![](image/8.png)

9、开发者1收到修改意见后，对代码进行修改，同时将修改sync出去

![](image/9.png)

10、reviewer1看到开发者1已经修改了对应的代码，并且没有其他问题了，此时提交一条comment，说自己已经完成了review，没有问题，如果没有其他的reviewer，则开发者1进行合并代码操作merge pull request（此时如果有2号reviewer，则让2号进行review），到这里，一个功能就已经完成了。

![](image/10.png)

11、这里介绍稍微复杂的情况，假设开发者1在开发task功能时候，同时开发者2在开发新功能friend，此时开发者2已经新建friend分支，提交代码，同时提交pull-request

![](image/11.png)

12、此处假设review工作已经完成，开发者2需要进行合并代码操作，因为在task功能合并完后，friend分支跟最新的master分支已经有冲突，此时需要开发者2解决冲突

![](image/12.png)

13、如下图，开发者2先将代码更新下来，然后合并当前最新的master分支（update from master），解决冲突（解决冲突可以使用其他工具解决），然后commit解决冲突后的代码，再sync更新后代码。

![](image/13.png)

14、再次查看pull-request，此时发现冲突已经解决，然后合并代码呗，开发者2进行合并代码操作merge pull request

![](image/14.png)

15、这里看一下最新的master，2次特性开发都已经合并到最新的master中了

![](image/15.png)

以上
