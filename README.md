# 最新版本
 v1.0

使用Androidx
# 
### 方法介绍
### boolean isTimer()

#### 获取是否正在倒计时

_true：正在倒计时_

_false：倒计时未开始_
#
### void setTimerLisenter(final int buttonType, int timerTime, final TimerLisenter timerLisenter)

#### 设置监听器
buttonType：按钮类型
``
BUTTON_TIMING:定时按钮 ``  `` BUTTON_TIMER：倒计时按钮    
``

timerTime：倒计时时间 ``单位:秒``

timerLisenter: 倒计时监听

```
timingButton.setTimerLisenter(TimingButton.BUTTON_TIMING, 6, new TimingButton.TimerLisenter() {
            /**
             * 
             * @param time 剩余时间（秒）
             */
            @Override
            public void clocking(int time) {
                //正在倒计时 
            }

            
            @Override
            public void timerOver() {
               //倒计时完成
            }

            @Override
            public void onClick(boolean state) {
                //倒计时按钮点击
            }
        });
```
#
### void start()
#### 开始倒计时
#
### void stop()  
#### 倒计时停止