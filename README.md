
# 面试实操题目：Todo管理应用

## 任务目标
开发一个包含以下功能的Todo管理应用：
1. 实现一个可以添加、删除、标记完成Todo的主页面。
2. 实现一个详情页面，展示单个Todo的详细信息。
3. 通过父子组件传递数据和回调函数实现状态管理，而不使用Context API或Redux等高级工具。
4. 保持代码模块化，尽量复用组件。

---

## 任务拆解

### 1. 初始化项目
由候选人执行以下命令初始化一个React项目：
```bash
npx create-react-app todo-app
cd todo-app
npm start
```

---

### 2. 页面与路由
创建两个页面：
- **Todo列表页面**：显示所有Todo。
- **Todo详情页面**：展示单个Todo的详细信息。
- 使用`react-router-dom`实现页面间路由切换。

#### 路由结构示例：
- `/todos` 显示Todo列表页面。
- `/todos/:id` 显示某个Todo的详情页面。

---

### 3. 组件开发

#### 要求：
1. **TodoItem组件**：显示单个Todo项，支持“标记完成”和“删除”操作。
   - 点击“完成”按钮时，将Todo标记为完成状态。
   - 点击“删除”按钮时，从列表中移除该Todo。
2. **TodoForm组件**：提供输入框和按钮，允许用户添加新Todo。

---

### 4. Todo详情页面
在Todo列表页面，点击某个Todo项的“查看详情”按钮时，跳转到详情页面并显示其详细信息（如标题、完成状态、创建时间等）。

---

## 额外要求
- 使用父子组件通信管理数据。
- 添加简单的样式，使页面看起来不至于过于简陋（可用`CSS Modules`或`styled-components`）。
- 提供基本的表单验证（例如，添加Todo时输入框不能为空）。
- 在页面之间切换时，显示简单的加载状态（如“Loading...”）。
- 用户需要：
  1. 创建一个新的分支，例如：`feature/todo-app`。
  2. 将代码提交到该分支。
  3. 推送到 GitHub 仓库。

---

## 加分项
- 使用TypeScript开发。
- 添加“清空已完成任务”的功能按钮。
- 适当考虑代码复用，例如将相似逻辑封装成辅助函数。
