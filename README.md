# Lhat-Communications-Standard  
> 欢迎使用Lhat的标准通信核心，这是一个**开源、安全、快捷、易上手**的通信核心。  
相信在我们的介绍后，你会停止犹豫使用什么样的通信核心的。  
## 什么是Lhat标准通信核心？  
就像上面所说的一样，除此之外，这个核心的实现是一个简单的Python模块文件。
只需要一个简单的`import chat_operations`就可以开始对该核心的探索之旅。  
## 如何使用Lhat标准通信核心？  
`import chat_operations`，这是你所要做的~~第一步~~，啊不是，第二步。  
首先，你要先克隆[Lhat官方存储库](https://github.com/3rdBit/Lhat)并在其中找到`chat_operations.py`。  
嗯，没错，这就是我们的通信核心了，看它是多么地小巧~~玲珑~~啊！  
当然，小巧了，说明你要写***更多**的代码来实现**更多**的功能*，这是*毋庸置疑*的。  
## 模块详细介绍  
嗯，既然准备好了，我们就开始吧！  
首先，四个核心函数，不要看仅仅有这么些就瞧不起它们，尽管它们不是很强大。  
### 几种被定义的消息类型  
TEXT_MESSAGE_ARTICLE：普通文本消息；  
USER_MANIFEST：在线用户列表；  
FILE_RECV_DATA：文件接收（仍为TODO，未开发）；  
不存在就会返回`UNKNOWN_MESSAGE_TYPE` 。  
### pack()函数  
`pack(raw_message: str, send_from, chat_with, message_type, file_name=None)`  
> 这是干什么用的？  
这是用于把普通的一些文本消息加上信息给结合成JSON消息的函数。  
> 打包消息，用于发送  
> :param raw_message: 正文消息  
> :param send_from: 发送者  
> :param message_type: 消息类型  
> :param file_name: 文件名，如果不是文件类型，则为None  
### unpack()函数  
`unpack(json_message: str)`  
> 加un了肯定就反过来了呗。  
没错。  
> 解包消息，用于接收JSON格式的消息  
> :param json_message: JSON消息  
> :return: 返回的东西有很多，也有可能是报错  
鬼知道返回值会返回什么，请查阅函数用法。  
### 其他函数  
剩下的函数都不与通信核心有太大关系，可以自行更改，它们都与Lhat的Qt界面有较大的耦合度。  
  
**Powered by 3rdBit Studio**
