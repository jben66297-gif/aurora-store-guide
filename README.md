# aurora-store-guide
Aurora Store 使用注意事项
# Aurora Store 避坑指南
## 📌 背景
Aurora Store 是一个第三方应用商店，可以让没有 Google Play 服务的设备也能下载应用。  
但很多新手第一次使用时会遇到报错，尤其是 SSL 握手失败或“设备不兼容”的提示。
## ❌ 常见问题
- **SSL 报错**：`SSLHandshakeException: connection closed`，握手失败，无法下载。  
- **设备不兼容**：伪装机型不对，提示“应用和手机不匹配”。  
- **内核不匹配**：伪装机型的 ABI 架构与应用要求不符。  
## ✅ 解决方案
1. **启用伪装功能**  
   - 在 Aurora 设置中选择 Pixel 或三星 Galaxy 等主流机型。  
   - 推荐机型：Pixel 9a / Pixel 9 Pro Fold、Galaxy S25 Ultra / S20+。  2. **选择合适的架构和 API Level**  
   - 确认伪装机型支持 arm64-v8a，与大多数现代应用兼容。  
   - 避免只支持 armeabi-v7a 的老机型（如 BRAVIA VU2、Nokia 1.3）。  
3. **辅助措施**  
   - 校准系统时间与时区。  
   - 更新 WebView/浏览器组件。  
   - 切换 VPN 节点，避免出口拦截。  
## 🧠 原理简述
- Aurora 默认使用设备真实 TLS 指纹，部分网络/CDN 会拒绝。  
- 伪装功能改变握手特征和 User-Agent，让设备看起来像主流机型。  
- 因此报错并非应用不兼容，而是网络策略与身份校验问题。  
## 🔗 备用商店
如果 Aurora 仍然无法使用，可以尝试：  
- [APKPure](https://apkpure.com)  
- [Uptodown](https://uptodown.com)  
- [APKMirror](https://www.apkmirror.com)  
- [F-Droid](https://f-droid.org)  
## 📑 总结
新手第一次接触 Aurora Store 时，遇到报错不要慌。  
先试 Pixel 伪装，再试三星或小米主流机型。  
记住：报错不是终点，伪装才是暗门。
