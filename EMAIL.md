# 邮箱模板

这个文件包含一些常用的邮箱模板，可以快速生成邮件。

## 验证码模板

该模板适用于邮箱验证码场景，请根据需要酌情修改。

<div style="border-bottom-left-radius: 5px;border-bottom-right-radius: 5px;">
    <div style="background: #67C23A;height: 3px;"></div>
    <dev style="padding-top: 200px;padding-bottom: 200px;text-align: center;background: white;">
        <h3>XXX 邮箱验证码</h3>
        <p>你正在进行邮箱验证操作，验证码为：</p>
        <div style="padding-left: 10px;padding-right: 10px;text-align: center;background: #f0f9eb;border-radius: 5px;"><strong style="color: #67C23A;letter-spacing: 3px;font-size: 23px">123456</strong></div>
        <p style="font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;margin-top: 50px;">此验证码 15 分钟内有效</p>
        <p style="font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;">如非本人操作</p>
        <p style="font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;">转给他人将导致账号被盗和个人信息泄漏，谨防诈骗</p>
        <p style="font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;margin-top: 50px;"><a href="https://dev.t1y.net/" target="_blank" style="color: #67C23A;">T1后端云</a> - 节省开发团队的每一分钟</p>
    </div>
</div>

### 代码

以下代码为双引号版本，部分不支持单引号变量的编程语言需要转义操作。

```html
<div style="border-bottom-left-radius: 5px;border-bottom-right-radius: 5px;">
    <div style="background: #67C23A;height: 3px;"></div>
    <dev style="padding-top: 200px;padding-bottom: 200px;text-align: center;background: white;">
        <h3>XXX 邮箱验证码</h3>
        <p>你正在进行邮箱验证操作，验证码为：</p>
        <div style="padding-left: 10px;padding-right: 10px;text-align: center;background: #f0f9eb;border-radius: 5px;"><strong style="color: #67C23A;letter-spacing: 3px;font-size: 23px">123456</strong></div>
        <p style="font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;margin-top: 50px;">此验证码 15 分钟内有效</p>
        <p style="font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;">如非本人操作</p>
        <p style="font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;">转给他人将导致账号被盗和个人信息泄漏，谨防诈骗</p>
        <p style="font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;margin-top: 50px;"><a href="https://dev.t1y.net/" target="_blank" style="color: #67C23A;">T1后端云</a> - 节省开发团队的每一分钟</p>
    </div>
</div>
```

单引号版本，若您的编程语言不支持单引号变量可以使用该版本，减去转义操作。

```html
<div style='border-bottom-left-radius: 5px;border-bottom-right-radius: 5px;'>
    <div style='background: #67C23A;height: 3px;'></div>
    <dev style='padding-top: 200px;padding-bottom: 200px;text-align: center;background: white;'>
        <h3>XXX 邮箱验证码</h3>
        <p>你正在进行邮箱验证操作，验证码为：</p>
        <div style='padding-left: 10px;padding-right: 10px;text-align: center;background: #f0f9eb;border-radius: 5px;'><strong style='color: #67C23A;letter-spacing: 3px;font-size: 23px'>123456</strong></div>
        <p style='font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;margin-top: 50px;'>此验证码 15 分钟内有效</p>
        <p style='font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;'>如非本人操作</p>
        <p style='font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;'>转给他人将导致账号被盗和个人信息泄漏，谨防诈骗</p>
        <p style='font-size: 12px;color: rgba(24, 24, 25, 0.42) !important;margin-top: 50px;'><a href='https://dev.t1y.net/' target='_blank' style='color: #67C23A;'>T1后端云</a> - 节省开发团队的每一分钟</p>
    </div>
</div>
```
