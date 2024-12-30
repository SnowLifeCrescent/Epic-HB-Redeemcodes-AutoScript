# Epic-HB-RedeemCodes-AutoScript

![Redeem](https://github.com/user-attachments/assets/008abea9-c011-4dee-8abf-4ef2f24e5ba2)


- [English README](README.en.md)
- [中文说明](README.zh.md)


## Repository Description
This repository consists of two parts of JavaScript code:

1. The script used on the HumbleBundle purchase confirmation page, found in the file `HB-RedeemCodes.txt`, used for batch retrieving redemption codes.

   ![image](https://github.com/user-attachments/assets/04dda569-0ea3-4ab8-a492-e26023076665)


2. The script used on the Epic Games Store redemption page, found in the file `Epic-RedeemCodes.txt`, used for batch redeeming codes.

   ![image](https://github.com/user-attachments/assets/cc8a8095-4a43-4b94-8a8c-91387eb0734d)


3. The scripts for HB and Epic Games Store are independent of each other. It is theoretically possible to redeem codes in bulk on Epic that were not obtained from HB.

## Usage Instructions

### HB-RedeemCodes Usage Instructions

1. Open your HB (HumbleBundle) thank you purchase page.
2. Click to retrieve all hidden redemption codes.
3. Press `F5` to refresh the page.
4. Press `F12` to open Developer Tools.
5. Paste the content of `HB-RedeemCodes.txt` into the console and press Enter.
6. You will see output similar to the following in the console:

 ```
提取的兑换码: (1)['THISI-SASIM-PLEEX-AMPLE']
 ```

7. Select all the content within the square brackets `[]` and copy it (including the square brackets `[]`).

  *For example: `['THISI-SASIM-PLEEX-AMPLE']`*

### Epic-RedeemCodes Usage Instructions

1. Open your Epic Games Store redemption code usage page.
2. Press `F12` to open Developer Tools.
3. Paste the content of `Epic-RedeemCodes.txt` into the console, *__and make sure not to press Enter__*.
4. Scroll up to find `const codes = ;` and paste your redemption codes before the semicolon `;`.

```
...
...
   const codes = [
    'THISI-SASIM-PLEEX-AMPLE'
    // ... 其它兑换码
];

redeemCodes(codes);
```

5. Check if your pasted redemption code already contains square brackets `[]`. If not, make sure to add them.
6. Press Enter and wait for the script to execute.
   During execution, the following points should be noted:

   - Do not press any keys while the script is inputting the current redemption code;
   - After the current redemption code is entered, manually press the `space bar` once (this manually enables the redeem button, otherwise it will remain inactive and you will not be able to redeem);
   - After pressing `space`, the script should automatically redeem and attempt to input the next redemption code;
   - If any asset is already owned or a code has already been used (the redeem button does not light up), press `Enter` to skip the current redemption code;
     
     ![Skip](https://github.com/user-attachments/assets/9ee4621d-4473-40ca-aeda-6c9b95795875)

   - If there is a network interruption, browser crash, or any other unexpected issue that causes the script to stop, please rerun the script. For already used codes, please follow the instructions above to skip them.


