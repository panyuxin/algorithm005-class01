学习笔记
最长公共子序列这里，超哥讲的是从最后一个字符来比较（自底向上），但是程序中是从i=1开始遍历的。可不可以理解为，从最后一个字符串比较想要得出的是自底向上递推公式，但是由于我们在dp中存储了状态，决定了我们需要从字符串头开始进行计算？
自底向上即i -1逐步递推，自顶向下是i + 1。类似问题像台阶，我们用自底向上的方法更容易得到递推公式。而这个递推公式其实是可以用递归去拆解的，即从i = str.length - 1开始，i - 1递归直到i = 0. 但是利用状态数组，我们不用一步步递归到i = 0才开始返回，而是直接从i = 0开始计算。也就是说动态规划是用递归的解决思路+中间状态存储?