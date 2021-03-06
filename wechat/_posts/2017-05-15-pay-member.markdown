---                 
layout:     post                 
title:       "20170515专题：支付会员"                     
date:       2017-05-15 19:00:00                   
author:     "PaymentGroup"            
tag:		[publish]   
                  
---                 
      
## 一、专题分享      
很荣幸给大家做这次的分享。我先自我介绍一下，我叫龚正，目前在滴滴金融工作。也是刚来不久，之前在美团和美丽说做支付相关的工作。所以今天 给大家介绍一下支付业务中支付会员相关的内容。   
![20170515_193139](http://static.cocolian.org/img/2017/20170515_193139.png)   
![20170515_193154](http://static.cocolian.org/img/2017/20170515_193154.png)   
我们都知道，支付体系中 如何识别一个用户 是有多种策略的。第三方支付也好 电商也好。但是 这个维度的不同 所建立的会员体系也是不同的。一般看来 第三方中的支付会员体系独立于 电商等业务，所以 我们下面对三个方面进行讲解：   
![20170515_193423](http://static.cocolian.org/img/2017/20170515_193423.png)   
![20170515_193441](http://static.cocolian.org/img/2017/20170515_193441.png)   
![20170515_193452](http://static.cocolian.org/img/2017/20170515_193452.png)   
业务系统在接入支付系统后，一般来说是需要做一个支付账户转换。会员系统中的会员 代表着这个用户在支付系统中的唯一身份。而以这个身份来产生的所有信息，都是这个会员的资产。一般来讲 一个或多个用户 对应一个支付会员。   
![20170515_193635](http://static.cocolian.org/img/2017/20170515_193635.png)   
而会员信息 分为两种：(ppt上不够细化)第一种是 资产;第二种是 信息。   
资产 一般包含用户的身份信息 昵称 会员密码等 也包含用户的手机号等。   
信息一般认为是会员的状态 如激活 冻结以及他产生的一些动作等信息。   
好了 我们对支付会员所拥有的信息有了了解 我们再深入一下 细节：   
![20170515_193924](http://static.cocolian.org/img/2017/20170515_193924.png)   
支付密码我们都非常的了解，每天都在用。所以我们来聊聊支付密码。   
![20170515_194018](http://static.cocolian.org/img/2017/20170515_194018.png)   
图上是我们最常用的支付宝和微信的支付密码输入图。当然还有线下的ATM啦，等等，都在使用6位支付密码。所以 大家都会有疑问，为什么我们的支付密码都是六位呢？   
![20170515_194137](http://static.cocolian.org/img/2017/20170515_194137.png)   
PPT中分了三点：防止暴力破解、增加用户体验、方便记忆。之前的支付宝以及银行都尝试过不同位数的支付密码，但是由于长度过长的不方便 ，效率低下，长度过短的，太容易破解   
都使用了6位支付密码。   
![20170515_194343](http://static.cocolian.org/img/2017/20170515_194343.png)   
一般来说，支付密码验证的过程是这样的：前端通过加密密码，传递到后端解密，然后使用hash算法算取hash值与后端保存的密码hash进行比较，最后返回成功还是失败。而在密码传输、密码hash中，都是用了安全级别比较高的算法。PPT中简述了一般加密使用的算法。而密码的保存，一般也是使用随机盐的方式，保证会员密码的安全性。   
![20170515_194650](http://static.cocolian.org/img/2017/20170515_194650.png)   
我们现在使用iphone非常的多 所以指纹支付也是非常的普及。很多android手机也大部分普及了指纹支付，这对我们的用户体验有了更大的提升。   
![20170515_194749](http://static.cocolian.org/img/2017/20170515_194749.png)   
指纹支付流程很简单。通过硬件判断是否成功，优势和劣势大家一想便知。所以，在风控方面考虑。指纹密码验证的安全性要低于6位支付密码的验证。   
![20170515_194900](http://static.cocolian.org/img/2017/20170515_194900.png)   
手势密码我们也很常用。   
![20170515_194926](http://static.cocolian.org/img/2017/20170515_194926.png)   
![20170515_194939](http://static.cocolian.org/img/2017/20170515_194939.png)   
还有一种是免密支付。虽然不需要输入密码 但是依然是通过用户的行为“指纹”来进行判断。   
![20170515_195038](http://static.cocolian.org/img/2017/20170515_195038.png)   
实名体系对于支付系统，乃至第三方来讲都是非常重要的。   
![20170515_195120](http://static.cocolian.org/img/2017/20170515_195120.png)   
![20170515_195138](http://static.cocolian.org/img/2017/20170515_195138.png)   
为了保证资金安全，实名对于第三方公司来说，是至关重要的。包括监管要求、用户安全、以及深度业务的拓展。   
![20170515_195233](http://static.cocolian.org/img/2017/20170515_195233.png)   
第三方支付中，实名账户分成三类，每种类型都有不同的限额。   
![20170515_195323](http://static.cocolian.org/img/2017/20170515_195323.png)   
![20170515_195335](http://static.cocolian.org/img/2017/20170515_195335.png)   
一般支付公司实名主要通过银行卡、通过银行通道对用户进行实名。但是我们发现，越来越多的第三方需要我们传递身份证信息，这也是为了增加三类实名的比例。   
当然啦，通过其他证件如港澳通行证等，以及 查询公积金、缴纳电费等，都可以实名。   
![20170515_195534](http://static.cocolian.org/img/2017/20170515_195534.png)   
这个是提供实名查询功能的公司。价格和实名级别都有所不同。   
![20170515_195619](http://static.cocolian.org/img/2017/20170515_195619.png)   
如下案例：   
![20170515_195634](http://static.cocolian.org/img/2017/20170515_195634.png)   
![20170515_195654](http://static.cocolian.org/img/2017/20170515_195654.png)   
![20170515_195705](http://static.cocolian.org/img/2017/20170515_195705.png)   
虽然本次分享没有完全把支付系统中的支付会员相关的知识完完全全的讲述给大家，但是从本次分享中 我们也知道了会员系统在支付系统中是至关重要的。   
对于我们支付系统的发展 以及配合监管 是不可或缺的一部分。   
![20170515_195848](http://static.cocolian.org/img/2017/20170515_195848.png)   
本次的分享就讲完啦，谢谢大家。[文中涉及的PPT下载地址](http://static.cocolian.org/img/hydra支付业务系统-会员系统.pdf)   
   
      
## 二、Q&A      
      
Q：户账分离 是怎么做的，电商会员和支付账户的分离？    
A：根据对支付系统的设计，是通过映射的方式进行分类 电商会员属于业务，而支付账户在支付账户里面，根据需求来定。   
   
Q：一个或多个用户 对应一个支付会员，有例子吗 ？   
A：有些公司是通过自然人来做的。   
   
Q：比如风控系统识别出近期行为接近危险的会员，预先在登录时就要求验证 ，有这种流程没？    
A：是有的   
   
Q：会员中的会员，和支付会员的具体区别场景，能不能再列举下？   
A：会员中的会员是业务，可能分了很多类，很多号，但是支付时，对应的号可能会不同，因为支付代表的是资金，二会员是业务。   
   
Q：会员的黑白灰名单机制是在支付会员系统中么    
A：这个在风控和会员体系中都有   
   
Q：如果冻结了会员，还会影响正常业务不？交易的资金会走到其他户里还是怎么处理，可以讲下这些么？    
A：冻结也分级别,最高的级别是不允许做任何资金操作的,比如监管下发冻结指令，那么用户的所有资金操作都不被允许。   
   
Q：会员中会员和支付会员，两套单独维护？    
A：淘宝账户和支付宝账户应该不是一个吧。   
   
Q：大家怎么看待指纹，不说手机上验的有多可靠，只说对服务端来说指纹就等同于免密，怎么宣传上都把指纹看作是个无比安全的东西。   
A：指纹确实比较安全，但是由于是手机黑盒，所以对于我们来讲，我们没有办法防止苹果伪造指纹。手机root了也可以修改指纹，毕竟返回的只是true和false。   
   
Q：一个或多个用户对应一个支付会员中多个用户怎么理解的   
A：有些公司的策略不同 有些是按照自然人来看的 有些是业务线不同账户 但是支付时是一个的。   
   
Q：那么那种在途交易的资金那样你们会怎么处理？是会原路返回么？还是会在中间户？ 回答：我一般放在中间户   
   
   
## 三、自由讨论   
   
PM1：	账户会有账户类型   
P2：	比如风控系统识别出近期行为接近危险的会员 预先在登录时就要求验证 有这种流程没   
P3：	首先感谢分享，会员中的会员，和支付会员的具体区别场景，能不能再列举下   
P4：	自然人在不同商户下的支付动作   
P4：	应该在第三方支付中对应不同的会员吧   
P5：	会员的黑白灰名单机制是在支付会员系统中么   
P6：	我的理解，会员就是客户，一个客户有多个登录账户也就是用户，一个用户又有多个记账账户   
P5：	还是常规的会员系统里面   
PM1：	@龚正 就是你们遇到风控监控异常的时候，会对交易进行冻结，还是会对会员整体的进行异常处理。如果冻结了会员，还会影响正常业务不？交易的资金会走到其他户里还是怎么处理，可以讲下这些么？   
P7：	@P6 我的理解，会员就是客户，一个客户有多个登录账户也就是用户，一个用户又有多个记账账户   
P7：	我们也是这样理解的   
P3：	会员中会员和支付会员，两套单独维护？   
P7：	客户、用户   
P8：	类似司法冻结了 那   
P9：	[玫瑰]   
P10：	大家怎么看待指纹，不说手机上验的有多可靠，只说对服务端来说指纹就等同于免密，怎么宣传上都把指纹看作是个无比安全的东西   
P11：	一个或多个用户对应一个支付会员中多个用户怎么理解的   
   
P2：	会员对应到实名的人 只是个记录信息 实际操作和业务发生在登录帐号上   
PM1：	@龚正，那么那种在途交易的资金那样你们会怎么处理？是会原路返回么？还是会在中间户？   
P8：	问个支付会计的问题：到会计落分录，听大家说一般 是业务属性+支付账户属性 来确认落到什么科目，你们这层到科目是怎么做映射的？   
P10：	@龚正?，对啊返回的只是true、false。对于网络报文来说，只能依赖客户端不被破解，本质和无密也差不多   
P3：	淘宝账户和支付宝账户应该是打通或者一样的吧。如果单独维护，两套体系会产生一个议题，就是会不会涉及到信息同步的问题？或者说，有些信息，比如userId应该是一样的，还有实名认证信息，是共享的。   
P11	[强]感谢ark的分享和解答   
PM1：	[强]感谢ark的分享和解答   
P6：	支付宝和淘宝不是一个，只是绑定关系   
P12：	淘宝账户和支付宝账户 一个是业务的 一个是底层的   
P15：:	联合登录后在库中是怎么存的，这块能说说么   
P8：	@龚正 账户记账映射到科目 是怎么做的   
P10：	淘宝账户和支付宝账号不同，我猜是个悲伤的故事，不知道有没有阿里的人   
龚正：	联合登录后在库中是怎么存的，这块能说说么 联合登录是什么意思   
P6：	支付宝和淘宝是两个体系，只是账户打通   
P10：	谢谢分享   
   
   
龚正：	账户记账映射到科目 是怎么做的 在账户中存科目呗   
龚正：	[阴险]   
P16：	淘宝只管订单方面，支付宝只管支付方面的，这个不冲突吧   
P8：	哈哈   
P6：	联合登录是一种授权登录   
龚正：	淘宝账户代表的是电商相关的资产 支付宝账户代表自己资产   
龚正：	资金资产   
P8：	账户中直接存了科目？   
P12：	支付宝服务对象不只有淘宝 是面向全行业的商家 大家不要搞混淆了   
P8：	支付宝是自己的 客户-账户   
P17：	淘宝和支付宝做的应该是账户互通   
P6：	淘宝是阿里巴巴的，支付宝是浙江蚂蚁金服的   
龚正：	其实我感觉联合登陆和微信登陆 微博登陆等等差不多吧   
龚正：	多个对应一个   
P12：	支付会员的场景 只有会员支付吗？   
P3：	好的，学习了。   
P18：	OAuth2.0 认证授权 挺流行的吧   
P19：	oauth严格意义没认证 只是授权   
P19：	目前最好的解决方案了   
P10：	阿里、支付宝都是一家，淘宝可以用支付宝登录。我行用户体系被强制统一，理由之一就是阿里两套用户带来许多麻烦   
P6：	是一样的，用户在微信登录时再在别的系统登录，传密文到目标系统，目标系统找到映射用户号，查出相关信息，存入缓存   
P2：	会员是身份证号 帐号是手机号 业务都发生在帐号上 要封号应该从会员上封   
P20：	淘宝和支付宝账号也没打通吧？还是需要相互授权吧？   
P15：	联合登后和自有的用户是分开存的吧？   
P16：	OAUTH2.0就是单点登录登录的一种，不用区分是哪家企业的   
P21：	淘宝和支付宝账号是分开的 有一套映射规则 淘宝uid是底层基础库的标识   
P16：	你在网易云音乐照样可以用微信登录，只要去微信那边注册下就行了   
P6：	联合登录就是一张映射表   
P20：	OAUTH2.0接入时已经区分接入的是哪家企业了   
P8：	@P10 “我行用户体系被强制统一” 能否介绍下这个   
P19：	oauth联合登陆 只是授权登录信息 这算最基础的应用了   
P22：	淘宝和支付宝是绑定关系，且支持多对一的绑定   
P20：	oauth最终是获取accesstoken，授权只是第一个阶段   
   
   
P19：	银行都建有统一会员系统吧   
P6：	银行是cif   
P22：	各位是怎么处理金融和支付账户的   
龚正：	[动画表情]   
P18：	支付会员由于人行监管问题，等级上明显要高于电商会员，通常高等级向低等级上授权， 一个电商会员去了支付系统，没各种实名认证，啥也不能做。   
P2：	风控统计这些要考虑会员下所有帐号了 至于相同会员不同帐号共享登录这些根据不同公司喜好吧   
P22：	@龚正?比如信贷业务和支付账户的关系有什么建议吗   
P23：	这些会员和电商会员区别在哪里   
龚正：	信贷一般是自然人为基准吧   
P19：	会员系统 和支付系统 之间 登录统一授权就好了   
   
P6：	信贷支付两个业务，支付账户用来处理资金转移通道，如提现，还款   
P19：	建立会员系统 和授权中心 通用授权的注册一次性授予 其他的单独授权也可以   
P19：	有了这个 多少系统 都是一样的吧   
P22：	感觉这样容易出问题，我们现在好几款信贷产品，账户没打通，结果部分客户出现了多头负债@P6?@龚正?   
P22：	当然也有可能是单个自然人没有最高限额导致的[捂脸]   
P20：	肯定是借贷记账不平导致的??   
P24：	淘宝和支付宝是绑定的关系，可随时解绑和环绑，没有打通。   
P24：	![20170515_203416](http://static.cocolian.org/img/2017/20170515_203416.png)   
P6：	信贷是基于客户的，应先建客户系统，全业务系统共享客户系统   
P20：	是的，都是独立的   
P25：	信贷产品之间互相的关联关系也有问题   
P22：	谢谢几位，看来我想复杂了   
P26：	@龚正?请问现在指纹支付这块，指纹数据都是存在本地，服务端只能授信于硬件，除了授信之外，有没有其他办法保证指纹数据正确？谢谢   
P6：	信贷产品挂在客户身上   
龚正：	指纹关键设备   
龚正：	并判断手机是否root   
P24：	金融和支付账户打通会有很多麻烦，监管对支付账户的各种要求会导致金融产品也得被迫「合规」改造，建议采用绑定方式。   
龚正：	目前也只能这样了   
P22：	@P6?目前是这么做的   
P26：	谢谢   
P2：	风控应该控制会员而不是帐号 一个会员小有多个帐号   
P18：	会员就是一套系统的用户体系，电商系统、支付系统、P2P系统一般都独立会员体系，登录账户可以共享，业务上差别很大的，拆开来比较合适，这样就不会人行支付监管需求，要影响P2P系统，完全共用的话，就相互影响咯。   
P6：	那就是授信问题了   
   
P27：	开始说到在账户中存科目，存的是一级科目吧，后面做总分对象平衡用到，这么理解不知道对不对？   
龚正：	存的是末级科目   
P6：	我们以前的会员体系是分业务的，用户分主副用户，副用户可以用主用户密码登录，用付用户做业务   
P10：	判断手机是否 root不够，因为请求可能根本没来自合法的客户端，当然这又是另外一个很大的话题   
P28：	设备指纹   
P24：	指纹支付对风控要求比较高，服务器端要验证 设备指纹，IP等客户信息，防伪造，同时要保证网络传输的安全性，防篡改。   
P28：	对的   
P12：	[强]   
P18：	一个账户的正常资金和冻结资金 你们一般怎么设计的？ 一条记录， 还是分开？   
P28：	一个用户有多个账户   
P2：	一会员多帐号这样会大大增加系统的复杂度 实名认证后应该合并成一个帐号 其实最终也是方便用户   
P28：	一个用户对应多个账户   
P28：	每个账户操作 都会对应相应的分录   
P2：	可以保留登录用户名 登录后操作都在应该帐号上   
P6：	账户的冻结解冻是有登记簿来管理的   
P6：	一会员多账户，账户实名时只实名当前账户，别的账户需要归并或签权合并，才能合到同一会员下   
P29：	支付系统中叫会员合适还是叫客户合适？   
P30：	会员   
P2：	允许多帐号实际上是破坏了关系数据库的范式约定 呵呵 不实名应该不允许产生业务数据 没实名前的帐号系统应该预留会员关联位置   
P29：	会员比客户含义貌似宽泛很多   
P6：	支付宝的会员含个人客户和商户，央行的客户指个人或买方   
P6：	不实名也应该能做业务   
P2：	如果帐号下已经跑了业务 那么关联数据会分散在各个地方 合并时风险就大了   
P6：	业务是跟着账户的，没问题   
P31：	你们所谓的一会员多账户是什么意思，能不能举个例子   
P29：	余额 余额宝   
P6：	一客户多用户，一个人有多个支付宝   
P2：	我说的是理想状态 实名现在有快捷途径操作很容易了 用户有能接受 这样减轻系统复杂度   
P11：	那怎么判断多个支付宝对应一个人   
P6：	理想是这样的，流程往往是业务说了算啊   
P29：	可以用一份实名认证吧   
P29：	支付宝是这样的   
P31：	一个人有多个支付宝？跟一账户多用户有什么关系，在银行卡没改制之前我一个银行也有多张银行卡，关键是系统也不见得把我分成一个人呀，都是一对一的关系   
P11：	即使实名的话，在数据库中认定也是不能体现的   
P11：	要根据唯一标识查询才能得到这个结果了   
P6：	银行肯定是一对多的   
P2：	风控就有漏洞了 前面敦煌那个人也是   
P6：	银行要cif就是干这个的   
P31：	问题是这玩意你们认为的那种一对多有什么好处？   
P31：	就好像我在这张银行卡猛消费，跟我另外一张银行卡有什么关系   
P31：	在银行卡没改革之前   
P6：	是和你本人有关   
P6：	客户是现实自然人在系统中的建模   
P31：	有什么关系，这个资金也不互通，积分也是，活动也是，想不出有什么关系   
P6：	信用   
P6：	授信，风控都会参考这些   
P6：	还有就是客户行为分析   
P31：	那如果你们搞这种一账户多用户的，系统里面单账户余额就是所有用户总额咯   
P31：	错了，是一会员多账户，会员余额就是多账户总额？   
P2：	业务可以存在多个帐号 但第一级关联必须是会员 之后二级关联到帐号 也没问题 说的是理想状态 不需要合并 但必须明确主体关联   
P6：	当然还有更多，可以这么说:相同姓名+身份证号视为同一个人，不论在哪个系统里，都是现实中的你，你在中行上了黑名单，招行也不会给你做业务   
P29：	余额好像一般是分开的，额度是一起共享的   
P6：	余额是另一个概念，资金账户   
P6：	额度是会员的资金账户，余额是用户的资金账户   
P32：	想请教下支付会员下会有哪些账户分类，分类的标准一般会有啥   
P31：	这个额度跟余额有什么关系没有   
P31：	还有这个额度代表什么，最高限额？   
P6：	我们先把概念统一了。 额度就是授信，类似于信用卡额度   
P29：	会员是身份证号，用户是身份证+手机号？   
P32：	在支付系统应该是限额，在消金领域即有限额又有授信   
P31：	哥们你一口气说完吧，我就看你的了，这些名词说实话每个人都不一样，我就看看你怎么说，按你标准理解   
P32：	估计不会这样，因为现在手机号就只能实名认证一张身份证   
P6：	用户一般用手机号区分   
P29：	@P6?我的理解对吗   
P32：	用组合标志去标识一个用户，拓展可能受限制   
P6：	等一下，我整理一下   
P2：	有业务就有风控要求 而风控对应会员 所以有业务前需要做实名认证   
P6：	我们的个人会员系统分三层:客户，用户，账户，客户就是一个自然人建模，用户常指一个注册用户，即系统使用者，也叫登录账户，账户，指存放资金的实体，用货币来计量   
P6：	客户通常通过其用户来使用系统，比如一个手机号注册的用户   
P29：	那会员这个概念呢？等同于客户吗   
P6：	对， 一个人有多个手机号，也就导致了同一个人在一个平台有多个用户   
P6：	一般是先有用户再有客户，用户通过实名认证产生客户，一个客户在系统中只有一个唯一标识:客户号   
P29：	明白了   
P6：	两个用户实名，如果证件号和姓名相同，我们认为是同一个客户下的两个用户在做实名   
P6：	第一个用户没问题，一对一产生了客户，当第二个用户实名时，由于客户已经存在，不能再创建了，或者说即使创建了也要合成一个，我们称为归并   
P29：	支付密码是在用户纬度是吗   
P2：	反正业务数据产生前必须找到客户 否则第一笔业务都可能产生风险 多个帐号没问题 加个登录用户也没关系 主要是业务安全上考虑   
P6：	可以在用户上。 归并一般是这样做的:当第二个用户实名时，系统检测到客户已经创建，会让第二个用户输入已实名用户的支付密码来进行签权归并   
P6：	支付宝以前是只有当你提现时才让你找客户，毕竟用户体验也要考虑   
P29：	现在用户发起交易的前提必须实名吗？   
P6：	我接着说归并，当第二个用户密码通过后，会把第二个也挂在此客户下，即:将客户号填入当前用户域中   
P6：	实不实名要看业务，也要看监管   
P2：	说影响体验看个人理解吧 除非跑的是无关紧要的数据 要不也是对客户不负责任[呲牙]   
P6：	基本上就这些吧，比较简单的。 从管控角度上说 客户冻结了，其下所有用户禁入，用户冻结了，用户下所有账户禁入   
P6：	一个原则:宽进严出   
P29：	[强]感谢   
P6：	你们聊吧，我看会黄金现货   
P2：	客户用户帐号之间就是两种关系表 业务表上存帐号id 统计就麻烦了   
P6：	业务表上同时存两个id   
P2：	客户的吗 用户没意义的 就是登录用   
P6：	都存，用户当然有意义了，你的操作是基于用户的   
P2：	再说吧 从关系表可以查到用户 用户可以看做是客户一个属性 无意义 有空聊吧 呵呵   
P6：	你考虑一下一个客户多用户时场景吧   
P6：	而且账户是在用户下的……   
P9：	其实最简单的我就是现在银行的系统下归集所有的银行卡的信用卡   
P31：	你那句会让已实名用户输入支付密码来进行归并是什么意思   
P31：	同一会员不同用户必须支付密码一样？还是说什么   
P6：	归并是要有验证的，否则我知道了你的证件，把自己用户挂你名下，如果你名下有信贷，钱就容易被我拿走。   
P6：	同一会员不同用户密码应该不一样   
P2：	知道 用户除了登录用处不大 业务已经关联帐号id了 这时的用户只是客户的暂时代表 在没实名前 实名后从关系可以找到客户那才是有用 业务要么多存客户id 要么不存就只有帐号id也可以 个人理解 数据存了终究要怎么用 风控时定位都用户还不够 要找到客户才行 不说了   
   
   
P8：	群里有没有做过资产证券化的？   
P6：	p2p么？   
P8：	信贷 ABS业务   
P33：	我·行·正在做ABS   
P8：	@P33    
P31：	Abs最好套个资管计划，不然资金池很稳定   
   
   
P31：	用户密码不一样但是支付密码一样？   
P6：	不一样，只有你知道另一个用户的密码的时候，才能确认另一个用户也是你   
P34：	在途资金、冻结资金、可用资金，需要通过多账户方法来实现吗？   
P2：	用户是虚拟的 客户帐号业务才是真正实体   
P31：	你这个流程我大概了解了，那我能不能说你这玩意其实是根据参照物来看的   
P31：	比如在中国人民银行看来的用户在商业银行看来可能是会员   
P20：	@P34?不需要多账户，账户中有账户余额，可用金额和冻结金额，账户余额=可用金额+冻结金额，一般只有出账账户需要冻结金额，冻结额度会存在一个冻结单，记录冻结的哪笔交易，哪个账户，冻结金额，冻结状态等，同时更新账户可用金额和冻结金额，交易成功做解冻出账，否则做解冻处理，恢复可用金额   
P34：	如果一笔交易，T日更新余额（在途状态），T+1转可用，如何在账户层面实现在途转可用的过程呢？   
P19：	余额 是 好几个值： 可用余额、 未确认余额、 冻结余额。当前 余额 是 这几个的总和。   
P20：	我认为在途金额处理方式跟冻结金额是一样的，在途金额转可用首先是这笔交易的最终状态肯定是确定的，要么成功要么失败   
P34：	如果通过支付账户挂子账户的方式实现？是不是很啰嗦？区分在途资金账户、冻结资金账户、可用资金账户。可用余额=可用资金账户。不可用余额=在途资金账户+冻结资金账户；总余额=可用+不可用   
P19：	有很多处理方法   
P6：	在途资金不应该和余额统一处理   
P34：	在请教问题：管理办法支付公司不允许为证券、信托等开户。   
P19：	有些交易是依赖冻结的 有些依赖中间账户   
P34：	那可否有业务往来？资金如何处理？   
P6：	余额是指已到账不可撤消的资金   
P34：	这个是呀   
P31：	民生哥们，我刚刚的比喻对不对   
P6：	差不多吧   
P31：	支付公司是尽量别跟那些玩意打交道，不然死的快，特别是证券[捂脸][捂脸][捂脸][捂脸]   
P20：	@P34?在途资金我刚才说法有误，请@P6?帮忙解答下[抱拳]   
P6：	余额和在途不是一个维度   
P6：	我想知道业务场景   
P6：	如果一笔交易，T日更新余额（在途状态），T+1转可用，如何在账户层面实现在途转可用的过程呢？   
P34：	代扣一笔，支付确认实时。   
P6：	是这个吧   
P34：	t+1，资金到备付金账户，转可用   
P34：	如何在账户层，实现资金在途到可用的变化捏？   
P34：	嗯那   
P18：	在途一般在中间户体现   
P35：	一个账户内设两个子账户，一个现金，一个在途   
P34：	看来每个公司账户设置都不一样啦[偷笑][偷笑]   
P34：	通用方案，或者说“准标准”方案，是啥咧？   
P36：	你定的在我眼里就是标准的   
P18：	供参考，一笔收单涉及2个结算，银行T+1结算： 渠道待清算账户（在途） -》 银存账户（备付金余额）； 商户T+1结算：结算中间户（在途）-》 商户结算账户（余额）；   
P34：	[呲牙][呲牙][呲牙][呲牙][偷笑][偷笑][偷笑]   
P6：	关键是有没有特殊处理   
P6：	你说的场景还是不是很清楚   
P20：	商户结算账户是不是就是在途资金账户？只有t+1结算账户金额被转到余额账户才能操作   
P36：	本质在于 我们给商户结算 是否应该依赖于通道方给我们结算   
P6：	不应该   
P36：	如果通道方没给我们结算 但是到了我们给商户结算的时间点 我们不想自己垫资给商户……   
P6：	这是两笔账   
P36：	这就是她的需求   
P36：	嗯 我也认为两者应该分开   
P6：	合同呢？   
P18：	信息流和资金流本来就是分开的。。   
P6：	如果通道不给你们结，你们永远不给商户结？   
P36：	现状是 通道方t+1结算给我们 我们跟商户的合同也是t+1 然后我们计算商户手续费 还要依赖于通道的对账文件   
P36：	嗯 如果通道没结 就先去追钱……因为额度太大 垫不起   
P6：	流程有问题   
P18：	垫资是因为这2个之前差异造成的。比如商户T0 银行T1   
P36：	嗯 应该完全隔离 通道和商户对吧   
P6：	对账流程有问题   
P36：	或者把商户结算周期拉长 或者自己垫资 就不会这么痛苦了   
P34：	如果有好的渠道可实时识别类别，可提前扣，不依赖于对账文件   
龚正：	一般都是商户周期很长啊   
P6：	对，对商户你们要自主对账，对于通道，以通道为主   
P34：	俺们特殊[呲牙]   
龚正：	厉害   
P36：	业务场景决定我们不能留钱……   
P38：	个人认为这个的记账完全根据业务来，在电商业务的余额体系里面，用户充值，支付渠道返回成功交易结果后，就该给用户显示余额。普通电商此时都不会有在途资金账户。高级一点能有这个账户。   
P36：	说白了 就是业主着急要钱！   
龚正：	着急要那为啥过你们。。[憨笑]   
P6：	分开处理就对了   
龚正：	还走第三方   
P6：	流水好看啊   
P34：	嗯嗯。   
龚正：	你们是房产交易吗   
龚正：	这种交易如果过第三方 时间是个问题啊   
P36：	是先过户 还是先给钱 ～我们就解决这个问题客户先拿出钱给我们就过户 过户后就给钱到业主   
P37：	房地产交易的支付宝   
P6：	分开处理，日终清算时，你们同时算好通道手续费及应收备付金，商户手续费及结算资金，对于双方都是对账打款，差错后期处理   
龚正：	厉害   
P36：	嗯 以后肯定要规范到这种正规流程   
龚正：	@小北-理房通-资金?你们自己是第三方呗   
P34：	嗯   
P6：	给通道方送个礼，上午给你们打款，你们下午打给业主   
P34：	[呲牙]   
P36：	[动画表情]   
龚正：	[动画表情]   
龚正：	房产的特点是客单量小 客单价大   
龚正：	普通电商的套路确实有点搞不定啊   
P36：	系统压力比你们小多了 我们可以慢点 ～不出资损就好   
龚正：	哈哈 要不你们就快一天 多收点手续费啥的   
龚正：	有垫资风险 就多点风险收益   
龚正：	[动画表情]   
P36：	木钱～   
P38：	T+0流水贷，提前结算   
P8：	账户中有账户余额，可用金额和冻结金额，账户余额=可用金额+冻结金额，一般只有出账账户需要冻结金额，冻结额度会存在一个冻结单，记录冻结的哪笔交易，哪个账户，冻结金额，冻结状态等，同时更新账户可用金额和冻结金额，交易成功做解冻出账，否则做解冻处理，恢复可用金额   
P6：	如果是这种情况，就用在途资金账户，因为一旦计入余额，就会纳入资产类，没人备付金，你纳入资产就有问题了   
龚正：	流水贷是啥意思啊   
龚正：	[惊恐]   
P34：	“银行系流水贷”？？？   
P8：	看到这个回答，记得还有一套类似模型。可用余额、预冻结金额、未达金额 、系统中金额   
P38：	@龚正?基于交易流水的贷款，也算是应收帐款贷款，同时基于企业资质。通常由收单支付公司或者合作资产方提供。   
P36：	学习了   
龚正：	奥 这样啊   
P32：	供应链金融？   
龚正：	厉害啦   
P8：	系统中金额用来处理A转给B 同时B转账给C   
龚正：	才看到你是ping++的   
龚正：	[色]   
P6：	应收账款的扺压贷款   
P38：	和供应链金融性质形似；流水贷是支付公司尝试的增值业务。   
P31：	你玩这种风险太大，个人建议小心为好   
P31：	你这种不是供应链金融，是信用贷款   
P6：	都有   
P31：	供应链金融必须有明确的标的，要么是应收账款类型，要么是预付款，要么存货，他这种流水贷其实跟阿里的借呗没啥区别   
P6：	不是有扺押么？纯信用？   
P38：	资方和第三方支付公司合作，或者第三方支付公司自己做，风险是很小的。原本通过第三方支付公司收单的资金T+1结算给商户，商户在第三方支付公司这开通流水贷，T+0就拿到对应的结算资金；对第三方支付公司而言，就是基于成功交易的交易流水提前一天向商户结算资金。   
P31：	不懂，我就往前反了一下，没看全   
龚正：	这种贷款一般问题不大   
P34：	您说的是特约商户t0业务   
P6：	基于结算资金抵押   
龚正：	回笼资金挺快 不过小公司作假就悲剧了   
龚正：	还是看信用   
P25：	这个也叫贷款？   
P31：	哦，这个叫流水贷[捂脸][捂脸][捂脸]，这个不就是D0业务吗   
P6：	我们叫D0   
P25：	一脸懵逼[尴尬]   
P31：	你看看又是名词定义不一样的结果   
P31：	[捂脸][捂脸][捂脸][捂脸][捂脸]   
P34：	[呲牙][呲牙][呲牙]   
P34：	哈哈哈哈哈   
P28：	这对于第三方来说 就是贷了结算款 t+1第三方不给商户结算 是这意思么   
P6：	垫资D0结算   
P38：	[Facepalm][Facepalm]   
P25：	对商户来说提前结算是好事   
P18：	全支付公司自己垫资是D0，区别引入了其它资产提供方？   
P25：	但不会是便宜事吧   
龚正：	提前结算还是有风险的   
P38：	收费标准不一   
P25：	利息是多少   
P6：	手续费就高   
P25：	拿个标准来思考下   
龚正：	所以实力雄厚才垫资 要不就找放贷方 放贷同时又买了保险   
P6：	我知道的有10%手续费   
P25：	这种业务场景也是真实存在的   
P28：	这没啥风险吧   
龚正：	也有   
P18：	银行一般万五？   
龚正：	风险肯定还是有的   
P6：	有，上游不给结就是风险   
P28：	该结多少就贷多少还是每天给商户贷的都一样？   
P28：	上游不就是银行吗   
P18：	POS T0结算很多都这么干吧，商户自己出手续费   
P25：	这种对应到线下有没得类似的实际业务   
P6：	银行卡套现业务   
P25：	感谢，不过银行卡套现和这个还不是很贴合   
P6：	睡了，大家继续   
P18：	套现都是急着想拿到钱的…   
P36：	[月亮][月亮]   
P25：	不是很清楚商户付相对较高的手续费来要求T+0清算的需求根源   
P25：	[月亮][月亮]   
P8：	@P6?你们说的这种提前收款和保理模式的提前收款是一类么？   
P31：	不可能百分之十的哥们，最多百一百二顶天了，百十的那是洗钱   
P18：	商户T0实时代发，通过线上充值一般是要垫资的，可以商户直接银行转账，系统实现自动登账，都能省点。   

## 四、其他讨论

00:43:52	请问各位行家，有visa master的预付卡吗   
00:45:07	国内哪家银行或者支付公司可以办   
08:47:35	自动对账功能有人用过分布式核对的么？   
08:48:20	。。   
08:49:39	自动对账 分布式核对？   
08:50:34	两本帐？   
08:51:37	嗯，我们几百个账户，有的一份账单200万的交易数据。单机跑，半小时跑不完   
08:52:30	自动对账可以分渠道分商户，分布式对账不也是把单机的数据分类跑吗   
08:52:34	嗯，商户交易明细和支付公司两边核对   
08:53:01	是的这样。@XXX支付?   
08:53:40	目前也是测试阶段，不知道会不会有其他的坑   
08:54:31	有没有考虑到，使用map reduce来解决？   
08:55:43	对账坑都是在数据整理、处理阶段，都是小坑慢慢填[呲牙]   
08:58:12	有的，核对过程有更新操作，但是我们账务基础数据大，我们的dba评估更新效率不高，估计半小时出不来   
09:00:05	对账就是在支付系统中读写操作最大，分库分表加缓存   
09:00:32	@XXXPM?[偷笑]   
09:01:41	数据据量大了，一般都用HDFS去对   
09:02:36	比如Hadoop   
09:03:01	可以可以[呲牙]   
09:03:09	[捂脸]，可以分库分表。我们拆分开来会有几十张表dba加个字段都加的累死@XXX支付?   
09:03:17	@XXX北京 很早很早之前我也在联想做过硬件驱动开发。   
09:05:12	哈哈，那你要多动脑筋了！看来你可以用分布式框架对了   
09:06:05	很早很早以前啊，前辈啊   
09:10:00	[20170511专题：预付卡](http://mp.weixin.qq.com/s?__biz=MzI4OTQ3MTI2NA==&mid=2247483761&idx=1&sn=a4386673a09448ad151a3670dfa93e10&chksm=ec2fef3edb586628bb42167b593a38315bd28c93c836e23ca434121fac1e4689b6c9fdab6ca0&mpshare=1&scene=1&srcid=0515fhi0gU31BeX225GtAC96#rd)   
09:17:59	不客气，具体问题还得具体分析，对账可以单独拉个课题了，多商户多渠道大数据读写比对，数据参数抓取处理.....可以一起讨论   
09:19:09	问一个具体技术问题。准备接各个地市的银行的支付渠道，想搞一套可扩展的方案。现在有两个想法：一个是用pf4j插件化的开发模式，还有一个就是类似微服务，一个渠道一个服务。大家有什么建议呢   
09:19:30	这个群我感觉可以挖人了[呲牙]   
09:20:04	别啊，纯技术讨论群   
09:20:08	还有对账这块的处理的流程   
09:20:18	这块都可以 好好沟通梳理下哇   
09:21:21	@XXX合肥   
09:21:31	OSGI这种插件形式会不会很合适   
09:21:41	[愉快]   
09:22:08	是啊，滴滴，共享单车，这些都是客户使用一次上一次保险，一天保险公司和滴滴或者共享单车对账数据非常非常大，在整个对账流程、数据处理上都需要深度的思考   
09:23:20	有人研究过资产的登记系统吗 由于涉及到 二次转让 是否要复式记账 单边帐能搞定吗   
09:23:55	@XXX北京 刚@错了，其实也不需要那么动态，只是现在人力不足，需要各个业务方兄弟配合一起接   
09:24:52	不知道哪种模式好点，插件化的话最终还是部署再一起，外部服务感觉增加了调用链，一致性也不好保证   
09:25:19	@XXX北京 我们的是复式的记账   
09:25:32	但是贷方基本上只有发行人。   
09:26:18	你们是金正 和 恒生的系统吧 设计方案我好像有 我研究下   
09:26:33	我们不用他们的   
09:26:36	自己开发的系统   
09:27:01	求分享金证和恒生的系统啊   
09:27:15	我找找呀   
09:28:45	对账是个事   
09:35:19	对于系统建设来说，建议走微服务，不走插件化，从设计角度上看，服务与是业务对齐的，更合理   
09:39:29	预付费卡和贷记卡的区别很容易区分，贷记卡是可以透支的，而预付费卡是不能的，必须先充值后消费。 预付费卡和借记卡的区别主要包括预付费卡不记息，也不能提现   
09:39:42	这个不能提现是绝对的说法吗？   
09:40:15	@XXX北京 微服务就涉及到分布式事物的问题~   
09:41:07	@sinory?是的，不能提现，最多原路退回   
09:41:27	预付费卡 还有能在ATM取款的   
09:41:58	@blue?那是违规   
09:42:05	比如中银通和银联发的   
09:42:29	那是另外一个逻辑   
09:42:40	微服务先考虑业务划分，再考虑数据分布，分布式事务是根据数据分布来的，当然，这个问题可以参考一些分布式事务的解决方案，比如2PC或柔性事务，   
09:42:41	走的联名卡   
09:42:46	一般机构是不能提现   
09:42:51	有发卡资质也不行？   
09:43:24	不能   
09:43:57	法规只有原路退款吧，没有提现一说，看产品怎么包装了   
09:45:32	没有「提现」这个说法，但是可以「退款」，当然也可以全额退款。实际上，可以包装成提现   
09:45:41	如果允许提现，那么预付卡就是洗钱了   
09:46:04	因为预付卡是不记名可以转赠的   
09:46:17	这样就有点倒卡了   
09:46:20	退款也是严格的原路退回 ？   
09:46:45	怎么包装成提现？   
09:47:04	可以退回账户余额吗？   
09:48:06	分布式事务，很多时候保证最终一致性就好吧，这个应该是次要考虑的，合理的补偿机制可以弥补很多   
09:49:22	微服务本质和分布式事务就是矛盾的。   
09:49:27	是的，只要保证最终一致性，并且关键接口一定要做幂等   
09:49:28	以前的第三方支付牌照中，只有预付卡牌照是可以合法进行资金沉淀的，但网络支付牌照进行支付账户分级后，这一点优势也荡然无存   
09:50:29	@XXXX 所以现在一些电商在持有网络支付牌照后，为了让资金尽量留在体系内运转，内部消化，退款到余额很常见   
09:50:59	退回余额以后是不是可以提现？   
09:51:13	这种提现算是洗钱吗？   
09:51:39	这个余额是指的是C端充值人的余额还是B端发卡人的余额   
09:51:41	@XXX北京 嗯~ 事务执行计划、补偿计划及各种状态检查和重试。   
09:51:46	你可以试试[呲牙]同卡进出并不被严格执行   
09:52:21	@XXX产品总监 ,是的   
09:53:29	为了减少分布式事务，在微服务设计上是有技巧的，要合理划分，同时，在数据分布上也有一定的技巧   
09:53:30	另外，有一点要纠正下，预付卡有记名和不记名两种类型，并不都是不记名卡   
09:54:36	微服务分布式事务 也比较麻烦   
10:02:09	支付事务的一致性是个问题   
10:06:49	这个东西就是麻烦一些 其实方案很成熟   
10:07:06	无非就是 tcc 和 最终一致   
10:09:39	服务治理比分布式事务更重要   
10:10:43	@XXX杭州?热点账户不一定是会计那边。比如商户账户的余额更新   
10:16:07	业务系统记流水，但不会每笔都更新商户账户余额，会计系统每天日结后再更新商户余额   
10:16:46	实时入账、异步入账、批量入账   
10:17:19	如果余额不实时更新的话，那么怎么解决1块钱买两款钱东西的问题呢   
10:17:24	@XXX杭州   
10:17:42	@XXX北京?恩，但应用层面也要做不少事   
10:18:12	新网的哥们，你说的支持账户分级是什么意思   
10:19:42	出账方是实时记余额的，但是收款方一笔都是商户账户，实时记录会存在锁账户问题，商户一笔存在两张账户，结算账户和提现账户，结算账户的钱商户是不能操作的，只能在日结后系统自动转账到提现账户，然后商户才能提现。   
10:21:27	@XXX杭州?工资发放是典型的一借多贷业务，如果走逐笔，借方账户就是典型热点。不过现在发工资都不走实时了。   
10:21:42	@XXX杭州?实时记录会存在锁账户问题，所以得锁分离啊   
10:23:04	我们现在对于商户账户 做了锁分离 热点粒度降的最小 生产环境运行良好 稳定   
10:23:34	你刚刚说的会计这边 其实我的理解是内部户余额更新   
10:25:03	@XXX研发 锁分离我们还没有使用，我们目前还是基于mysql行级锁做的处理，如果能够解决锁账户的问题，实时更新余额也是可以的[微笑]   
10:29:25	@XXX珠海 工资发放的业务没接触过，如果是逐笔处理的话，也不会产生热点问题。[微笑]   
10:30:45	@XXX研发 锁分离的技术方案可否简单分享下？[呲牙]   
10:36:04	@XXX杭州?逐笔是串行，锁等待时间太长   
10:37:40	锁分离 我抛一个砖 1：考虑业务场景 是否可以每笔业务分子账户 避免冲突。 如果一定要实时记账存在并发 首先事务处理内容要足够的小 仅记录流水和修改余额 其他异步 2：账户操作前redis并发锁控制操作权限获取，设置超时及尝试间隔 3：账户实体本身增加乐观锁 捕获锁异常自动重试 4：使用akka框架 actor模式 （测试阶段）   
10:39:12	软件除了技术架构外 更底层的应该有个数据架构 以前的软件处理的只是一个商店或一个单位的数据 看不出什么 现在要面对的是全民的数据 现在的很多问题如事务处理应该从数据层面去找解决方案 跳出软件框框回看现实世界里并行发生的各种事件 这些人物事件之间其实相互关联很少 干嘛都把他们塞在一起呢是吧   
10:39:48	领域驱动？   
10:44:11	不相关的数据塞在一起 造成每次处理时都要先排除千千万万与其无关的数据 定位-加锁-修改 坏的情况还会触发整体联动 好像是很高深的样子呵呵   
10:47:36	我认为恰恰相反，随着科技发展，事物之间的联系会越来越密切，不论是直接还是间接，数据处理始终是个问题，只不过是如何减少复杂度的问题   
10:47:46	结构的复杂造成了处理逻辑的复杂   
10:48:26	哈哈，说到底还是认知的局限性   
10:55:12	@XXX北京 多谢分享~   
10:56:56	客气～   
11:15:00	@XXX北京?我要说关系数据库是个坑 大数据是巨头的预谋你估计要跳脚 权当娱乐吧   
11:20:22	搞什么？这分享的是啥玩意？   
11:28:09	跑题了 抱歉[握手]   
11:30:45	出款第一步减余额必须实时更新余额吧，通常是复试记账，另一方可以非实时，中间账户加减都可非实时；账户更新余额可以行锁（注意等待时间），cas快速失败。   
   
12:37:39	@XXX北京?请教一下你们加共享锁时落实到操作上就是设置隔离级别吧 不知道你们怎么实现的 自己写还是用什么框架   
12:47:12	锁实现是依靠redis键值的有效期 加while循环自动间隔重试 比较常见的redis分布式锁实现了，数据库层级就是乐观锁简单说就是靠版本号管理 然后你说的隔离级别是指事务隔离级别？   
12:47:25	羡慕北京童鞋，我也想参加[可怜]   
12:50:34	@XXX合肥?这个我这边是类似你说的第二种方案，我们是一个通道一个服务。通过服务注册，目录查询发现服务。上线后通过控制中心配置通道上下线   
12:54:04	@XXX北京?是的 你说的版本号和   
12:55:28	zk有分布式锁   
12:56:34	我们用的oracle 默认隔离级别Read Committed   
12:57:10	。。。在外面redis的功能差不多吧 感觉最终起作用的还是隔离级别 对单键值和范围的还有多种可能 感觉最终还是要依靠数据库本身的控制才可靠   
12:58:03	mysql的好像是rr   
12:58:15	不是啊 分布式锁是在操作前获得权限   
12:58:36	如果单靠数据库 是所有逻辑操作执行完成   
12:58:55	提交时控制 本身也是在做无用计算了   
12:59:50	知道 在共享内存读写个标记 当前是我的才发起事务   
13:00:06	嗯   
13:01:40	这个和记录里的版本号类似我觉得 不同隔离级别读出来的是有偏差的   
13:03:00	当然redis可以减轻数据库的一些压力 但还是不能完全依赖   
13:04:19	这个取决于你如何定义redis的键值了 这个键值是否有必要有版本的概念 嗯大家实现方式各不同吧   
13:04:50	市面上号称实现xa的方案可靠性不知怎样 性能呢   
13:07:07	是的 redis可以提升性能 设计好的话数据库那里可以用轻量级别 只是最理想化的   
13:09:31	嗯 静待群里更多解决方案 并发是挺麻烦   
13:15:21	算是业界难题吧 期待这方面有更多分享[微笑]   
13:19:22	@blue?zk在这里和redis角色差不多 感觉zk还重了些   
13:21:21	是的 角色差不多   
13:56:42	@XXX北京?前面你说的while循环尝试申请redis锁这里 会不会有性能问题 因为等的时候会占用一个线程 虽然一般都不会出现等多次的情况 我想有无可能转成异步让redis或者谁来通知 再触发继续 只是个想法啊   
14:01:17	这里不适合用通知的方式   
14:02:06	因为业务耦合的很紧密，通知又需要时间，因此一来会造成系统复杂度提高，二来反而增加了操作时间。   
14:02:35	[java异步无锁共享内存 可实现进程间通信](https://github.com/peptos/traffic-shm)   
14:05:20	或许折中方案 有个东西专门和redis打交道 负责全部锁申请事务 并负责唤醒下游的异步事件 可以节省线程消耗   
14:05:34	嗯 其实所有的并发最终本质解决方案 都是串行 我一直想把akka的actor模式用起来 但是 还在摸索 不确认是不是账户相关操作的一种解决方案 只是个建议   
14:07:45	你说的专门有个东西和redis打交道，是有的，但是其实就是自己写个服务方，封闭所有对redis和数据库层面的操作，对外暴露简单的接口   
14:08:17	我记得有个专门的名词，但是忘了。。。   
14:08:49	akka和直接用netty差不多吧 用原生的好我觉得 在没有作用到数据本身时可以不用要求串行 也是个人理解   
14:10:57	另外scala是吗有人批它 用回java好 都是一家之言   
14:13:20	@mark?自己写也可以吧 就是探讨流程上优化的可能   
14:21:40	@XXX?底层的东西复杂多变 文档里写的都不一定对 研究罢了   
14:22:52	对的，主要是在流程上和线程模型上要掌握好   
14:36:12	或者第一次尝试失败就转异步 在平时第一次成功的占多数情况 如果失败说明可能碰到秒拍这类场景了 不管是等还是超时失效都不好 异步这时候才是最好的   
14:46:50	应用场景不同要求的处理逻辑不同 虽然都是一个入口 但面对的条件可能千差万别   
15:39:59	@XXX?http://www.yinwang.org/blog-cn/2016/01/18/java   
15:52:15	王垠的文章吧？   
15:55:25	是的   
15:56:48	我只知道淘宝从php换成了java   
15:56:58	但是我同学说 php是世界上最好的...   
15:59:03	独立思考 即使是错过了不会损失太大 如果上错了船那就代价大了 很多市面上流行的概念也好方案也好水分很大   
16:03:15	php不了解多少 一个请求一个进程的方式是吗 访问量少当然快 大了是直接考验系统能力了 可能理解有误啊   
16:11:15	[OK]   
16:27:29	php 不是 性能爆表了吗 世界上最好的变成语言[呲牙]   
17:12:21	这个风控架构是适用于哪里的   
17:17:52	[强]   
17:19:13	这个风控系统是实时的吗？   
17:19:24	就是交易直接送风控系统   
17:19:44	处理时间大约多长时间？   
17:20:06	实时和准实时吧   
17:24:11	[鼓掌]   
17:24:15	准实时应该，时间百毫秒级别吧   
17:24:34	那不错   
17:24:44	百毫秒到秒级   
17:24:55	交易场景反欺诈。才是你们说的这样   
17:25:07	这样风控应该是以规则为主吧   
17:25:12	风控必须要在100ms内返回结果   
17:25:43	真正的风控，没有实时一说，有的公司，有自动风控，偏向于较简单的因子项   
17:25:44	里面也有实时的好像   
17:25:46	风控要求的是准实时性   
17:26:10	更多的风控系统做的事风控决策，有部分决策建议是实时的。   
17:26:15	那天问过财付通的，他们的交易一般处理时间不高于300毫秒   
17:26:28	加上监控和响应   
17:26:40	规则的话，可以做到实时啊   
17:26:58	结果响应也是实时   
17:27:14	当然也有准实时   
17:27:32	这个检查的是交易场景反欺诈。   
17:27:34	好厉害啊   
17:27:43	[强]   
17:27:54	各位 限额限次 你们是放风控系统还是单独抽出来做？   
17:28:07	盗刷或者其他的异常。   
17:28:08	如果分开 是先过风控还是限额限次？   
17:28:15	风控应该需要加上更多的纬度因子对交易进行验证   
17:28:35	对的   
17:28:40	资金上，只能发现关联性   
17:28:41	尽量多的数据   
17:28:47	嗯   
17:28:55	类似准入。   
17:31:49	其实交易数据还是有限   
17:38:53	没想到风控的需求这么复杂 就是识别一个异常吧 另一个是快速响应   
17:42:41	复杂就在于识别异常。   
17:43:00	问一下那个地方有比较详细的介绍风控规则吗？   
17:43:45	异常不好识别，可以识别正常   
17:45:57	@XXX深圳?财付通有这样共享的文档么，是不是也可以分享下你们那边的做法？   
17:46:20	[皱眉]   
17:46:24	识别异常 就是根据多维度识别 有业务数据 也有设备数据   
17:46:37	很期待你们财付通那边做法   
17:48:31	对于风控，规则属于涉密的数据。能够对外提供的，也是一些通用的，简单的规则。这种自己想想也能知道有什么了。基于那么几个维度。   
17:49:37	大家多讨论，思路就会明朗，文档这样的东西不是很好分享，多维度的数据收集才是风控的核心   
17:50:38	数据是基础   
17:50:58	没数据，再多的规则，再好的模型，也只是摆设。   
17:53:49	规则主要就是： 上下文Context、统计Stats、信誉Reputation、计数Count、模式pattern、速率Velocity等类型及其组合   
17:54:06	@XXX深圳?那真的好可惜，太遗憾了[捂脸]   
17:54:28	问个问题 风控系统应该是个很独立的产品 如果在做支付交易的时候 需要某些数据 比如用户的一些数据 该怎么获取？让支付系统送还是自己通过接口查？但支付系统可能并不关心这些信息，（支付系统也不想查） 如果风控系统自己查 必然会影响响应时间 该怎么处理？   
17:54:56	这里说的查 是调用用户相关接口   
17:55:46	@XXX苏州?[憨笑]大家都在摸索   
17:56:13	我看有个思路是键盘击打的频率，时间间隔，然后建模，确实熟练的人和盗卡首次熟人的人还是在模型上能区分开的   
17:56:14	嗯，一起摸索[机智]   
17:57:03	感觉应该分级别 比如涉及到钱的应该严密监控 未产生钱变动的可以慢点响应 另外既然风控这么敏感 软件设计时在正常流程上应该给风控强行介入留个接口吧 风险产生的可能只有万分之一 但是这么看风控消耗的资源可能是十分之一 呵呵   
18:03:19	另一个思路是延时分析 比如确立异常等级 一旦级别高的出现了才启动全模型检测分析 没出现高级别异常前就是记录日志 这样把资源用到核心的处理上   
18:04:58	风控系统 有接口规范 需要的数据写在规范里，调用者按规范传要素 就完，至于分级 什么的 都是内部处理方式了   
18:10:52	我两个手机号在微信里绑定银行卡 都绑定成功了 过阵子微信说我帐号异常需要他人认证才能解锁 级别应该是有涵盖优先权重这些概念的 银行卡绑定成功但是被其他规则给否定了 合理吗   
18:18:25	可能他设置一个手机多个号的危险等级比银行账户可信度的级别更高？   
18:38:58	真正涉及到钱变动的流程也不会很多吧 比如转账 而且从启动转账到完成中间环节多耗时长 要监控也不是难事 其他次要的记日志然后离线跑分析就可以了   
   
      
