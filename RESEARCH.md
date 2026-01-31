# 市场调研：Servicing Calculator 工具

## 一、市面主流工具分析

### 1. Aggregator 内置工具

#### AFG FLEX
- **优点：** 直接对接 lender 系统，政策自动更新
- **缺点：** 仅限 AFG broker，界面复杂
- **收入处理：** 完整的 shading matrix

#### Connective Mercury
- **优点：** 50+ lender 比较，与 CRM 集成
- **缺点：** 绑定 Connective 平台
- **特色：** Best-fit lender 推荐

#### Finsure Infynity
- **优点：** 一体化 CRM + Servicing
- **缺点：** 学习曲线陡
- **特色：** 自动 compliance 检查

---

### 2. 独立专业工具

#### ServiceCalc (servicecalc.com.au)
- **价格：** ~$99/月 专业版
- **优点：** 
  - 最专业的独立工具
  - 支持 resi + commercial
  - 政策更新快
  - 多 lender 比较
- **缺点：**
  - 界面老旧（像 2010 年代的网站）
  - 需要大量输入
  - 学习曲线陡
- **隐私：** 要求完整 PII

#### LoanApp
- **优点：** Servicing + Lodgement 一体
- **缺点：** 主要面向 lodgement，servicing 是附属功能
- **特色：** 自动填充申请表

---

### 3. 银行公开 Calculator

| 银行 | 公开工具特点 | 与真实差距 |
|------|-------------|-----------|
| CBA | 最简化，5 个问题 | 差距 30-50% |
| NAB | 稍详细，有投资选项 | 差距 20-40% |
| WBC | 中等详细 | 差距 20-30% |
| ANZ | 较详细，有 self-emp | 差距 15-25% |

**共同问题：**
- 不反映真实 credit policy
- Buffer 通常用较低数值（marketing 目的）
- 不考虑 existing commitments 的复杂性
- 无法处理 commercial 场景

---

### 4. 消费者工具

#### Canstar / RateCity
- 比较型网站的附属功能
- 极度简化
- 目的是获取 lead，不是准确计算

#### MoneySmart (ASIC)
- 政府教育工具
- 保守计算
- 无商业场景

---

## 二、竞品 UI/UX 分析

### 共同问题

1. **信息过载**
   - 一次性展示太多输入框
   - 用户不知道从哪里开始

2. **缺乏引导**
   - 没有 step-by-step wizard
   - 没有 tooltip 解释术语

3. **结果不直观**
   - 只显示最终数字
   - 看不到计算过程
   - 难以发现输入错误

4. **隐私问题**
   - 要求过多 PII
   - 数据存储不透明

### 最佳实践参考

| 工具 | 我们可以学习的 |
|------|--------------|
| Stripe Dashboard | 清晰的数据可视化 |
| Figma | 干净的 UI，减少干扰 |
| Linear | 键盘快捷键，高效操作 |
| Notion | 灵活的 block 结构 |

---

## 三、差异化机会

### 1. Privacy-First（独一无二）
市面上**没有**工具强调隐私。我们可以成为第一个：
- "No data stored" 作为核心卖点
- 只要必要信息，不多问
- Client-side only 计算

### 2. Visual Cash Flow（差异化）
- 大多数工具只给数字
- 我们给**可视化的资金流向图**
- 一眼看出钱从哪来、去哪里

### 3. Flexible Buffer（专业级）
- 消费者工具固定 buffer
- 我们允许专业用户调节
- 支持不同 lender tier 的不同规则

### 4. Combined Transaction（填补空白）
- 很少工具能同时处理 resi + commercial
- 这是高端 broker 的刚需

---

## 四、目标用户画像

### Primary: Mortgage Broker
- 需要快速估算客户 capacity
- 需要对比不同 lender
- 需要清晰的输出给客户看

### Secondary: Commercial Broker
- 需要处理复杂收入结构
- 需要 cash flow based 分析
- 需要灵活的 buffer 设置

### Tertiary: 高端消费者
- 想自己先算算
- 不想给 broker 太多个人信息
- 需要教育性内容理解结果

---

## 五、定价策略建议

### Option A: Freemium
- **Free:** Residential PAYG 基础版
- **Pro ($29/月):** Commercial + Combined + 高级功能

### Option B: 一次性购买
- **Standard ($99):** 终身使用
- **Pro ($199):** 含 commercial 模块

### Option C: 完全免费
- 作为 Oney & Co 的 marketing 工具
- 建立品牌认知和信任
- 通过 broker 服务变现

---

## 六、技术选型建议

### 前端框架
- **推荐：Vue 3 + Vite**
  - 轻量，响应式
  - 组件化，易维护
  - 优秀的 TypeScript 支持

### UI 库
- **推荐：TailwindCSS + Headless UI**
  - 快速开发
  - 高度自定义
  - 响应式设计

### 可视化
- **推荐：D3.js 或 Chart.js**
  - Cash flow 图表
  - 动态更新

### PDF 导出
- **推荐：html2pdf.js**
  - 简单直接
  - 保持页面样式

---

## 七、下一步行动

1. ✅ 完成市场调研
2. 🔄 创建基础 UI 原型
3. 🔜 实现 PAYG 计算逻辑
4. 🔜 添加可视化
5. 🔜 测试和迭代
