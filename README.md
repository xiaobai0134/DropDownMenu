# DropDownMenu
这是一个简单的下拉菜单
使用方法：
添加  #import "XBListView.h"

 NSMutableArray * tmpArray = [NSMutableArray arrayWithObjects:@"第一条",@"第二条",@"第三条",@"第四条",@"第五条",@"第六条", nil];
    
 XBListView * listView = [[XBListView alloc]initWithFrame:CGRectMake(100, 100, 100, 30) andWithDataSourceArray:tmpArray];
 
 [listView setSetSelectNum:^(NSInteger tmpTag)
 {
      NSLog(@"选中的选项是%@",tmpArray[tmpTag]);  
 }];
    
[self.view addSubview:listView];
