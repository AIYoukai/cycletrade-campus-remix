# CycleTrade Campus

面向香港高校的校园二手单车交易平台，CDT504「产品-服务一体化系统」课程交互原型。

**在线预览：** https://aiyoukai.github.io/cycletrade-campus-remix/

## 这是什么

一个单文件的静态交互原型：车架号核验、12 项官方验车报告、第三方担保交易、线下合作车行交付。所有数据都是模拟的，不产生真实交易。

## 页面

- **首页**：Z 型动线，验车报告样例、平台数据与在售车辆
- **在售车辆**：搜索、价格/校区/车型/成色筛选、排序、收藏、车辆详情
- **服务流程**：七阶段时间线、资金托管与履约金规则、方法论映射
- **我的订单**：看车预约、担保订单状态机、退款与确认收货
- **后台审核**：车架号核验队列、上架审核、争议工单
- **发布闲置**：两步表单，含香港手机号校验与验车预约

## 本地运行

页面是纯静态的，直接打开 `index.html` 即可；建议起一个本地服务：

```bash
python3 -m http.server 8000
# http://localhost:8000
```

唯一外部依赖是 Tailwind CSS CDN，断网时样式会失效；车辆插画全部是内联 SVG。

## 结构

```
index.html          单页应用（结构 + 样式 + 交互）
FEATURES.md         功能核对清单与已知问题
STYLE-BRIEF.md      风格改造记录与设计 token
docs/style/         四份风格参考（Z / corporate-clean / japanese-fresh / Neumorphism）
```

## 说明

- 演示数据写死在 `index.html` 里，刷新即重置
- 无后端、无登录、无真实支付
- 基线来自 [youleyuanmax-svg/cycletrade-campus](https://github.com/youleyuanmax-svg/cycletrade-campus)，本仓库是风格与结构魔改版
- 仅用于课程展示，不构成真实交易
