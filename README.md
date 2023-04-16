# 乐健体育

> 代码兼容 Quantumult X

> 每日活动 自动报名、自动签退

> 主要适配 uestc 沙河校区，其余学校或校区可以自行抓包更改参数

> boxjs订阅 https://raw.githubusercontent.com/MCdasheng/QuantumultX/main/mcdasheng.boxjs.json

> 需要在boxjs中填入以下参数: 

>     legym_loginBody (包含用户密码、学校信息)
>     legym_signBody  (日更、手动签到时自动获取)

## 配置 (Quantumult X)

```properties

[rewrite_local]
^https\:\/\/cpes\.legym\.cn\/education\/activity\/app\/attainability\/sign url script-request-body https://raw.githubusercontent.com/MCdasheng/Legym/main/legym_sign.cookie.js

[task_local]
30 10 * * * https://raw.githubusercontent.com/MCdasheng/Legym/main/legym.js, tag=乐健体育报名, img-url=figure.disc.sports.system, enabled=true
30 16 * * * https://raw.githubusercontent.com/MCdasheng/Legym/main/legym_sign.js, tag=乐健体育签退, img-url=figure.disc.sports.system, enabled=true

[MITM]
hostname = cpes.legym.cn

```
