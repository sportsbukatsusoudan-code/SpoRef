<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>SpoRef - サッカー審判マッチング | 全国対応</title>
<meta name="description" content="サッカーの審判を全国どこでも手配できる審判専用マッチングサービス。登録は無料、依頼料は1名1,000円。主審8,000円・副審6,000円(交通費込み)。" />
<style>
  :root{
    --primary:#1e5fbf;
    --primary-dark:#163f80;
    --primary-light:#3b82f6;
    --accent:#22c55e;
    --bg:#f5f8fc;
    --card:#ffffff;
    --text:#1a2540;
    --text-sub:#5b6a85;
    --border:#e3e9f3;
    --shadow:0 4px 16px rgba(30,95,191,.08);
    --shadow-lg:0 12px 32px rgba(30,95,191,.14);
  }
  *{box-sizing:border-box;margin:0;padding:0}
  body{
    font-family:"Hiragino Sans","Yu Gothic UI","Meiryo",system-ui,sans-serif;
    background:var(--bg);color:var(--text);line-height:1.7;-webkit-font-smoothing:antialiased;
  }
  a{color:var(--primary);text-decoration:none}
  img{max-width:100%;display:block}

  /* Header */
  header{
    background:#fff;border-bottom:1px solid var(--border);
    position:sticky;top:0;z-index:100;
  }
  .nav{
    max-width:1200px;margin:0 auto;padding:14px 20px;
    display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:10px;
  }
  .logo{font-size:1.4rem;font-weight:800;color:var(--primary);display:flex;align-items:center;gap:8px}
  .logo-mark{
    width:34px;height:34px;border-radius:10px;
    background:linear-gradient(135deg,var(--primary),var(--primary-light));
    color:#fff;display:flex;align-items:center;justify-content:center;font-size:1.1rem;
  }
  .nav-links{display:flex;gap:22px;align-items:center;flex-wrap:wrap}
  .nav-links a{color:var(--text);font-weight:500;font-size:.95rem}
  .nav-links a:hover{color:var(--primary)}
  .btn{
    display:inline-block;padding:10px 22px;border-radius:8px;font-weight:600;
    cursor:pointer;border:none;font-size:.95rem;transition:.2s;text-align:center;
  }
  .btn-primary{background:var(--primary);color:#fff}
  .btn-primary:hover{background:var(--primary-dark);transform:translateY(-1px);box-shadow:var(--shadow)}
  .btn-outline{background:transparent;color:var(--primary);border:2px solid var(--primary)}
  .btn-outline:hover{background:var(--primary);color:#fff}

  /* Hero */
  .hero{
    background:linear-gradient(135deg,#1e5fbf 0%,#3b82f6 100%);
    color:#fff;padding:80px 20px 90px;position:relative;overflow:hidden;
  }
  .hero::before{
    content:"⚽";position:absolute;font-size:18rem;opacity:.06;
    right:-30px;top:50%;transform:translateY(-50%) rotate(-15deg);
  }
  .hero-inner{max-width:1100px;margin:0 auto;position:relative;z-index:1}
  .hero .tag{
    display:inline-block;background:rgba(255,255,255,.2);padding:6px 16px;
    border-radius:20px;font-size:.85rem;margin-bottom:18px;backdrop-filter:blur(6px);
  }
  .hero h1{font-size:2.6rem;line-height:1.3;margin-bottom:18px;font-weight:800}
  .hero h1 span{color:#fde047}
  .hero p{font-size:1.1rem;opacity:.95;margin-bottom:28px;max-width:680px}
  .hero-cta{display:flex;gap:14px;flex-wrap:wrap}
  .btn-white{background:#fff;color:var(--primary)}
  .btn-white:hover{background:#f1f5f9}
  .btn-ghost{background:rgba(255,255,255,.15);color:#fff;border:2px solid rgba(255,255,255,.5)}
  .btn-ghost:hover{background:rgba(255,255,255,.25)}

  /* Section */
  section{padding:70px 20px}
  .container{max-width:1100px;margin:0 auto}
  .section-title{text-align:center;margin-bottom:50px}
  .section-title h2{font-size:2rem;margin-bottom:10px;color:var(--text)}
  .section-title p{color:var(--text-sub)}

  /* Pricing */
  .price-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:22px;margin-bottom:30px}
  .price-card{
    background:var(--card);border-radius:14px;padding:30px 26px;
    box-shadow:var(--shadow);border:2px solid var(--border);transition:.3s;text-align:center;
  }
  .price-card:hover{transform:translateY(-4px);box-shadow:var(--shadow-lg);border-color:var(--primary-light)}
  .price-card.highlight{border-color:var(--primary);background:linear-gradient(180deg,#fff 0%,#f0f6ff 100%)}
  .price-icon{font-size:2.4rem;margin-bottom:12px}
  .price-card h3{font-size:1.15rem;margin-bottom:14px;color:var(--text)}
  .price-amount{font-size:2rem;font-weight:800;color:var(--primary);margin-bottom:6px}
  .price-amount small{font-size:.9rem;color:var(--text-sub);font-weight:400}
  .price-note{font-size:.85rem;color:var(--text-sub);margin-top:10px}
  .price-summary{
    background:#eff6ff;border-left:4px solid var(--primary);padding:18px 22px;
    border-radius:8px;font-size:.95rem;color:var(--text);
  }
  .price-summary strong{color:var(--primary)}

  /* Flow */
  .flow{background:#fff}
  .flow-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:22px}
  .flow-step{text-align:center;padding:24px 18px;border-radius:12px;background:var(--bg);position:relative}
  .flow-num{
    width:42px;height:42px;border-radius:50%;background:var(--primary);color:#fff;
    display:flex;align-items:center;justify-content:center;font-weight:700;
    margin:0 auto 12px;font-size:1.1rem;
  }
  .flow-step h4{margin-bottom:8px;font-size:1.05rem}
  .flow-step p{font-size:.9rem;color:var(--text-sub)}

  /* Forms */
  .form-section{background:#fff}
  .tabs{
    display:flex;gap:8px;margin-bottom:30px;justify-content:center;flex-wrap:wrap;
  }
  .tab{
    padding:12px 28px;border:2px solid var(--border);background:#fff;border-radius:10px;
    cursor:pointer;font-weight:600;color:var(--text-sub);transition:.2s;
  }
  .tab.active{background:var(--primary);color:#fff;border-color:var(--primary)}
  .form-card{
    background:var(--card);border-radius:14px;padding:36px;
    box-shadow:var(--shadow);border:1px solid var(--border);max-width:780px;margin:0 auto;
  }
  .form-card h3{margin-bottom:8px;color:var(--primary);font-size:1.3rem}
  .form-card .lead{color:var(--text-sub);margin-bottom:24px;font-size:.95rem}
  .form-grid{display:grid;grid-template-columns:1fr 1fr;gap:18px}
  .form-grid .full{grid-column:1/-1}
  .field label{display:block;font-weight:600;font-size:.9rem;margin-bottom:6px;color:var(--text)}
  .field label .req{color:#dc2626;margin-left:3px}
  .field input,.field select,.field textarea{
    width:100%;padding:11px 14px;border:1.5px solid var(--border);border-radius:8px;
    font-size:.95rem;font-family:inherit;transition:.2s;background:#fff;
  }
  .field input:focus,.field select:focus,.field textarea:focus{
    outline:none;border-color:var(--primary);box-shadow:0 0 0 3px rgba(30,95,191,.12);
  }
  .field textarea{resize:vertical;min-height:90px}
  .check-group{display:flex;flex-wrap:wrap;gap:10px;margin-top:6px}
  .check-group label{
    display:inline-flex;align-items:center;gap:6px;padding:8px 14px;
    border:1.5px solid var(--border);border-radius:20px;cursor:pointer;
    font-size:.88rem;font-weight:500;background:#fff;transition:.2s;
  }
  .check-group label:hover{border-color:var(--primary)}
  .check-group input{display:none}
  .check-group input:checked + span{color:var(--primary)}
  .check-group label:has(input:checked){background:#eff6ff;border-color:var(--primary)}
  .form-submit{margin-top:24px;text-align:center}
  .form-submit .btn{padding:14px 50px;font-size:1rem}
  .agree{font-size:.85rem;color:var(--text-sub);margin-top:14px}

  .form-panel{display:none}
  .form-panel.active{display:block}

  .price-table{
    background:#f0f6ff;border-radius:10px;padding:20px;margin-bottom:24px;
    border:1px solid var(--border);
  }
  .price-table h4{color:var(--primary);margin-bottom:10px;font-size:1rem}
  .price-table ul{list-style:none}
  .price-table li{
    padding:6px 0;font-size:.92rem;border-bottom:1px dashed var(--border);
    display:flex;justify-content:space-between;
  }
  .price-table li:last-child{border:none}
  .price-table li strong{color:var(--primary)}

  /* FAQ */
  .faq{background:var(--bg)}
  .faq-list{max-width:800px;margin:0 auto}
  .faq-item{
    background:#fff;border-radius:10px;margin-bottom:12px;
    box-shadow:var(--shadow);overflow:hidden;
  }
  .faq-q{
    padding:18px 22px;font-weight:600;cursor:pointer;
    display:flex;justify-content:space-between;align-items:center;color:var(--text);
  }
  .faq-q::after{content:"+";color:var(--primary);font-size:1.4rem;font-weight:300;transition:.2s}
  .faq-item.open .faq-q::after{transform:rotate(45deg)}
  .faq-a{
    padding:0 22px;max-height:0;overflow:hidden;transition:.3s;
    color:var(--text-sub);font-size:.94rem;
  }
  .faq-item.open .faq-a{max-height:300px;padding:0 22px 18px}

  /* Footer */
  footer{background:#163f80;color:#cbd5e1;padding:40px 20px 24px;text-align:center}
  footer .links{margin-bottom:16px}
  footer .links a{color:#cbd5e1;margin:0 12px;font-size:.9rem}
  footer .links a:hover{color:#fff}
  footer .small{font-size:.82rem;opacity:.7}
  footer .related{
    background:rgba(255,255,255,.06);border-radius:10px;padding:14px 18px;
    margin:0 auto 22px;max-width:600px;font-size:.9rem;
  }
  footer .related a{color:#fde047;font-weight:600}

  /* Responsive */
  @media(max-width:720px){
    .hero{padding:50px 20px 60px}
    .hero h1{font-size:1.8rem}
    .hero p{font-size:1rem}
    .form-grid{grid-template-columns:1fr}
    .form-card{padding:24px 20px}
    section{padding:50px 16px}
    .section-title h2{font-size:1.55rem}
    .nav-links{gap:12px;font-size:.85rem}
    .nav-links a:not(.btn){display:none}
  }
</style>
</head>
<body>

<header>
  <div class="nav">
    <div class="logo">
      <div class="logo-mark">⚽</div>
      <span>SpoRef</span>
    </div>
    <div class="nav-links">
      <a href="#about">サービス</a>
      <a href="#price">料金</a>
      <a href="#flow">ご利用の流れ</a>
      <a href="#register">審判登録</a>
      <a href="#request">依頼する</a>
      <a href="#faq">FAQ</a>
      <a href="#register" class="btn btn-primary">無料で審判登録</a>
    </div>
  </div>
</header>

<!-- Hero -->
<section class="hero">
  <div class="hero-inner">
    <span class="tag">⚽ 全国47都道府県対応 / サッカー審判専用</span>
    <h1>サッカーの審判を、<br><span>全国どこでも</span>手配できる。</h1>
    <p>練習試合・大会・リーグ戦の審判確保にお困りの方へ。<br>
       資格を持つ審判員と主催者をシンプルにつなぐ、サッカー審判専用マッチングサービスです。<br>
       <strong>審判登録は完全無料。</strong> 依頼者は1名あたり1,000円のマッチング料のみ。</p>
    <div class="hero-cta">
      <a href="#register" class="btn btn-white">審判として登録する(無料)</a>
      <a href="#request" class="btn btn-ghost">審判を依頼する</a>
    </div>
  </div>
</section>

<!-- About / Pricing -->
<section id="price">
  <div class="container">
    <div class="section-title">
      <h2>シンプルでわかりやすい料金体系</h2>
      <p>審判は登録無料。依頼者は必要な分だけ、明朗会計でご利用いただけます。</p>
    </div>

    <div class="price-grid">
      <div class="price-card">
        <div class="price-icon">📝</div>
        <h3>審判登録料</h3>
        <div class="price-amount">無料 <small>/ 永年</small></div>
        <div class="price-note">登録費・年会費・月額費用は一切かかりません</div>
      </div>
      <div class="price-card highlight">
        <div class="price-icon">🤝</div>
        <h3>マッチング料(依頼者)</h3>
        <div class="price-amount">¥1,000 <small>/ 審判1名</small></div>
        <div class="price-note">サイト経由でお支払いいただく利用料です</div>
      </div>
      <div class="price-card">
        <div class="price-icon">🟨</div>
        <h3>主審 報酬</h3>
        <div class="price-amount">¥8,000 <small>/ 1試合</small></div>
        <div class="price-note">交通費込み・現地で直接お支払い</div>
      </div>
      <div class="price-card">
        <div class="price-icon">🚩</div>
        <h3>副審 報酬</h3>
        <div class="price-amount">¥6,000 <small>/ 1試合</small></div>
        <div class="price-note">交通費込み・現地で直接お支払い</div>
      </div>
    </div>

    <div class="price-summary">
      💡 <strong>たとえば：</strong> 主審1名・副審2名(合計3名)を依頼する場合<br>
      ・サイトへのお支払い：1,000円 × 3名 ＝ <strong>3,000円</strong>(事前決済)<br>
      ・現地でのお支払い：主審 8,000円 ＋ 副審 6,000円 × 2名 ＝ <strong>20,000円</strong>(当日現金)<br>
      ※ 報酬には<strong>交通費が含まれます</strong>。別途交通費の請求は発生しません。
    </div>
  </div>
</section>

<!-- Flow -->
<section id="flow" class="flow">
  <div class="container">
    <div class="section-title">
      <h2>ご利用の流れ</h2>
      <p>シンプルな4ステップで、審判の手配が完結します。</p>
    </div>
    <div class="flow-grid">
      <div class="flow-step">
        <div class="flow-num">1</div>
        <h4>依頼内容を入力</h4>
        <p>日時・会場・必要人数・カテゴリーをフォームから送信</p>
      </div>
      <div class="flow-step">
        <div class="flow-num">2</div>
        <h4>審判をマッチング</h4>
        <p>運営から登録審判員へ案内し、対応可能な方をご紹介</p>
      </div>
      <div class="flow-step">
        <div class="flow-num">3</div>
        <h4>マッチング料を決済</h4>
        <p>1名1,000円のマッチング料をオンライン決済</p>
      </div>
      <div class="flow-step">
        <div class="flow-num">4</div>
        <h4>当日試合・報酬支払</h4>
        <p>会場で審判を実施。報酬は現地で直接お支払い</p>
      </div>
    </div>
  </div>
</section>

<!-- Forms -->
<section id="register" class="form-section">
  <div class="container">
    <div class="section-title">
      <h2>登録・依頼フォーム</h2>
      <p>下のタブを切り替えて、目的のフォームをご利用ください。</p>
    </div>

    <div class="tabs">
      <div class="tab active" data-tab="ref">⚽ 審判として登録(無料)</div>
      <div class="tab" data-tab="req">📋 審判を依頼する</div>
    </div>

    <!-- 審判登録 -->
    <div class="form-panel active" id="panel-ref">
      <div class="form-card">
        <h3>サッカー審判 登録フォーム</h3>
        <p class="lead">登録は完全無料です。試合のご紹介を希望される方は以下にご記入ください。資格証明書はマッチング前に別途確認させていただきます。</p>

        <form onsubmit="handleSubmit(event,'審判登録')">
          <div class="form-grid">
            <div class="field">
              <label>氏名 <span class="req">*</span></label>
              <input type="text" name="name" required />
            </div>
            <div class="field">
              <label>ふりがな <span class="req">*</span></label>
              <input type="text" name="kana" required />
            </div>
            <div class="field">
              <label>メールアドレス <span class="req">*</span></label>
              <input type="email" name="email" required />
            </div>
            <div class="field">
              <label>電話番号 <span class="req">*</span></label>
              <input type="tel" name="tel" required />
            </div>
            <div class="field">
              <label>生年月日</label>
              <input type="date" name="birthday" />
            </div>
            <div class="field">
              <label>居住都道府県 <span class="req">*</span></label>
              <select name="prefecture" required id="ref-pref">
                <option value="">選択してください</option>
              </select>
            </div>
            <div class="field full">
              <label>市区町村</label>
              <input type="text" name="city" placeholder="例：仙台市青葉区" />
            </div>
            <div class="field full">
              <label>JFA審判資格 <span class="req">*</span></label>
              <select name="grade" required>
                <option value="">選択してください</option>
                <option>1級審判員</option>
                <option>女子1級審判員</option>
                <option>2級審判員</option>
                <option>3級審判員</option>
                <option>4級審判員</option>
                <option>U-15/U-12 4級</option>
                <option>フットサル1級</option>
                <option>フットサル2級</option>
                <option>フットサル3級</option>
                <option>フットサル4級</option>
                <option>資格はないが経験あり(要相談)</option>
              </select>
            </div>
            <div class="field">
              <label>審判経験年数</label>
              <input type="number" name="years" min="0" max="60" />
            </div>
            <div class="field">
              <label>審判登録番号</label>
              <input type="text" name="refnum" placeholder="任意" />
            </div>
            <div class="field full">
              <label>対応可能な役割 <span class="req">*</span></label>
              <div class="check-group">
                <label><input type="checkbox" name="role" value="主審"><span>主審</span></label>
                <label><input type="checkbox" name="role" value="副審"><span>副審</span></label>
                <label><input type="checkbox" name="role" value="第4の審判員"><span>第4の審判員</span></label>
              </div>
            </div>
            <div class="field full">
              <label>対応可能なカテゴリー <span class="req">*</span></label>
              <div class="check-group">
                <label><input type="checkbox" name="cat" value="U-12"><span>U-12(少年)</span></label>
                <label><input type="checkbox" name="cat" value="U-15"><span>U-15(中学生)</span></label>
                <label><input type="checkbox" name="cat" value="U-18"><span>U-18(高校生)</span></label>
                <label><input type="checkbox" name="cat" value="一般男子"><span>一般男子</span></label>
                <label><input type="checkbox" name="cat" value="一般女子"><span>一般女子</span></label>
                <label><input type="checkbox" name="cat" value="シニア"><span>シニア</span></label>
                <label><input type="checkbox" name="cat" value="フットサル"><span>フットサル</span></label>
              </div>
            </div>
            <div class="field full">
              <label>対応可能な活動範囲(複数選択可)</label>
              <div class="check-group">
                <label><input type="checkbox" name="area" value="居住県内のみ"><span>居住県内のみ</span></label>
                <label><input type="checkbox" name="area" value="近隣県も可"><span>近隣県も可</span></label>
                <label><input type="checkbox" name="area" value="全国対応可"><span>全国対応可</span></label>
              </div>
            </div>
            <div class="field full">
              <label>自己PR・実績</label>
              <textarea name="pr" placeholder="主な担当試合、所属協会、得意なカテゴリーなど"></textarea>
            </div>
          </div>

          <div class="form-submit">
            <button type="submit" class="btn btn-primary">この内容で登録する(無料)</button>
            <p class="agree">※ 送信前に <a href="#privacy">プライバシーポリシー</a> をご確認ください。本フォームは現在ベータ版のため、実際の送信処理はメールでの確認となります。</p>
          </div>
        </form>
      </div>
    </div>

    <!-- 依頼フォーム -->
    <div class="form-panel" id="panel-req">
      <div class="form-card">
        <h3>サッカー審判 依頼フォーム</h3>
        <p class="lead">下記内容で審判をお探しします。マッチング成立後、1名あたり1,000円のマッチング料をオンライン決済いただきます。</p>

        <div class="price-table">
          <h4>💰 料金のご案内</h4>
          <ul>
            <li><span>マッチング料(サイトへ事前決済)</span><strong>¥1,000 / 1名</strong></li>
            <li><span>主審 報酬(現地払い・交通費込)</span><strong>¥8,000 / 試合</strong></li>
            <li><span>副審 報酬(現地払い・交通費込)</span><strong>¥6,000 / 試合</strong></li>
          </ul>
        </div>

        <form onsubmit="handleSubmit(event,'審判依頼')">
          <div class="form-grid">
            <div class="field">
              <label>ご担当者氏名 <span class="req">*</span></label>
              <input type="text" name="name" required />
            </div>
            <div class="field">
              <label>団体・チーム名</label>
              <input type="text" name="org" />
            </div>
            <div class="field">
              <label>メールアドレス <span class="req">*</span></label>
              <input type="email" name="email" required />
            </div>
            <div class="field">
              <label>電話番号 <span class="req">*</span></label>
              <input type="tel" name="tel" required />
            </div>
            <div class="field">
              <label>試合日 <span class="req">*</span></label>
              <input type="date" name="matchdate" required />
            </div>
            <div class="field">
              <label>試合開始時刻 <span class="req">*</span></label>
              <input type="time" name="matchtime" required />
            </div>
            <div class="field">
              <label>都道府県 <span class="req">*</span></label>
              <select name="prefecture" required id="req-pref">
                <option value="">選択してください</option>
              </select>
            </div>
            <div class="field">
              <label>市区町村 <span class="req">*</span></label>
              <input type="text" name="city" required />
            </div>
            <div class="field full">
              <label>会場名・住所 <span class="req">*</span></label>
              <input type="text" name="venue" placeholder="例：〇〇総合運動公園 サッカー場" required />
            </div>
            <div class="field">
              <label>カテゴリー <span class="req">*</span></label>
              <select name="category" required>
                <option value="">選択してください</option>
                <option>U-12(少年)</option>
                <option>U-15(中学生)</option>
                <option>U-18(高校生)</option>
                <option>一般男子</option>
                <option>一般女子</option>
                <option>シニア</option>
                <option>フットサル</option>
                <option>その他</option>
              </select>
            </div>
            <div class="field">
              <label>試合形式</label>
              <select name="format">
                <option>11人制</option>
                <option>8人制</option>
                <option>5人制(フットサル)</option>
                <option>その他</option>
              </select>
            </div>
            <div class="field">
              <label>主審 必要人数</label>
              <input type="number" name="ref_main" min="0" max="10" value="1" />
            </div>
            <div class="field">
              <label>副審 必要人数</label>
              <input type="number" name="ref_sub" min="0" max="10" value="2" />
            </div>
            <div class="field">
              <label>試合数(連続して何試合あるか)</label>
              <input type="number" name="games" min="1" max="20" value="1" />
            </div>
            <div class="field">
              <label>希望する資格等級</label>
              <select name="grade">
                <option>不問</option>
                <option>4級以上</option>
                <option>3級以上</option>
                <option>2級以上</option>
                <option>1級</option>
              </select>
            </div>
            <div class="field full">
              <label>大会・試合内容の補足</label>
              <textarea name="note" placeholder="例：練習試合、〇〇カップ予選、リーグ戦◯節 など"></textarea>
            </div>
          </div>

          <div class="form-submit">
            <button type="submit" class="btn btn-primary">この内容で依頼を送信する</button>
            <p class="agree">※ 送信後、運営からマッチング状況とお支払い手続きについてご連絡します。マッチング不成立の場合、料金は発生しません。</p>
          </div>
        </form>
      </div>
    </div>
  </div>
</section>

<!-- FAQ -->
<section id="faq" class="faq">
  <div class="container">
    <div class="section-title">
      <h2>よくあるご質問</h2>
    </div>
    <div class="faq-list">
      <div class="faq-item">
        <div class="faq-q">審判登録に費用はかかりますか？</div>
        <div class="faq-a">いいえ、審判の登録・利用は完全無料です。年会費・月額費用も一切いただきません。報酬は試合ごとに現地で直接お受け取りいただきます。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">交通費は別途請求できますか？</div>
        <div class="faq-a">いいえ、主審 8,000円・副審 6,000円の報酬には交通費が含まれます。別途の交通費請求はできかねますので、活動可能エリアを登録時にご指定ください。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">マッチング料 1,000円はいつ支払いますか？</div>
        <div class="faq-a">担当審判が確定した時点で、オンライン決済のご案内をお送りします。決済完了後に審判員の連絡先・詳細をお伝えします。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">マッチングが成立しなかった場合は？</div>
        <div class="faq-a">対応可能な審判が見つからなかった場合は料金は発生しません。一定期間内にご連絡できなかった場合は、その旨ご報告いたします。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">資格を持っていなくても登録できますか？</div>
        <div class="faq-a">JFA審判資格(4級以上)の保有を推奨していますが、経験豊富な方は「要相談」枠で登録いただけます。マッチング前に運営より状況を確認させていただきます。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">キャンセルした場合はどうなりますか？</div>
        <div class="faq-a">試合4日前までのキャンセルはマッチング料を全額返金します(決済手数料を除く)。3日前〜前日は50%、当日キャンセルは返金不可となります。天候不良等の場合はご相談ください。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">対応エリアはどこまでですか？</div>
        <div class="faq-a">全国47都道府県すべてに対応していますが、エリアによっては登録審判員が少なく、マッチングまでお時間をいただく場合があります。お早めのご依頼をお勧めします。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q">SpoMatch との違いは？</div>
        <div class="faq-a">本サイト SpoRef は「サッカー審判」に特化したシンプルなマッチングサービスです。指導者・トレーナーをお探しの場合は、姉妹サイト <a href="https://sportsbukatsusoudan-code.github.io/SpoMatch/" target="_blank">SpoMatch</a> をご利用ください。</div>
      </div>
    </div>
  </div>
</section>

<!-- Footer -->
<footer>
  <div class="related">
    指導者・トレーナーをお探しの方は、姉妹サイト
    <a href="https://sportsbukatsusoudan-code.github.io/SpoMatch/" target="_blank">SpoMatch</a> をご利用ください。
  </div>
  <div class="links">
    <a href="#price">料金</a>
    <a href="#flow">ご利用の流れ</a>
    <a href="#register">審判登録</a>
    <a href="#request">依頼する</a>
    <a href="#faq">FAQ</a>
    <a href="#privacy">プライバシーポリシー</a>
    <a href="#tos">利用規約</a>
  </div>
  <div class="small">
    © SpoRef - サッカー審判マッチング. All rights reserved.<br>
    運営：スポーツ・部活相談サポート
  </div>
</footer>

<script>
  // 47都道府県
  const PREFECTURES = [
    "北海道","青森県","岩手県","宮城県","秋田県","山形県","福島県",
    "茨城県","栃木県","群馬県","埼玉県","千葉県","東京都","神奈川県",
    "新潟県","富山県","石川県","福井県","山梨県","長野県",
    "岐阜県","静岡県","愛知県","三重県",
    "滋賀県","京都府","大阪府","兵庫県","奈良県","和歌山県",
    "鳥取県","島根県","岡山県","広島県","山口県",
    "徳島県","香川県","愛媛県","高知県",
    "福岡県","佐賀県","長崎県","熊本県","大分県","宮崎県","鹿児島県","沖縄県"
  ];

  function fillPref(id){
    const sel = document.getElementById(id);
    PREFECTURES.forEach(p=>{
      const o = document.createElement("option");
      o.value = p; o.textContent = p;
      sel.appendChild(o);
    });
  }
  fillPref("ref-pref");
  fillPref("req-pref");

  // タブ切替
  document.querySelectorAll(".tab").forEach(t=>{
    t.addEventListener("click",()=>{
      document.querySelectorAll(".tab").forEach(x=>x.classList.remove("active"));
      document.querySelectorAll(".form-panel").forEach(x=>x.classList.remove("active"));
      t.classList.add("active");
      document.getElementById("panel-"+t.dataset.tab).classList.add("active");
    });
  });

  // 「依頼する」リンクで自動的に依頼タブへ
  document.querySelectorAll('a[href="#request"]').forEach(a=>{
    a.addEventListener("click",()=>{
      document.querySelector('.tab[data-tab="req"]').click();
    });
  });

  // FAQ開閉
  document.querySelectorAll(".faq-q").forEach(q=>{
    q.addEventListener("click",()=>q.parentElement.classList.toggle("open"));
  });

  // フォーム送信(仮)
  function handleSubmit(e,type){
    e.preventDefault();
    alert(`【${type}】を受け付けました。\n\n※ 現在はベータ版のため、運営より改めてご連絡いたします。\n(本番運用時には Google Forms / Formspree / Netlify Forms 等の連携をご利用ください)`);
    e.target.reset();
  }
</script>

</body>
</html>
