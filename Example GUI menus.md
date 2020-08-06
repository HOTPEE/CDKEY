# GUI菜单例子
这些帮助可以帮助你更好地制作自己的菜单

## [工具包](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/kits.yml)
这个实例能够简单的介绍如何制作一个工具包菜单， 这个例子菜单展现了三种不同的状态

比如什么时候能够领取，什么时候有冷却，什么时候不能领取(锁定中)

需要这个菜单正常工作 还需要下载 [Essentials](https://ci.ender.zone/job/EssentialsX/lastSuccessfulBuild/) 然后利用命令下载 Essentials 的占位符表达式

>/papi ecloud download Essentials
>/papi reload

## [矿区传送](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/mines.yml)

这个实例能够简单的介绍如何制作一个矿区传送菜单， 这个例子菜单展现了三种不同的状态

比如什么时候矿区解锁，什么时候允许挖矿，什么时候是锁定的

需要这个菜单正常工作 还需要下载 [EzRanksPro](https://www.spigotmc.org/resources/10731/) (需要付费) 然后利用命令下载 Essentials 的占位符表达式

>/papi ecloud download Player
>/papi ecloud download EzRanksPro
>/papi reload

## [跨服传送](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/serverselector.yml)

这个实例能够简单的介绍如何制作一个跨服传送菜单， 这个例子菜单展现了两种不同的状态

比如服务器开启时或关闭时的状态

需要这个菜单正常工作 还要利用命令下载 服务器相关占位符表达式

>/papi ecloud download Pinger
>/papi ecloud download Server
>/papi reload

在这个例子中，我们使用了在一个Bungeecord 服务器上的 2个不同子服 vanilla 服 和 games 服

假如我们现在已经在这个服务器游戏了

如果我们想要玩家连接到 vanilla 子服， 那么我们需要利用一些字符来设置 

left_click_commands: **相应节点
* * * 

在我们的例子中，我们首先使用 [close] 字符串 以使得先关闭菜单，然后利用 [message] 字符串来给玩家发送信息，最后使用 [connect] 来让玩家连接到相应服务器

为了让菜单显示该子服有多少玩家，我们要使用占位符 %pinger_players_<ip>:<port>%

值得注意的是，Pinger占位符有自己的刷新间隔，如果你更改了他 那么就去 PlaceholderAPI 的 config文件里 改变 check_interval: 的值 (默认是 30 秒)

但是如果服务器是关闭状态呢？

如果是这样的话，我们会使用更低优先级的第二物品，假如 第一物品的 view_requirement: 布尔值不是真，那么就会在菜单展示

所以如果服务器离线，我们可以显示其他东西，但是如果这个服务器从关闭变为开启，那么物品不会自动更新

但是我们可以通过玩家点击物品 然后触发 [refresh] 字符串来更新菜单!

第二个物品比较简单，因为我们已经连接到了，我们只需要发送消息即可

然后我们可以使用 %server_online% 占位符来显示服务器玩家数量

## [商城](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/store.yml)

这个实例能够简单的介绍如何制作一个商城菜单，然后通过虚拟经济系统来 达到在菜单上购买/出售物品的目的

需要这个菜单正常工作 还要利用命令下载 玩家， 物品检查 和 你要用的经济插件的相关占位符表达式

>/papi ecloud download Player
>/papi ecloud download CheckItem
>/papi ecloud download Vault
>/papi ecloud download TokenEnchant
>/papi ecloud download PlayerPoints
>/papi reload

[Vault](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/store.yml#L18-L59)
[TokenEnchant](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/store.yml#L61-L106)
[Player Points](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/store.yml#L108-L150)
[Player XP](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/store.yml#L152-L195)

## [META](https://github.com/help-chat/DeluxeMenus/blob/master/gui_menus/meta.yml)

简单的展示了 [meta](https://wiki.helpch.at/clips-plugins/deluxemenus/options-and-configurations#actions-types) 工作原理