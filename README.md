# hw2
| 任務 | 說明           | 需時(天) | 前置任務    | 開始時間 | 結束時間 |               
|:------:|:----------------:|:----------:|:--------------:|:----------:|:----------:|
| 1    | 研擬計畫       | 1        | -           | 第1天    | 第1天    |                
| 2    | 任務分配       | 4        | 1            | 第2天    | 第5天    |                    
| 3    | 取得硬體       | 17       | 1            | 第2天    | 第18天   |                     
| 4    | 程式開發       | 70       | 2            | 第6天    | 第75天   |                     
| 5    | 安裝硬體       | 10       | 3            | 第19天   | 第28天   |                     
| 6    | 程式測試       | 30       | 4            | 第76天   | 第105天  |                     
| 7    | 撰寫使用手冊   | 25       | 5            | 第29天   | 第53天   |                     
| 8    | 轉換檔案       | 20       | 5            | 第29天   | 第48天   |                     
| 9    | 系統測試       | 25       | 6            | 第106天  | 第130天  |                     
| 10   | 使用者訓練     | 20       | 7, 8      | 第54天   | 第73天   |                     
| 11   | 使用者測試     | 25       | 9, 10      | 第131天  | 第155天  |                   

PERT/CPM圖
``` mermaid
graph LR
    A1[任務1: 研擬任務<br>開始: 2024-11-01<br>結束:2024-11-01<br>時長: 1天] --> A2[任務2: 任務分配<br>開始: 2024-11-02<br>結束: 2024-11-05<br>時長: 4天]
    A1 --> A3[任務3: 取得硬體<br>開始: 2024-11-02<br>結束: 2024-11-18<br>時長: 17天]
    A2 --> A4[任務4: 程式開發<br>開始: 2024-11-06<br>結束: 2025-01-15<br>時長: 70天]
    A3 --> A5[任務5: 安裝硬體<br>開始: 2024-11-19<br>結束: 2024-11-28<br>時長: 10天]
    A4 --> A6[任務6: 程式測試<br>開始: 2025-01-16<br>結束: 2025-02-14<br>時長: 30天]
    A5 --> A7[任務7: 撰寫使用手冊<br>開始: 2024-11-29<br>結束: 2024-12-23<br>時長: 25天]
    A5 --> A8[任務8: 轉換檔案<br>開始: 2024-11-29<br>結束: 2024-12-18<br>時長: 20天]
    A6 --> A9[任務9: 系統測試<br>開始: 2025-02-15<br>結束: 2025-03-09<br>時長: 25天]
    A7 --> A10[任務10: 使用者訓練<br>開始: 2024-12-24<br>結束: 2025-01-12<br>時長: 20天]
    A8 --> A10
    A9 --> A11[任務11: 使用者測試<br>開始: 2025-03-10<br>結束: 2025-04-03<br>時長: 25天]
    A10 --> A11
```

```mermaid
gantt
title 甘特圖
    dateFormat  YYYY-MM-DD
    section 任務
    研擬任務      :done,    des1, 2024-11-01, 1d
    任務分配      :active,  des2, after des1, 4d
    取得硬體      :         des3, after des1, 17d
    程式開發      :         des4, after des2, 70d
    安裝硬體      :         des5, after des3, 10d
    程式測試      :         des6, after des4, 30d
    撰寫使用手冊  :         des7, after des5, 25d
    轉換檔案      :         des8, after des5, 20d
    系統測試      :         des9, after des5, 25d
    使用者訓練    :         des10, after des7 des8, 20d
    使用者測試    :         des11, after des6 des9 des10, 25d
```

```
關鍵路徑(任務):1、2、4、6、9、11
```

