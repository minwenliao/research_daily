时间戳对齐：
get_frame() 

```python
img_left = self.img_left_deque[-1]
img_right = self.img_right_deque[-1]
puppet_arm_left = self.puppet_arm_left_deque[-1]
```
```python
frame_time = min(
    img_left.header.stamp.to_sec(), 
    img_right.header.stamp.to_sec(), 
    puppet_arm_left.header.stamp.to_sec(),
)
```
```python
while self.img_left_deque[0].header.stamp.to_sec() < frame_time:
    self.img_left_deque.popleft()
# 拿出同步时刻的图像
img_left = self.img_left_deque.popleft()
```