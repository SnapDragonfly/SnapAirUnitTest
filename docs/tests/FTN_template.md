# Feature Template

*Note 1: It's good to use english as communication language.*

*Note 2: We have to admit this is a project launched by mainly Chineses.*

*Note 3: It's welcomed that the test case is using English as description language, especially API tests.*

*Note 4: Chinese is also accepted by description of manual test.*

#
Below is an example for test cases.
#


# Feature: FTN_06_004_03 账号密码-登录

## Test Case 1

- 测试编号: FTN_06_004_03_01
- 测试内容: 账号密码-登录-未注册场景
- 前提条件: 
> 1. 平台功能正常 
> 2. 无账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：master
>   - 密码：123456
> 3. 点击【login】按钮，登录平台
- 判定标准:
> 1. PASS: 平台提示“该账号不存在”
> 2. FAIL: 平台提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员

#
## Test Case 2

- 测试编号: FTN_06_004_03_02
- 测试内容: 账号密码-登录-常规场景
- 前提条件: 
> 1. 平台功能正常 
> 2. 已存在账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：master
>   - 密码：123456
> 3. 点击【login】按钮，登录平台
- 判定标准:
> 1. PASS: 进入平台账号界面
> 2. FAIL: 平台提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员

#
## Test Case 3

- 测试编号: FTN_06_004_03_03
- 测试内容: 账号密码-登录-密码错误场景
- 前提条件: 
> 1. 平台功能正常 
> 2. 已存在账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：master
>   - 密码：654321 (错误密码)
> 3. 点击【login】按钮，登录平台
- 判定标准:
> 1. PASS: 平台提示“密码错误”
> 2. FAIL: 平台提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员


#
## Test Case 4

- 测试编号: FTN_06_004_03_04
- 测试内容: 账号密码-登录-账号错误场景
- 前提条件: 
> 1. 平台功能正常 
> 2. 已存在账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：masterr (错误账号)
>   - 密码：123456
> 3. 点击【login】按钮，登录平台
- 判定标准:
> 1. PASS: 平台提示“该账号不存在”
> 2. FAIL: 平台提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员

#
## Test Case 5

- 测试编号: FTN_06_004_03_05
- 测试内容: 账号密码-登录-空账号
- 前提条件: 
> 1. 平台功能正常 
> 2. 已存在账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：留空
>   - 密码：123456
> 3. 点击【login】按钮，登录平台
- 判定标准:
> 1. PASS: 平台提示“账号为空”
> 2. FAIL: 平台提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员

#
## Test Case 6

- 测试编号: FTN_06_004_03_06
- 测试内容: 账号密码-登录-空密码
- 前提条件: 
> 1. 平台功能正常 
> 2. 已存在账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：master
>   - 密码：留空
> 3. 点击【login】按钮，登录平台
- 判定标准:
> 1. PASS: 平台提示“密码为空”
> 2. FAIL: 平台提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员

#
## Test Case 7

- 测试编号: FTN_06_004_03_07
- 测试内容: 账号密码-登录-账号超长场景
- 前提条件: 
> 1. 平台功能正常 
> 2. 已存在账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：输入超长账号 > 15字符
>   - 密码：
- 判定标准:
> 1. PASS: 平台登录界面，账号输入框提示“已超过账号长度, 15字符”
> 2. FAIL: 平台登录界面，账号输入框提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员


#
## Test Case 8

- 测试编号: FTN_06_004_03_08
- 测试内容: 账号密码-登录-密码超长场景
- 前提条件: 
> 1. 平台功能正常 
> 2. 已存在账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：master
>   - 密码：输入超长账号 > 15字符
- 判定标准:
> 1. PASS: 平台登录界面，密码输入框提示“已超过账号长度, 15字符”
> 2. FAIL: 平台登录界面，密码输入框提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员


#
## Test Case 9

- 测试编号: FTN_06_004_03_09
- 测试内容: 账号密码-登录-账号特殊字符
- 前提条件: 
> 1. 平台功能正常 
> 2. 已存在账号和密码
- 测试步骤:
> 1. 输入平台登录页面URL (https://test.com/login)
> 2. 在登录界面输入账号和密码
>   - 账号：账号特殊字符
>   - 密码：123456
- 判定标准:
> 1. PASS: 平台登录界面，密码输入框提示“特殊字符，请注意”
> 2. FAIL: 平台登录界面，密码输入框提示除PASS以外信息 或者无提示
- 测试结果:
> PASS or FAIL
- 严重程度:
> 请参考: [Bug Priority & Severity](./Bug_Priority_Severity.md)
- 耗时时间(分钟): 1 分钟
- 原因分析:
> 根据平台登录界面提示信息，进行测试级别定位分析，并根据分析结果，将ISSUE指派给正确的处理人员