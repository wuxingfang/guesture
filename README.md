# H5单页面手势滑屏切换示例

- 手指在屏幕上滑动时，页面跟随移动
- 当手指离开屏幕时，计算手指在屏幕上停留的时间
   
- 如果停留时间小于300ms，则认为是快速滑动切换，页面切换到下一页

- 如果停留时间大于300ms,则认为是慢速滑动，慢速滑动按如下规则处理：
- 如果滑动距离小于屏幕宽度的50%，则回退到上一页
- 如果滑动距离大于屏幕宽度的50%，则切换到下一页 

## 对于多手指触摸操作：  
- 第一个手指触摸时，正常滑动  
- 第二个手指按下时，不做任何响应操作，继续原有的滑动  
- 当任意一个手指离开屏幕时，结束滑动，剩余的手指操作不做任何处理  
- 当第二个手指再次按下时，触发新的滑动开始，但由于获取的是touches[0],因此，第一个手指移动才会引起页面的滑动  
- 支持多手指同时按下时进行滑动
 
