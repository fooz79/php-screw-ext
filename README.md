# php-screw-ext
PHP 混淆解密扩展

## 介绍

### 谁的肩膀

- 基于 https://sourceforge.net/projects/php-screw/
- 参考 https://github.com/del-xiong/screw-plus/

### 验证及解密流程

基于非对称密钥的解密权限验证

- 模块在编译时内置验证用开发者公钥

- 运行环境通过 ini 设置由开发者用公钥加密的许可证
  - 许可证包含下列信息
    1. 运行环境唯一值
    2. 有效期
    3. 混淆解密用密钥

- 许可证有效时，在读取 PHP 代码时对混淆的代码块同步解密

### TODO

- [ ] 了解 EXT Hook 的方法，确认要 Hook 的位置
- [ ] 解密扩展 
- [ ] 加密工具 (PHP)
