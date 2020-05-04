# 在你的WP博客展示Steam游戏库，适用于绝大多数WP主题
作为一个爱玩游戏的人，博客怎么能没有你的游戏库呢！貌似这个页面好像并没有多少人有，所以我把他做出来了
本模版理论适配了大部分WP主题，部分布局比较奇葩的WP主题也能用但是可能需要改CSS，如果你们有更好看的样式，分享给我呗，秋泥膏~

`PS`：如果第一次打开样式有问题就把CSS添加到全局里

### 样式参考
https://github.com/HCLonely/hexo-steam-games

### 版本说明
#### 通用版&API版
优点：个人信息实时更新、页面加载快、支持选择展示类型和数量、可以通过API实现即时更新游戏库、支持缓存游戏库数据、适配所有地区服务器

缺点：用本地需要手动更新JSON数据，使用API需要找台境外的虚拟主机或者服务器（PHP环境）

##### 不使用API
1. 下载我项目中的文件，将`page-steam.php` 扔到你的主题根目录，修改此文件中的第14行为你的SteamID
`$steamid = "76561198849944519";`

2. 将`json`整个目录扔到你的站点根目录内，修改此目录内的 `steam.json` 文件内容为你的Steam游戏库的JSON
	怎么获取见此：[https://m1314.cn/327.html](https://m1314.cn/327.html "https://m1314.cn/327.html")

3. 信息填好后，后台新建页面选择 `Steam游戏库` 这个模版即可

##### 使用API
1. 下载我项目中的文件，将`page-steam.php` 扔到你的主题根目录，修改此文件中的第14行为你的SteamID，15行为你的API地址
`$steamid = "76561198849944519";$steamAPI = "http://你的域名/SteamAPI.php?id=76561198849944519&type=all";`
我免费提供了两个API但是不保证稳定性，在文章末尾获取

2. 将`page-steam.php`文件第19行用`//`注释掉，删除第22-29行之间的注释符`/*`，将`json`整个目录扔到你的站点根目录内

3. 信息填好后，后台新建页面选择 `Steam游戏库` 这个模版即可

#### 代理版&境外版
优点：个人信息实时更新、游戏库实时更新、支持选择展示类型和数量、适配境外服务器及部分大陆服务器（看脸）

缺点：页面处理速度取决于你的代理速度或你的服务器访问Steam社区的速度


1. 下载我项目中的文件，将`page-steam_proxy.php` 扔到你的主题根目录，修改此文件中的第15行为你的SteamID，其他看注释即可

2. 信息填好后，后台新建页面选择 `Steam游戏库代理版` 这个模版即可

### API说明
请求示例：`https://localhost/SteamAPI.php?id=76561198849944519&type=all`
| 值  | 参数  |
| :------------ | :------------ |
| id  | 你的SteamID  |
| type  | all为全部游戏，recent为最近游玩  |

### 演示
[Steam游戏库](https://m1314.cn/game/ "Steam游戏库")
