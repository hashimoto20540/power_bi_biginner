# power_bi_biginner

# 概要
書籍を一冊ハンズオンで取り組んだ

# OUTPUT
- power_bi_desktop概要レポート.png
- power_bi_desktop影響分析レポート.png
- power_bi_desktop分解分析レポート.png

# 学んだこと
- 環境構築
    - PowerBI desktop
    - PowerBI Service
        - ワークスペース作成
        - レポート発行の紐付け
        - オンプレのデータソースから自動更新スケジュールを設定
- BI開発の基本的な流れ
    - 要件定義
    - 元データ収集
        - データの種類
        - どこから取得するのか
    - データモデル（視覚化しやすい形にデータ構造）の作成
        - データの正規化
        - クレンジング（重複削除、表記揺れ）
        - インポート
        - リレーションシップ
    - 視覚化
        - グラフを作成して発行
- Power Queryを使用したデータモデリング
    - スタースキーマでテーブルを加工
        - factテーブルが中心で、dim（dimension）テーブルが外側
        - factと各dimは1対n
        - テーブルの正規化、リレーション、ER図
- DAXを使用してデータを加工
    - 計算列: 新しい列を作成
    - メジャー: CALCULATE関数
    - 日付テーブルの作成
- まとめ：契約分析レポートの作成（添付画像参照）
    - データ加工
        - データ分類（型）指定
        - 不要な列の非表示
        - スタースキーマでリレーションシップの設定
    - テーブル
        - モデルビュー（ER図）.pngに記載
        - SupportPage/Chapter7/SampleData_Chapter7.xlsx
    - 概要レポート
        - ビジュアルの種類
            - カード、スライサー、ウォーターフォール図、マップ、積み上げ横棒グラフ、ドーナツグラフ、マトリックス
    - 影響分析レポート
        - ビジュアルの種類
            - 積み上げ横棒グラフ
            - 主要なインフルエンサー
    - 分解分析レポート
        - ビジュアルの種類
            - マトリックス
            - 分解ツリー

# 参考書籍
青井航平他、PowerBI[実践]入門、技術評論社、2023年

# 参考サイト
- マップが表示されない
https://frogwell.co.jp/blogs/powerbi-map/

# 苦労点
- 会社や学生用のMicroSoftアカウントがなくpowerBIが使えなかった点→サブスクを購入するにも、何が対応できているか読み解く力が足りなかった
    - もともとMicroSoft365Personalを使用していたが、それでできるか試していたができず
    - 書籍には、Microsoft 365 Developer Program（Microsoft 365開発者プログラム）を使用すれば無料でできると記載されていたが、Instant sandboxの画面に遷移せず。Power BI以外のwordとかは使用できた
    - エラーをググると、
        - 2024/2まで、アカウント発行が一時停止中
        https://learn.microsoft.com/ja-jp/answers/questions/1531154/microsoft365-sandbox-subscription
        - 2024/2以降、完全無料でテナントを作成することはできなさそう
        https://learn.microsoft.com/ja-jp/answers/questions/1681736/microsoft-developer-program-1
        - 開発者ブログでは、Visual Studio Enterprise のアクティブなサブスクリプションを持つ開発者および/または組織に制限https://www.reddit.com/r/Office365/comments/1afn2vf/cant_get_microsoft_365_developer_program_sandbox/
    - 上記からMicrosoft 365 Developer Programは使用できなさそうと判断
    - PowerBIの使用方法を検索
        - Power BIサービスの利用は、職場や学校の、組織アカウントが必要
        https://www.powerplatformknowledge.com/powerbi-howtouse-basic5step/
        - Microsoft 365 Business Basicを無料で試した
            - 決済でエラーになってクレジットカードの登録はしなかったが、たまたま会社用のアカウントは作成された
            - 〇〇〇〇@〇〇〇[.onmicrosoft.com](mailto:hashikazu20540@hashimoto102.onmicrosoft.com)という形式のアカウントが作成された
    - 会社用のMicroSoftアカウントでpower BI DeskTopと、power BI serviceを利用することができた
    - 職場または学校のメール アカウントがない場合でも、Power BI Pro または Fabric (無料) の試用版を開始できるとのこと
        - https://learn.microsoft.com/ja-jp/power-bi/fundamentals/service-self-service-signup-purchase-for-power-bi?tabs=trial

