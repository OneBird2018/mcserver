

# Minecraft基岩版粉丝网站 - 免责声明与代码指南

## 📜 免责声明

**本项目为粉丝创作的非官方作品，与Mojang Studios/Microsoft无任何关联**

1. **版权声明**  
   - 所有Minecraft游戏内容版权归 [Mojang Studios](https://www.minecraft.net/) 和 Microsoft 所有
   - 本项目中使用的游戏截图、图标等资源仅用于教育目的，符合 [Mojang品牌指南](https://www.minecraft.net/zh-hans/brand)
   - 如涉及侵权请提交Issue，我们将立即移除相关内容

2. **使用限制**  
   - 禁止将本项目用于商业用途
   - 禁止声称此项目为官方产品
   - 二次发布需保留原始免责声明

3. **免责条款**  
   ```plaintext
   本项目按"原样"提供，不承担任何因使用此代码导致的直接或间接损失
   包括但不限于：账号封禁、设备损坏、数据丢失等风险
   ```



## 💻 代码结构详解

### 🏗️ 项目架构
```
.
├── index.html                # 主页面

```

### 🎨 核心技术亮点

#### 1. 像素风格实现
```css
/* 使用8-bit字体 */
font-family: 'Press Start 2P', cursive;

/* 像素边框效果 */
border: 4px solid #3B8526;
box-shadow: 4px 4px 0 #6D4C35;

/* 纯CSS像素问号图标 */
.pixel-help::before {
    box-shadow: 
        2px 0 0 var(--mc-light),
        4px 0 0 var(--mc-light),
        ... /* 精确控制每个像素 */
}
```

#### 2. 智能下载跳转
```javascript
fetch('https://ipapi.co/json/')
    .then(response => response.json())
    .then(data => {
        // 中国大陆用户跳转网易版
        if (data.country === 'CN') {
            window.location.href = 'https://mc.163.com/';
        } else {
            window.location.href = 'https://www.minecraft.net/download';
        }
    })
```

#### 3. 响应式设计
```css
@media (max-width: 768px) {
    /* 移动端适配 */
    .nav-links {
        flex-direction: column;
    }
    .pixel-help {
        right: 10px;
    }
}
```

### 🛠️ 部署指南

1. **基础部署**
   ```bash
   # 克隆仓库
   git clone https://github.com/yourusername/minecraft-bedrock-fansite.git
   
   # 部署到GitHub Pages
   # 1. 仓库设置 → Pages → 选择main分支
   # 2. 访问 https://yourusername.github.io/minecraft-bedrock-fansite/
   ```

2. **自定义配置**
   - 修改 `index.html` 中的服务器IP：
   ```html
   <div class="server-ip">IP: <strong>your.server.ip</strong></div>
   ```
 
---

## 📚 学习资源

- [Mojang官方品牌规范](https://www.minecraft.net/zh-hans/brand)
- [Minecraft Wiki（红石教程）](https://minecraft.fandom.com/zh/wiki/红石电路)
- [CSS像素艺术教程](https://css-tricks.com/create-pixel-art-with-css/)

---

## 🤝 贡献建议

欢迎通过Pull Request提交改进：
1. 添加更多建筑风格示例
2. 完善红石教程内容
3. 优化移动端体验

**请确保所有提交内容不包含版权受限素材**

---

> 📢 此项目仅为技术演示用途，不替代官方产品  
> 官方游戏请访问 [minecraft.net](https://www.minecraft.net/)

