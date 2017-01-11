# Egret之list自定义item  
#### Egret 中提供list的控件，但是原生的list只支持label，很多时候我们都需要图标加不同位置的label。要想实现item的不同样式，只能自己定义item,对list的itemRendererSkinName 进行重新赋值。
## 示例代码如下：
自定义skin

```
<?xml version="1.0" encoding="utf-8"?>
<e:Skin class="GameMessageItem"  width="750" height="150" xmlns:e="http://ns.egret.com/eui" xmlns:w="http://ns.egret.com/wing">
	<e:Image id="gameImg" source="{data.gameImg}" width="117" height="117" x="24" anchorOffsetX="0" anchorOffsetY="0" verticalCenter="0"/>
	<e:Label id="gameName" text="{data.gameName}" x="176.06" fontFamily="SimHei" verticalCenter="-28"/>
	<e:Label id="tips" text="{data.tips}" x="176.06" anchorOffsetY="0" height="42.12" fontFamily="SimHei" verticalCenter="28" size="28"/>
	<e:Rect width="116" height="39" x="600.69" y="20.23" anchorOffsetX="0" anchorOffsetY="0" fillColor="0xe81010" ellipseWidth="15" ellipseHeight="15"/>
	<e:Label id="gameStatus" x="583.69" y="23.23" text="{data.gameStatus}" anchorOffsetX="0" width="146" anchorOffsetY="0" height="29" textAlign="center" fontFamily="SimHei"/>
	<e:Rect anchorOffsetX="0" anchorOffsetY="0" ellipseWidth="70" ellipseHeight="70" scaleX="1" scaleY="1" left="0" right="0" bottom="0" x="10" y="10" height="1" fillColor="0x545454"/>
</e:Skin>

```
## 效果如下：
![image](assets/images/avatar.jpg)
### 赋值代码
对原生的list控件的itemRendererSkinName 进行重新赋值就可以实现了。
var list = new eui.List();
list.itemRendererSkinName = ‘GameMessageItem’;
