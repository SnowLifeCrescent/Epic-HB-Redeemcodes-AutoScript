# Epic-HB-RedeemCodes-AutoScript

![兑换](https://github.com/user-attachments/assets/008abea9-c011-4dee-8abf-4ef2f24e5ba2)


## 仓库说明
该库由两部分JavaScript代码构成：

1. 在 HumbleBundle 的购买后页面使用的脚本，文件为 `HB-RedeemCodes.txt`，用于批量获取兑换码。

   ![image](https://github.com/user-attachments/assets/04dda569-0ea3-4ab8-a492-e26023076665)


2. 在 Epic 商城的兑换码使用页面使用的脚本，文件为 `Epic-RedeemCodes.txt`，用于批量使用兑换码。

   ![image](https://github.com/user-attachments/assets/cc8a8095-4a43-4b94-8a8c-91387eb0734d)


3. HB 的脚本与 Epic 商城的脚本是互相独立的。想要在 Epic 商城批量使用非从 HB 获得的兑换码理论上完全可行。

## 使用说明

### HB-RedeemCodes 使用说明

1. 打开你的 HB 感谢购买页面。
2. 点击获取所有隐藏的兑换码。
3. 按下 `F5` 刷新页面。
4. 按下 `F12` ，打开检查。
5. 在控制台中粘贴 `HB-RedeemCodes.txt` 中的文本内容并按下回车。
6. 你将会在控制台得到类似如下回显打印：
 ```
提取的兑换码: (1)['THISI-SASIM-PLEEX-AMPLE']
 ```

7. 请选中方括号 `[]` 中的所有内容并复制（包含方括号 `[]`）。

   *例如：`['THISI-SASIM-PLEEX-AMPLE']`*

### Epic-RedeemCodes 使用说明

1. 打开你的 Epic 商城兑换码使用页面。
2. 按下 `F12` ，打开检查。
3. 在控制台中粘贴 `Epic-RedeemCodes.txt` 中的文本内容，*__并注意不要按下回车__*。
4. 向上找到 `const codes = ;` 并在分号 `;` 前粘贴你的兑换码。
```
...
...
   const codes = [
    'THISI-SASIM-PLEEX-AMPLE'
    // ... 其它兑换码
];

redeemCodes(codes);
```

5. 检查你粘贴的兑换码是否自带了一重 `[]`，如若没有，请补上。
6. 按下回车，等待脚本执行。
   执行过程中有如下要点：

   - 在脚本输入当前兑换码时请不要按动任何按键；
   - 在当前兑换码输入完成后，请手动按下一次 `空格键`（此为手动使能兑换按钮，否则按钮将不会亮起，无法兑换）；
   - 按下 `空格` 后，此时脚本应自动兑换并尝试输入下一个兑换码；
   - 如果存在某一资产已经拥有、某一代码已经使用等情况（兑换按钮不亮），请按下一次 `回车键` 以对当前兑换码进行跳过；
     
     ![跳过](https://github.com/user-attachments/assets/9ee4621d-4473-40ca-aeda-6c9b95795875)

   - 如果存在网络中断、浏览器闪退等意外情况，导致脚本兑换过程中断，请重新运行脚本。其中，对已使用的兑换码请按照上条中内容所述进行处理。
