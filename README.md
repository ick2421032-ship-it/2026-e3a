<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RESEARCH APP / 課題研究ダッシュボード</title>
    <style>
        /* グラデーションとダークモードのベース設定 */
        :root {
            --bg-color: #0b0f19;
            --card-bg: #161b26;
            --accent-blue: #00f2fe;
            --accent-purple: #4facfe;
            --text-main: #f1f5f9;
            --text-sub: #94a3b8;
        }

        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.7;
            color: var(--text-main);
            background-color: var(--bg-color);
            margin: 0;
            padding: 0;
        }

        /* アプリ風のヘッダーナビゲーション */
        .app-bar {
            background-color: rgba(22, 27, 38, 0.8);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 100;
        }

        .app-logo {
            font-weight: bold;
            font-size: 1.2rem;
            letter-spacing: 2px;
            background: linear-gradient(45deg, var(--accent-purple), var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .app-badge {
            background: rgba(0, 242, 254, 0.1);
            border: 1px solid var(--accent-blue);
            color: var(--accent-blue);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            text-transform: uppercase;
        }

        /* メインビジュアル（ヒーローエリア） */
        .hero {
            text-align: center;
            padding: 80px 20px;
            background: radial-gradient(circle at top, #1e2640 0%, var(--bg-color) 70%);
        }

        .hero h1 {
            font-size: 2.8rem;
            margin: 0 0 20px 0;
            font-weight: 800;
            letter-spacing: -1px;
            background: linear-gradient(120deg, #fff 30%, var(--text-sub));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            color: var(--text-sub);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        /* コンテナ */
        .container {
            max-width: 900px;
            margin: 0 auto 80px auto;
            padding: 0 20px;
        }

        /* グリッドレイアウト（結果と考察などを並べる用） */
        .grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        @media (max-width: 768px) {
            .grid { grid-template-columns: 1fr; }
            .hero h1 { font-size: 2rem; }
        }

        /* アプリのカード型セクション */
        .card {
            background-color: var(--card-bg);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 16px;
            padding: 30px;
            margin-bottom: 24px;
            transition: transform 0.3s ease, border-color 0.3s ease;
        }

        .card:hover {
            transform: translateY(-2px);
            border-color: rgba(0, 242, 254, 0.3);
        }

        /* 近未来的な見出し */
        .card h2 {
            margin-top: 0;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            color: #fff;
        }

        .card h2::before {
            content: '';
            display: inline-block;
            width: 8px;
            height: 18px;
            background: linear-gradient(to bottom, var(--accent-purple), var(--accent-blue));
            margin-right: 12px;
            border-radius: 4px;
        }

        /* データの数値などを目立たせるパーツ */
        .data-status {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 8px;
            padding: 15px;
            margin: 15px 0;
            border-left: 4px solid var(--accent-purple);
        }

        /* リストスタイル */
        ul, ol {
            padding-left: 20px;
            color: var(--text-sub);
        }

        li { margin-bottom: 10px; }

        code {
            background: #242b3d;
            padding: 2px 6px;
            border-radius: 4px;
            color: var(--accent-blue);
            font-family: monospace;
        }

        /* フッター */
        footer {
            text-align: center;
            padding: 4px;
            color: var(--text-sub);
            font-size: 0.85rem;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            background-color: var(--card-bg);
        }
    </style>
</head>
<body>

    <div class="app-bar">
        <div class="app-logo">RESEARCH_DASHBOARD</div>
        <div class="app-badge">PROJECT v1.0</div>
    </div>

    <div class="hero">
        <h1>ここに研究のメインタイトルを入力</h1>
        <p>〇〇県立〇〇高等学校 科学部 / 課題研究第〇班</p>
    </div>

    <div class="container">

        <div class="card">
            <h2>OVERVIEW / 研究概要</h2>
            <p style="color: var(--text-sub);">ここに研究のざっくりとしたまとめを記述します。ダークモードの背景に鮮やかな青と紫のアクセントを効かせ、最先端のアプリケーションやダッシュボードのような洗練された雰囲気を演出しています。</p>
        </div>

        <div class="grid">
            <div class="card">
                <h2>01 / 背景と目的</h2>
                <p style="color: var(--text-sub);">なぜこの研究を始めようと思ったのか、自分たちの問題意識を書きましょう。</p>
                <div class="data-status">
                    <span style="color: #fff; font-weight: bold;">[MISSION]</span><br>
                    〇〇という課題に対し、〇〇を明らかにすることを目的とする。
                </div>
            </div>

            <div class="card">
                <h2>02 / 研究・実験方法</h2>
                <p style="color: var(--text-sub);">どのような手順で実験や調査を行ったかをステップ順に書きます。</p>
                <ol>
                    <li>サンプルの準備と抽出</li>
                    <li>装置の条件設定と計測</li>
                    <li>解析アルゴリズムの適用</li>
                </ol>
            </div>
        </div>

        <div class="card">
            <h2>03 / 結果と考察</h2>
            <p style="color: var(--text-sub);">実験や調査によって得られた事実（結果）と、そこから何が考えられるか（考察）を書きます。</p>
            <p style="color: var(--text-sub);">ここにグラフなどの画像（<code>&lt;img&gt;</code>タグ）を入れると、一気にデータダッシュボード感が強まってさらにカッコよくなります！</p>
        </div>

        <div class="card">
            <h2>04 / 結論と今後の展望</h2>
            <p style="color: var(--text-sub);">今回の研究で最終的に分かった結論をまとめます。さらに、今後の発展可能性についても触れておきましょう。洗練されたデザインは、説得力をより高めてくれます。</p>
        </div>

        <div class="card" style="margin-bottom: 0;">
            <h2>REFERENCES & ACKNOWLEDGMENTS</h2>
            <p style="font-size: 0.9rem; color: var(--text-sub);"><strong>参考文献：</strong></p>
            <ul style="font-size: 0.9rem;">
                <li>著者名『本・論文のタイトル』出版社（発行年）</li>
                <li>サイト名「ページのタイトル」URL（最終閲覧日）</li>
            </ul>
        </div>

    </div>

    <footer>
        <p>&copy; 2026 課題研究チーム名. Powered by HTML&CSS.</p>
    </footer>

</body>
</html>

