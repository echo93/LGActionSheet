# LGActionSheet
之前的项目里封装的一个简单的ActionSheet,类似微信的那种, 终于有空把他弄到GitHub上

把三个文件拖进项目里,并引入 LGActionSheet.h头文件

注: UIDefines.h这个文件几乎项目中都要类似的,可以用自己项目里的替换
// 两行代码搞定
-(void)buttonClicK:(UIButton *)button{ 
  // 创建 
  LGActionSheet *actionSheet = [[LGActionSheet alloc] initWithTitle:nil subTitles:@[@"加为好友",@"拉黑",@"举报",@"拉黑并举报",@"删除"] delegate:self]; 
  // 显示 
  [actionSheet show];
}

// 需要遵守LGActionSheetDelegate协议
-(void)actionSheet:(LGActionSheet *)actionSheet clickedAtIndex:(NSInteger)buttonIndex{ 
  // 做想做的事 
  NSString *title = actionSheet.subTitles[buttonIndex]; 
}
可以自己设置标题和子标题的字体,颜色; 也可以在.m里直接修改默认,包括背景色,分割线颜色,选中背景色,遮罩等
