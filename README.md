# EVEText
单元测试作业


# **为什么要进行单元测试**

   #### 便于后期重构。单元测试可以为代码的重构提供保障，只要重构代码之后单元测试全部运行通过，那么在很大程度上表示这次重构没有引入新的BUG，当然这是建立在完整、有效的单元测试覆盖率的基础上。
   #### 优化设计。编写单元测试将使用户从调用者的角度观察、思考，特别是使用TDD驱动开发的开发方式，会让使用者把程序设计成易于调用和可测试，并且解除软件中的耦合。
   #### 文档记录。单元测试就是一种无价的文档，它是展示函数或类如何使用的最佳文档，这份文档是可编译、可运行的、并且它保持最新，永远与代码同步。
   #### 具有回归性。自动化的单元测试避免了代码出现回归，编写完成之后，可以随时随地地快速运行测试，而不是将代码部署到设备之后，然后再手动地覆盖各种执行路径，这样的行为效率低下，浪费时间。
   #### 首先，带来自信。在接手一个新的项目，或者说是参与一个新的项目开发时，往往这种情况是你半途参加进去的，你需要对已有的代码结构进行解读和理解，对于业务的理解，对于代码个中各个模块关系的理解。如果一开始就理财出错，很可能修改后的代码会引起更多的BUG出现，到那时候又需要修复更多的BUG，改了一个地方，很有可能会莫名其妙地影响另外一个地方，这种现象是很常见的。还有一种情况，假设你修改的功能没问题，但是需要去测试验证，在测试的时候就需要考虑这个功能点它原有的测试路径有哪些，又需要一一去验证功能路径，以证明本次修改对于已存在的功能点不造成影响。这其中就存在着很大的时间成本，导致效率不高。那是否存在着这么一种方式，我需要修改我想改动的地方，不需要关心修改完之后它所造成的影响，也不需要关心它的测试回归性，有，此时就是单元测试登场的时候。写单元测试代码，可以让我自己写的代码足够自信，它是经得起考验的。
   ####  其次，更快反馈。对于有一定编程经验的开发人员来说，当他拿到一个新需求的时候，首先想到的不是动手 Coding ，而是会先想想代码的结构，有些类，数据结构该是如何，然后才开始敲代码。如果没有单元测试，一般流程基本是这个模块功能全部写完才开始测试，比如利用 MVP 架构的功能。一般都是开始 Model 模块,然后完善 Presenter 模块，最后写 View 模块，等这几个模块都写完了，再把 APP 跑起来，验证自己写的功能模块是否符合需求，没有符合则继续回去修改代码，这中间需要花费很长的时间才能知道当下自己写的代码是否符合要求，是否正确。那有没有一种即时反馈的方式呢，有，写单元测试即可，当你写完一个函数，马上就匹配一个单元测试函数，这样即写即测的方式可以保证你当场写的代码马上进行修改，测试通过一个，就表示完成一个小的功能点，最后，把函数组装起来，就是我们想要大的功能点。
   #### 最后，节约时间。对于 Android 开发来说，一遍一遍的运行 APP ，然后执行相应的用户操作，看界面是否正确的显示，通过这种方式来测试功能，其实是非常浪费时间，而且效率不高，而用单元测试，可以几乎不用打开 APP 来执行，当然有些需要一些资源文件的是需要 APP 运行条件，绝大部分的功能在单元测试阶段就能验证完毕，那么速度就相对快很多。此外，单元测试还能帮忙减少 BUG ，从而减少调试 BUG 的时间，一些低级犯的错误在单元测试阶段就能避免掉。
   
  #### 单元测试保证局部代码的质量，单元测试在隔离的前提下，分别对各个代码单元进行测试，能够达到其他测试不可能达到的测试完整性，从而保证了局部代码的质量。只有局部代码的质量得到了保证，软件产品的质量才可能得到保证。

  ## 单元测试改良项目代码的整体结构
  #### 要对代码进行单元测试，最起码的前提是代码能够隔离，也就是说，要具有一定的可测性，因此，单元测试是一种有效的约束机制，这种机制将有效地改良代码的整体结构。例如，如果把业务代码直接写在界面类中，将很难进行单元测试，随意的不合理的紧耦合也会造成难于测试，单元测试使这些不好的特性得于及时发现，从而很容易进行修正。可测性是高质量代码的首要特性，不具有可测性，也就无法衡量代码的正确性，有了可测性，也就基本上保证了代码的可扩展性、可复用性。

## 单元测试降低测试、维护升级的成本
#### 错误越早发现，修复的代价越小，另一方面，如果代码经过了充分的单元测试，集成测试和系统测试就只需要关注设计方面的问题。自动回归测试也大量降低升级维护成本。

## 使开发过程适应频繁变化的需求
#### 单元测试自然地使开发流程变得“敏捷”，这是因为，整体结构良好的代码具有较好的可扩展性，自动回归测试又能保证修改不会引入新的错误，因此可以适应频繁变动的需求，降低系统分析、架构设计和后期测试的压力。

## 单元测试有助于提升程序员的能力
#### 对程序员来说，单元测试有利于养成缜密的思维习惯，及提高设计能力。





---

白盒测试法测冒泡排序法
        1.冒泡排序法Java源代码

   /*
 * 冒泡排序
 */
public class BubbleSort {
　　
 
   public void BubbleSort(int[] arr){
 
　　　　for(int i=0;i<arr.length-1;i++){//外层循环控制排序趟数
　　　　　　for(int j=0;j<arr.length-1-i;j++){//内层循环控制每一趟排序多少次
　　　　　　　　if(arr[j]>arr[j+1]){
　　　　　　　　　　int temp=arr[j];
　　　　　　　　　　arr[j]=arr[j+1];
　　　　　　　　　　arr[j+1]=temp;
　　　　　　　　}
　　　　　　}
　　
        //输出
 
        System.out.println("排序后数组元素为:");
        for(int num : arr){
 
           System.out.print( num + "  " );
 
           }
       }　　
 
 
}
 2.冒泡排序法程序流程图
![avatar](https://img-blog.csdnimg.cn/20190420162306850.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0dlb29vbw==,size_16,color_FFFFFF,t_70)









