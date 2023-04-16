# 乐健体育

> 代码兼容 QuanX

> 详见 https://github.com/MCdasheng/QuantumultX/blob/main/Scripts/myScripts/legym.js

> 需要在boxjs中填入参数: 

>     legym_loginBody (包含用户密码、学校信息)

>     legym_signBody (日更、手动签到时自动获取)

## 配置 (QuanX)

```properties

[rewrite_local]
^https\:\/\/cpes\.legym\.cn\/education\/activity\/app\/attainability\/sign url script-request-body https://raw.githubusercontent.com/MCdasheng/QuantumultX/main/Scripts/myScripts/legym_sign.cookie.js

[task_local]
30 10 * * * https://raw.githubusercontent.com/MCdasheng/QuantumultX/main/Scripts/myScripts/legym.js, tag=乐健体育报名, img-url=figure.disc.sports.system, enabled=true
30 16 * * * https://raw.githubusercontent.com/MCdasheng/QuantumultX/main/Scripts/myScripts/legym_sign.js, tag=乐健体育签退, img-url=figure.disc.sports.system, enabled=true

[MITM]
hostname = cpes.legym.cn

```

