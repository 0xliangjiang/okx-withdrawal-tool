# OKX Batch Withdrawal Tool | OKX批量提币工具

[English](#english) | [中文](#chinese)

<a name="english"></a>
# English

A Python-based tool for batch cryptocurrency withdrawals on OKX exchange.

## Features

- Query currency and chain information
- Batch withdrawal to multiple addresses
- Random withdrawal amount within specified range
- Configurable delay between withdrawals
- Support for multiple blockchain networks

## Prerequisites

- Python 3.7+
- OKX API credentials (API Key, Secret Key, Passphrase)
- Valid withdrawal addresses

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/okx-withdrawal-tool.git
cd okx-withdrawal-tool
```

2. Install required packages:
```bash
pip install python-okx tabulate
```

## Configuration

1. Update API credentials in `wallet/okx_wallet.py`:
```python
apikey = "YOUR_API_KEY"
secretkey = "YOUR_SECRET_KEY"
passphrase = "YOUR_PASSPHRASE"
```

2. Configure withdrawal settings in `WITHDRAWAL_CONFIG`:
```python
WITHDRAWAL_CONFIG = {
    "currency": "ETH",              # Currency to withdraw
    "chain": "ETH-Base",           # Blockchain network
    "amount_range": (0.002, 0.0024), # Random amount range
    "delay_range": (5, 30)         # Random delay range in seconds
}
```

3. Prepare address file:
- Create a text file with one address per line
- Default path: `wallet.txt`
- Addresses can be with or without '0x' prefix

## Usage

1. Run the script:
```bash
python okx_withdrawal.py
```

2. Available options:
- Query Currency: Check currency and chain information
- Start Batch Withdrawal: Begin the batch withdrawal process
- Exit: Close the program

## Security Notes

- Keep your API credentials secure
- Test with small amounts first
- Verify addresses before withdrawal
- Enable IP restrictions on OKX API
- Set appropriate withdrawal limits

## Error Handling

The tool includes error handling for:
- Invalid API credentials
- Network connection issues
- Invalid addresses
- Insufficient balance
- API rate limits

## Disclaimer

This tool is for educational purposes only. Use at your own risk. Always verify transactions before confirming.

## License

MIT License

## Contributing

Feel free to submit issues and pull requests.

---

<a name="chinese"></a>
# 中文

基于Python的OKX交易所批量提币工具。

## 功能特点

- 查询币种和链信息
- 批量向多个地址提币
- 随机提币金额（可配置范围）
- 可配置提币间隔时间
- 支持多个区块链网络

## 环境要求

- Python 3.7+
- OKX API凭证（API密钥、Secret密钥、密码短语）
- 有效的提币地址

## 安装步骤

1. 克隆仓库：
```bash
git clone https://github.com/yourusername/okx-withdrawal-tool.git
cd okx-withdrawal-tool
```

2. 安装依赖包：
```bash
pip install python-okx tabulate
```

## 配置说明

1. 在 `okx_withdrawal.py` 中更新API凭证：
```python
apikey = "你的API密钥"
secretkey = "你的Secret密钥"
passphrase = "你的密码短语"
```

2. 配置提币设置 `WITHDRAWAL_CONFIG`：
```python
WITHDRAWAL_CONFIG = {
    "currency": "ETH",              # 提币币种
    "chain": "ETH-Base",           # 区块链网络
    "amount_range": (0.002, 0.0024), # 随机金额范围
    "delay_range": (5, 30)         # 随机延迟范围（秒）
}
```

3. 准备地址文件：
- 创建文本文件，每行一个地址
- 默认路径：`wallet.txt`
- 地址可以带或不带'0x'前缀

## 使用方法

1. 运行脚本：
```bash
python okx_withdrawal.py
```

2. 可用选项：
- 查询币种：检查币种和链信息
- 开始批量提币：启动批量提币流程
- 退出：关闭程序

## 安全提示

- 妥善保管API凭证
- 先用小额测试
- 提币前验证地址
- 启用OKX API的IP限制
- 设置合适的提币限额

## 错误处理

工具包含以下错误处理：
- 无效的API凭证
- 网络连接问题
- 无效地址
- 余额不足
- API限流

## 免责声明

本工具仅用于教育目的。使用风险自负。请在确认交易前仔细验证。

## License | 许可证

MIT License

## Contributing | 贡献

欢迎提交问题和拉取请求。
