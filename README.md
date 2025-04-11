
README.md
GMGN.ai wallet_mark_multichain 数据导出工具
本工具用于从 https://gmgn.ai/ 的 localStorage 中导出 wallet_mark_multichain 数据，并将其转换为 地址:标签 格式（例如 7vgLiMobieR1KvuociQSj17byPS6svrqLLaLXLLm6zmH:aaa），保存为文本文件。
操作步骤：通过 F12 开发者工具导出
以下是通过浏览器开发者工具导出的详细步骤，全程无需安装额外软件。
打开 GMGN.ai 网站  
打开你的浏览器（推荐 Chrome、Edge 或 Firefox）。  
访问 https://gmgn.ai/。  
注意：确保你已登录或完成必要操作（如连接钱包），以保证 wallet_mark_multichain 数据已生成。
打开开发者工具  
在 https://gmgn.ai/ 页面，按键盘上的 F12 键。  
或者，右键点击页面空白处，选择“检查”或“审查元素”。  
这会打开开发者工具窗口。
切换到 Console 面板  
在开发者工具窗口顶部，找到 Console（控制台）选项卡，点击切换。  
如果看不到 Console，可能需要点击 >> 或其他扩展菜单找到它。
粘贴并运行代码  
复制以下 JavaScript 代码：

在 Console 面板中，点击空白处，粘贴代码（右键粘贴或按 Ctrl+V）。  
按 回车 键运行代码。
检查导出结果  
如果成功，浏览器会自动下载一个名为 wallet_mark_multichain.txt 的文件。  
打开文件，内容将类似以下格式（每行一个地址和标签）：
7vgLiMobieR1KvuociQSj17byPS6svrqLLaLXLLm6zmH:aaa
在 Console 面板中，你会看到类似以下输出：
成功导出到 wallet_mark_multichain.txt
如果看到错误信息，例如：
错误：未找到 wallet_mark_multichain 数据：说明 wallet_mark_multichain 未生成，请确认是否已登录或连接钱包。
导出失败：...：可能是数据格式问题，请联系支持。
验证文件  
打开下载的 wallet_mark_multichain.txt 文件，确认内容是否正确。  
如果文件为空或未下载，检查 Console 的错误提示并确保已正确执行步骤。
注意事项
必须在 GMGN.ai 运行：代码需在 https://gmgn.ai/ 页面运行，localStorage 数据与网站域名绑定。  
登录状态：如果 wallet_mark_multichain 需要登录或连接钱包（如 Phantom、Telegram 钱包）后生成，请先完成相关操作。  
数据安全：导出的文件可能包含敏感信息（如钱包地址和标签），请妥善保存，避免泄露。  
浏览器支持：推荐使用最新版本的 Chrome、Edge 或 Firefox，旧版浏览器可能不完全支持。
示例输出
假设 wallet_mark_multichain 数据为：
json
{
  "bsc": {},
  "sol": {
    "7vgLiMobieR1KvuociQSj17byPS6svrqLLaLXLLm6zmH": "aaa"
  }
}
导出的 wallet_mark_multichain.txt 内容为：
7vgLiMobieR1KvuociQSj17byPS6svrqLLaLXLLm6zmH:aaa
常见问题
Q：运行后没有下载文件？
A：检查 Console 是否有错误提示，可能未登录或 wallet_mark_multichain 未生成。尝试重新登录或刷新页面后重试。  
Q：导出的文件是空的？
A：说明数据中没有有效的地址和标签。请确认 wallet_mark_multichain 是否包含数据。  
Q：我想导出为其他格式（如 CSV）？
A：请联系开发者，提供具体需求（如 address,label 的 CSV 格式）。
