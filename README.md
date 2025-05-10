# IntusVia

個人に寄り添う記憶チャットシステム

**IntusVia** は、あなたの内面（Intus）を時間の流れ（Via）とともに紡ぎ、会話を通じて記憶を保持・活用する次世代チャットパートナーです。

---

## 🔖 Features

* **継続的なコンテキスト管理**
  ユーザーとの対話履歴をトピカルに整理し、会話の前後関係を維持します。
* **パーソナライズドメモリー**
  ユーザーの好み・興味・過去の問いかけを蓄積し、適切に参照します。
* **プライバシー重視**
  ローカルストレージまたは指定の安全なクラウドにのみデータを保存。
* **拡張可能なプラグイン**
  カスタムメモリーモジュールや分析プラグインを自由に追加可能。

## 🚀 Getting Started

### Prerequisites

* Python 3.8+
* pip
* （任意）Docker

### Installation

```bash
# リポジトリをクローン
git clone https://github.com/<your-org>/IntusVia.git
cd IntusVia

# 仮想環境を作成
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# 必要なパッケージをインストール
pip install -r requirements.txt
```

### Usage

```bash
# 環境変数に OpenAI API キーを設定
export OPENAI_API_KEY=your_api_key

# サーバーを起動
python app.py
```

初回起動後、`http://localhost:8000` にアクセスするとチャットインターフェースが利用できます。

## 🛠️ Architecture

```
+-----------------+     +---------------------+     +-------------+
|  Frontend (UI)  | <-- |   API Server (FastAPI)  | --> | Memory DB  |
+-----------------+     +---------------------+     +-------------+
                                 |
                                 v
                          +-----------------+
                          |  OpenAI LLM API |
                          +-----------------+
```

* フロントエンド：React + Tailwind CSS
* バックエンド：FastAPI
* データベース：SQLite / PostgreSQL
* メモリー管理：カスタム ORM レイヤー

## 📅 Roadmap

* [ ] 会話履歴の検索・フィルタ機能
* [ ] プラグインマーケットプレイス
* [ ] モバイル対応 UI
* [ ] エンドツーエンド暗号化オプション

## 🤝 Contributing

1. Fork  the repository
2. Create  a branch (`git checkout -b feature/YourFeature`)
3. Commit  your changes (`git commit -m 'Add some feature'`)
4. Push  to the branch (`git push origin feature/YourFeature`)
5. Open  a Pull Request

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

© 2025 IntusVia Project
