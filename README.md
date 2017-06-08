# LGActionSheet 旨在简单好用
封装的一个简单的ActionSheet,类似微信的那种简单的ActionSheet
引入头文件LGActionSheet.h 遵守协议LGActionSheetDelegate

注:UIDefines.h里面的宏大部分项目都有,可以用自己项目的替换

标题,子标题字体颜色都可以自定义,也可以在.m文件中直接修改默认值
- (void)buttonClicK:(UIButton *)button{

    // 创建
    
    LGActionSheet *actionSheet = [[LGActionSheet alloc] initWithTitle:nil subTitles:@[@"加为好友",@"拉黑",@"举报",@"拉黑并举报",@"删除"] delegate:self];
    
    // 显示
    [actionSheet show];
    
}


- (void)actionSheet:(LGActionSheet *)actionSheet clickedAtIndex:(NSInteger)buttonIndex{
    
    // 做想做的事
    
    NSString *title = actionSheet.subTitles[buttonIndex];
   
   NSLog(@"%@",title);
}
