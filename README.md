# PDF 添加页码工具

本脚本为当前目录下的所有PDF文件批量添加页码：

- 🖨️ 自动创建"output"文件夹存储处理后的文件
- 🔢 支持为不同文档设置自定义起始页码
- 🧱 自动展平PDF解决注释兼容性问题
- ⚙️ 基于 PyMuPDF (fitz) 和 ReportLab 开发

# 环境依赖
安装依赖库：
``` bash
pip install PyMuPDF reportlab
```

> 注意：尽管代码中使用 import fitz，实际安装命令为 pip install PyMuPDF

# 使用说明

1. 将需要处理的PDF文件放入脚本所在目录
2. 运行脚本：
``` bash
python add_page_numbers.py  
```
3. 根据提示为每个PDF输入起始页码
4. 处理后的文件保存在 /output 目录


# 处理流程
​​
1. 展平PDF​​ → 移除不兼容的注释元素
​​2. 添加页码​​ → 在页面右下角生成白底黑色页码
​​3. 保存结果​​ → 原始文件名不变，存储至子文件夹

> 📝 ​​注意事项​​
> 
> 页码位置固定距页面右侧 1.2 英寸，底部 0.5 英寸
> 字号：14pt | 字体：Helvetica
> 临时展平文件会自动删除
> 支持所有常见页面尺寸（自动适配源文件）

*README由Deepseek生成*
