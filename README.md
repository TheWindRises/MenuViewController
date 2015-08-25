# 滚动视图
=====
这是一个简单实现滑动视图的控制器，实现在一个视图中能够滚动视图。实现的时候只要完成以下三步就可以使用了：
>1.给子视图设置相关的标题和子控制器<br>
 _menuvc = [[MenuViewController alloc] initViewControllerWithTitleArray:@[@"首页",@"动态"] vcArray:@[marsterVc, dynamicVc]];<br>
2.设置大小，这里规避的是导航控制器(49)和标签控制器(64)<br>
 _menuvc.view.frame = CGRectMake(0, 64, self.view.frame.size.width, [UIScreen mainScreen].bounds.size.height - 64 - 49);<br>
3.将视图加到相应的视图<br>
 [self.view addSubview:_menuvc.view];<br>
 
 
