# Gestures-password-Swift

<html>
<body>
<h2>什么是 Gestures-password-Swift</h2>
<p>这是一个基于swift语言实现的手势解锁封装</p>

<h2>效果图展示</h2>

<h3>效果图1</h3>
<p><img src="picture/44867EAD-661E-47FB-BB43-A2B4C5CEC74F.png"/></p>

<h3>效果图2</h3>
<p><img src="picture/2DCEED84-0B4C-4991-BE9C-6E3ED1E11E8F.png"/></p>

<h3>效果图3</h3>
<p><img src="picture/0E0B7B00-18EF-4425-BE67-87FFADA677D0.png"/></p>

<h3>效果图4</h3>
<p><img src="picture/1AE0C451-5D56-4FD3-BBF0-89E81B293245.png"/></p>
<h2>使用方法</h2>
<h3>设置新密码的时候</h3>
<p>let passwordLock = NSUserDefaults.standardUserDefaults().objectForKey("passwordLock")</br>
        if let pass = passwordLock {</br>
            let alertView = UIAlertView.init(title: "提示", message: "您已经设置了手势密码", delegate: nil, cancelButtonTitle: "确定")</br>
            alertView.show()</br>
        }else{</br>
            let lockView = LockViewController()</br>
            self.presentViewController(lockView, animated: true, completion: nil)</br>
        }</br></p>
        
        
<h3>重置密码或者验证密码的时候</h3>
</body>
<p>let passwordLock = NSUserDefaults.standardUserDefaults().objectForKey("passwordLock")</br>
        if let pass = passwordLock {</br>
            let lockView = LockViewController()</br>
            //下面这个参数是用来说明是重置密码还是验证密码</br>
//            lockView.resetIs = "resetIs"</br>
            lockView.reset = "请输入原密码"</br>
            self.presentViewController(lockView, animated: true, completion: nil)</br>
        }else{</br>
            
            let alertView = UIAlertView.init(title: "提示", message: "您尚未设置手势密码", delegate: nil, cancelButtonTitle: "确定")</br>
            alertView.show()</br>
        }</br></p>
</html>