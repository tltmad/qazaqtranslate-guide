# qazaqtranslate-guide
Educational website-guide on using Google Translate and ChatGPT for Kazakh language translation.  Created as a practical product for an academic research project.
<!doctype html>
<html lang="kk">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>QazaqTranslate Guide</title>
  <meta name="description" content="Қазақ тіліне автоматты аударманы (Google Translate, ChatGPT) дұрыс қолдануға арналған практикалық нұсқаулық."/>
  <style>
    :root{
      --bg:#0b1220;
      --card:#111a2e;
      --card2:#0f1730;
      --text:#e9eefc;
      --muted:#b9c3e6;
      --accent:#4da3ff;
      --accent2:#6ee7b7;
      --line:rgba(255,255,255,.10);
      --shadow:0 14px 35px rgba(0,0,0,.35);
      --radius:18px;
      --max:1100px;
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family:system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;
      background:
        radial-gradient(1100px 600px at 20% 0%, rgba(77,163,255,.25), transparent 60%),
        radial-gradient(900px 520px at 90% 10%, rgba(110,231,183,.18), transparent 55%),
        var(--bg);
      color:var(--text);
      line-height:1.55;
    }
    a{color:inherit;text-decoration:none}
    .wrap{max-width:var(--max);margin:0 auto;padding:22px}
    /* Top bar */
    .nav{
      position:sticky; top:0; z-index:99;
      background:rgba(11,18,32,.65);
      backdrop-filter: blur(10px);
      border-bottom:1px solid var(--line);
    }
    .nav .wrap{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;align-items:center;gap:10px;font-weight:800;letter-spacing:.3px}
    .dot{width:10px;height:10px;border-radius:50%;
      background:linear-gradient(135deg,var(--accent),var(--accent2))}
    .menu{display:flex;flex-wrap:wrap;gap:8px}
    .menu a{
      font-size:13px;color:var(--muted);
      padding:8px 10px;border-radius:12px;border:1px solid transparent;
    }
    .menu a:hover{border-color:var(--line);color:var(--text)}
    /* Hero */
    header{padding:26px 0 10px}
    .grid{display:grid;gap:16px;grid-template-columns:1.25fr .75fr}
    @media(max-width:920px){.grid{grid-template-columns:1fr}}
    h1{font-size:38px; margin:0 0 10px}
    .lead{color:var(--muted);margin:0 0 16px;max-width:70ch}
    .pillrow{display:flex;flex-wrap:wrap;gap:10px;margin:12px 0 0}
    .pill{
      font-size:12.5px;color:var(--muted);
      border:1px solid var(--line);
      background:rgba(255,255,255,.03);
      padding:8px 12px;border-radius:999px;
    }
    .card{
      background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      border:1px solid var(--line);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
      padding:18px;
    }
    .tag{
      display:inline-block;font-size:12px;font-weight:800;
      padding:6px 10px;border-radius:999px;
      color:#081120;
      background:linear-gradient(135deg,var(--accent),var(--accent2));
    }
    .kpi{display:grid;gap:12px;grid-template-columns:repeat(3,1fr);margin-top:14px}
    @media(max-width:700px){.kpi{grid-template-columns:1fr}}
    .box{border:1px solid var(--line);border-radius:16px;padding:12px;background:rgba(255,255,255,.02)}
    .num{font-size:22px;font-weight:900}
    .small{font-size:13px;color:var(--muted)}
    /* Sections */
    section{padding:18px 0}
    .section-title{display:flex;justify-content:space-between;gap:12px;align-items:flex-end;margin:0 0 10px}
    .section-title h2{margin:0;font-size:22px}
    .hint{color:var(--muted);font-size:13px}
    .two{display:grid;grid-template-columns:1fr 1fr;gap:16px}
    @media(max-width:920px){.two{grid-template-columns:1fr}}
    ul{margin:10px 0 0 18px;color:var(--muted)}
    li{margin:7px 0}
    /* Tool cards */
    .toolgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
    @media(max-width:920px){.toolgrid{grid-template-columns:1fr}}
    .tool h3{margin:10px 0 6px}
    .badge{display:inline-flex;align-items:center;gap:8px;font-size:12px;color:var(--muted)}
    .badge i{display:inline-block;width:8px;height:8px;border-radius:50%;background:var(--accent)}
    /* Selector */
    .selector{display:grid;grid-template-columns:1fr 1fr;gap:16px}
    @media(max-width:920px){.selector{grid-template-columns:1fr}}
    .field{margin:10px 0}
    label{display:block;font-size:13px;color:var(--muted);margin:0 0 6px}
    select, input[type="checkbox"], input[type="radio"], textarea{
      font:inherit;
    }
    select, textarea{
      width:100%;
      background:rgba(255,255,255,.03);
      border:1px solid var(--line);
      color:var(--text);
      padding:10px 12px;
      border-radius:14px;
      outline:none;
    }
    textarea{min-height:92px;resize:vertical}
    .row{display:flex;gap:12px;flex-wrap:wrap;align-items:center}
    .chip{
      display:inline-flex;align-items:center;gap:8px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.02);
      padding:8px 10px;border-radius:999px;
      color:var(--muted);
      font-size:13px;
    }
    .btnrow{display:flex;gap:10px;flex-wrap:wrap;margin-top:12px}
    .btn{
      cursor:pointer;
      display:inline-flex;align-items:center;justify-content:center;gap:8px;
      padding:10px 14px;border-radius:14px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.03);
      color:var(--text);
      font-size:14px;
    }
    .btn:hover{border-color:rgba(255,255,255,.20)}
    .btn.primary{
      border-color:transparent;
      background:linear-gradient(135deg,var(--accent),var(--accent2));
      color:#081120;
      font-weight:800;
    }
    .result{
      border:1px solid var(--line);
      border-radius:16px;
      padding:14px;
      background:rgba(255,255,255,.02);
    }
    .result h3{margin:0 0 8px}
    .mono{
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace;
      font-size:13px;
      white-space:pre-wrap;
      background:rgba(0,0,0,.25);
      border:1px solid rgba(255,255,255,.08);
      padding:12px;
      border-radius:14px;
    }
    .ok{color:var(--accent2)}
    .warn{color:#ffcc66}
    .danger{color:#ff7b7b}
    /* Footer */
    footer{padding:28px 0 40px;border-top:1px solid var(--line);margin-top:8px}
    .footgrid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
    @media(max-width:920px){.footgrid{grid-template-columns:1fr}}
    .mini{font-size:12px;color:var(--muted)}
  </style>
</head>

<body>
  <div class="nav">
    <div class="wrap">
      <div class="brand"><span class="dot"></span> QazaqTranslate Guide</div>
      <div class="menu">
        <a href="#tools">Құралдар</a>
        <a href="#choose">Қалай таңдау</a>
        <a href="#prompts">Prompt</a>
        <a href="#check">Тексеру</a>
        <a href="#survey">Сауалнама</a>
      </div>
    </div>
  </div>

  <div class="wrap">
    <header>
      <div class="grid">
        <div>
          <h1>Қазақ тіліне автоматты аударманы дұрыс қолдану</h1>
          <p class="lead">
            Бұл сайт Google Translate және ChatGPT арқылы қазақ тіліне аударғанда дұрыс құралды таңдауға,
            қателерді азайтуға және нәтижені тексеруге арналған. Ішінде шағын “таңдау көмекшісі” бар —
            мақсатыңа қарай қай құрал тиімді екенін көрсетеді.
          </p>
          <div class="pillrow">
            <span class="pill">Негізі: теория + сауалнама (33 респондент)</span>
            <span class="pill">Фокус: қазақ тіліндегі қате түрлері</span>
            <span class="pill">Практика: чек-лист + prompt үлгілері</span>
          </div>

          <div class="kpi">
            <div class="box">
              <div class="num">60,6%</div>
              <div class="small">аудармашыларды жиі қолданады</div>
            </div>
            <div class="box">
              <div class="num">69,7%</div>
              <div class="small">қателерді жиі байқайды</div>
            </div>
            <div class="box">
              <div class="num">54,5%</div>
              <div class="small">ең тиімді құрал: Google Translate</div>
            </div>
          </div>
        </div>

        <div class="card">
          <span class="tag">Неге маңызды?</span>
          <h3 style="margin:12px 0 8px">Қысқаша түсінік</h3>
          <p class="small">
            Қазақ тілі агглютинативті болғандықтан, жалғау-жұрнақ, сөз тәртібі, тұрақты тіркес сияқты
            факторлар автоматты аудармада қате тудыруы мүмкін. Сондықтан “аудару” ғана емес, тексеру және
            постредактирование қажет.
          </p>
          <div class="btnrow">
            <a class="btn primary" href="#choose">Таңдау көмекшісін ашу</a>
            <a class="btn" href="#check">Чек-лист</a>
          </div>
        </div>
      </div>
    </header>

    <!-- Tools -->
    <section id="tools">
      <div class="section-title">
        <h2>Негізгі құралдар</h2>
        <div class="hint">қай кезде қайсысы тиімді</div>
      </div>

      <div class="toolgrid">
        <div class="card tool">
          <div class="badge"><i></i> Жылдам & қарапайым</div>
          <h3>Google Translate</h3>
          <p class="small">
            Қысқа мәтін, тұрмыстық сөйлем, жалпы ақпаратқа ыңғайлы. Жылдам нәтиже береді.
          </p>
          <ul>
            <li><b>Артықшылығы:</b> өте жылдам, қолжетімді.</li>
            <li><b>Шектеуі:</b> күрделі стиль/термин/қосымшада қате болуы мүмкін.</li>
            <li><b>Үздік жағдай:</b> бастапқы нұсқа алу.</li>
          </ul>
        </div>

        <div class="card tool">
          <div class="badge"><i style="background:var(--accent2)"></i> Контекст & стиль</div>
          <h3>ChatGPT</h3>
          <p class="small">
            Мәтінді табиғи етіп қайта құра алады, стильді сақтауға көмектеседі.
          </p>
          <ul>
            <li><b>Артықшылығы:</b> түсіндіреді, бірнеше нұсқа береді.</li>
            <li><b>Шектеуі:</b> кейде “еркін” өзгертіп жіберуі мүмкін.</li>
            <li><b>Үздік жағдай:</b> ұзақ мәтін, стиль, түсіндіру.</li>
          </ul>
        </div>

        <div class="card tool">
          <div class="badge"><i style="background:#ffcc66"></i> Альтернатива</div>
          <h3>Yandex Translate / басқа</h3>
          <p class="small">
            Кей жағдайда пайдалы, бірақ қазақ тілінде нәтиже тұрақсыз болуы мүмкін.
          </p>
          <ul>
            <li><b>Артықшылығы:</b> кейбір сөздерге балама табуы мүмкін.</li>
            <li><b>Шектеуі:</b> сапа әртүрлі, бірізділік әлсіз болуы ықтимал.</li>
            <li><b>Үздік жағдай:</b> салыстыру үшін қосымша нұсқа.</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- Choose helper -->
    <section id="choose">
      <div class="section-title">
        <h2>Қай құралды таңдау керек?</h2>
        <div class="hint">шағын көмекші (таңда + ұсыныс ал)</div>
      </div>

      <div class="selector">
        <div class="card">
          <span class="tag">Таңдау</span>

          <div class="field">
            <label for="goal">1) Негізгі мақсатың қандай?</label>
            <select id="goal">
              <option value="study">Оқу (тапсырма, мәтін түсіну)</option>
              <option value="work">Жұмыс (ресми хат, құжат)</option>
              <option value="chat">Күнделікті қарым-қатынас</option>
              <option value="web">Интернет мәтіндері / жаңалық</option>
            </select>
          </div>

          <div class="field">
            <label for="textType">2) Мәтін түрі қандай?</label>
            <select id="textType">
              <option value="short">Қысқа (1–3 сөйлем)</option>
              <option value="medium">Орташа (1–2 абзац)</option>
              <option value="long">Ұзақ (бірнеше абзац)</option>
              <option value="terms">Термин көп (ғылыми/ресми)</option>
            </select>
          </div>

          <div class="field">
            <label>3) Сен үшін не маңызды?</label>
            <div class="row">
              <span class="chip"><input type="radio" name="priority" value="speed" checked> Жылдамдық</span>
              <span class="chip"><input type="radio" name="priority" value="quality"> Табиғилық/сапа</span>
              <span class="chip"><input type="radio" name="priority" value="accuracy"> Дәлдік/термин</span>
            </div>
          </div>

          <div class="field">
            <label>4) Нәтижені тексересің бе?</label>
            <div class="row">
              <span class="chip"><input type="checkbox" id="checklist"> Иә, чек-листпен тексеремін</span>
              <span class="chip"><input type="checkbox" id="doubleCheck"> Екі құралмен салыстырамын</span>
            </div>
          </div>

          <div class="btnrow">
            <button class="btn primary" id="btnSuggest">Ұсыныс беру</button>
            <button class="btn" id="btnReset" type="button">Тазалау</button>
          </div>

          <p class="small" style="margin:12px 0 0">
            Кеңес: егер мақсат “ресми/термин көп” болса, бір ғана құралға сенбей,
            міндетті түрде салыстыру және тексеру жасаған дұрыс.
          </p>
        </div>

        <div class="card">
          <span class="tag">Нәтиже</span>
          <div class="result" id="resultBox" aria-live="polite">
            <h3 style="margin:0 0 8px">Ұсыныс осында шығады</h3>
            <p class="small" style="margin:0">
              Сол жақтан параметрлерді таңда да, <b>“Ұсыныс беру”</b> батырмасын бас.
            </p>
          </div>

          <div style="height:12px"></div>

          <div class="result">
            <h3 style="margin:0 0 8px">Дайын prompt</h3>
            <p class="small" style="margin:0 0 10px">
              Егер ChatGPT ұсынса, төмендегі prompt-ты көшіріп қолдан.
            </p>
            <div class="mono" id="promptBox">Мұнда prompt пайда болады…</div>
            <div class="btnrow">
              <button class="btn" id="btnCopyPrompt" type="button">Prompt көшіру</button>
            </div>
            <div class="small" id="copyMsg" style="margin-top:8px"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Prompts -->
    <section id="prompts">
      <div class="section-title">
        <h2>Prompt үлгілері</h2>
        <div class="hint">аударманы сапалы қылудың тәсілдері</div>
      </div>

      <div class="two">
        <div class="card">
          <h3>Ресми стиль</h3>
          <div class="mono">Мәтінді қазақ тіліне ресми стильде аудар. Терминдерді бірізді сақта. 
Соңында 5 негізгі терминге қысқа түсіндірме бер.</div>
          <p class="small">Құжат, хат, өтініш сияқты мәтіндерге ыңғайлы.</p>
        </div>
        <div class="card">
          <h3>Екі нұсқа</h3>
          <div class="mono">Мәтінді қазақ тіліне 2 нұсқада аудар: 
(а) дәлме-дәл; (ә) табиғи әдеби стиль. Айырмашылықтарын 3 тармақпен түсіндір.</div>
          <p class="small">Салыстыру арқылы ең дұрыс нұсқаны таңдауға көмектеседі.</p>
        </div>
      </div>
    </section>

    <!-- Checklist -->
    <section id="check">
      <div class="section-title">
        <h2>Тексеру чек-листі</h2>
        <div class="hint">постредактирование</div>
      </div>

      <div class="card">
        <ul style="color:var(--text)">
          <li>Мағына (негізгі ой) сақталды ма?</li>
          <li>Жалғау, септік, жіктік дұрыс па?</li>
          <li>Сөз тәртібі қазақ тіліне табиғи ма?</li>
          <li>Терминдер бірізді ме (бір термин – бір балама)?</li>
          <li>Тұрақты тіркес сөзбе-сөз аударылмаған ба?</li>
          <li>Қажет болса, сөйлемді қайта құрастыруға бола ма?</li>
        </ul>
        <p class="small" style="margin-top:10px">
          Сауалнамада респонденттердің көп бөлігі қателерді жиі байқайды (69,7%).
          Сондықтан соңғы нұсқаны міндетті түрде тексеру ұсынылады.
        </p>
      </div>
    </section>

    <!-- Survey -->
    <section id="survey">
      <div class="section-title">
        <h2>Сауалнама деректері</h2>
        <div class="hint">қысқаша жинақ</div>
      </div>

      <div class="card">
        <ul>
          <li><b>33 респондент:</b> 18–25 жас тобы басым (42,4%).</li>
          <li><b>Қолдану жиілігі:</b> 60,6% автоматты аударманы жиі қолданады.</li>
          <li><b>Ең жиі құралдар:</b> Google Translate – 39,4%, ChatGPT – 39,4%.</li>
          <li><b>Ең жақсы құрал:</b> Google Translate – 54,5%.</li>
          <li><b>Қате мәселесі:</b> 69,7% қателерді жиі байқайды.</li>
        </ul>
      </div>
    </section>

    <footer>
      <div class="footgrid">
        <div class="card">
          <span class="tag">Өнім туралы</span>
          <p class="small" style="margin:10px 0 0">
            Бұл сайт — оқу және зерттеу мақсатында жасалған практикалық өнім.
            Мақсаты: қолданушыға дұрыс құрал таңдау, сапаны арттыру және аударманы тексеру дағдысын қалыптастыру.
          </p>
        </div>
        <div class="card">
          <span class="tag">Ескерту</span>
          <p class="small" style="margin:10px 0 0">
            Автоматты аударма – көмекші құрал. Маңызды/ресми мәтінде соңғы шешімді адам қабылдауы керек.
          </p>
          <div class="mini" style="margin-top:10px">© 2026 QazaqTranslate Guide</div>
        </div>
      </div>
    </footer>
  </div>

  <script>
    const el = (id) => document.getElementById(id);

    const goal = el("goal");
    const textType = el("textType");
    const checklist = el("checklist");
    const doubleCheck = el("doubleCheck");
    const resultBox = el("resultBox");
    const promptBox = el("promptBox");
    const copyMsg = el("copyMsg");

    function getPriority(){
      const r = document.querySelector('input[name="priority"]:checked');
      return r ? r.value : "speed";
    }

    function buildPrompt(mode){
      // mode: formal / natural / compare
      const base =
`Төмендегі мәтінді қазақ тіліне аудар.
Талаптар:
- Мағынаны сақта
- Терминдерді бірізді қолдан
- Сөз тәртібін қазақ тілінің нормасына келтір
- Қажет болса, 1-2 сөйлемді табиғи етіп қайта құрастыр
Мәтін:
[МҰНДА МӘТІНДІ ҚОЙ]`;

      if(mode==="formal"){
        return base + `\n\nҚосымша: Ресми стильді сақта. Соңында 5 негізгі терминге қысқа түсіндірме бер.`;
      }
      if(mode==="compare"){
        return `Мәтінді қазақ тіліне 2 нұсқада аудар:
(а) дәлме-дәл; (ә) табиғи әдеби стиль.
Әр нұсқаның артық/кем тұсын 3 тармақпен түсіндір.
Мәтін:
[МҰНДА МӘТІНДІ ҚОЙ]`;
      }
      return base + `\n\nҚосымша: Мәтінді табиғи әрі түсінікті етіп жаса.`;
    }

    function suggest(){
      const g = goal.value;
      const t = textType.value;
      const p = getPriority();
      const useCheck = checklist.checked;
      const useDouble = doubleCheck.checked;

      let tool = "Google Translate";
      let why = [];
      let caution = [];
      let prompt = "ChatGPT ұсынбады — қажет емес.";

      // Decision rules (simple but logical)
      if(t === "terms" || g === "work" || p === "accuracy"){
        tool = "ChatGPT + Google Translate (салыстыру)";
        why.push("Термин көп немесе ресми мәтін: бір құралға ғана сүйену қауіпті.");
        why.push("ChatGPT контекст пен стильді түзете алады, ал Google Translate — жылдам базалық нұсқа береді.");
        prompt = buildPrompt("formal");
      } else if(t === "long" || p === "quality"){
        tool = "ChatGPT";
        why.push("Ұзақ мәтінде контекст маңызды, ChatGPT сөйлемді табиғи етуге көмектеседі.");
        prompt = buildPrompt("compare");
      } else if(t === "short" && p === "speed" && g !== "work"){
        tool = "Google Translate";
        why.push("Қысқа мәтін және жылдамдық керек болса, Google Translate жеткілікті.");
      } else {
        tool = "Google Translate + ChatGPT (қажет болса)";
        why.push("Алдымен Google Translate арқылы базалық нұсқа алуға болады.");
        why.push("Түсініксіз жер болса, ChatGPT-тен түсіндіру/қайта жазуды сұраған дұрыс.");
        prompt = buildPrompt("natural");
      }

      if(!useCheck){
        caution.push("Нәтижені тексерусіз қолдану қателерді көбейтеді (сауалнамада 69,7% қателерді жиі байқайды).");
      } else {
        why.push("Чек-листпен тексеру сапаны арттырады.");
      }

      if(useDouble){
        why.push("Екі құралмен салыстыру дұрыс нұсқаны таңдауға көмектеседі.");
      } else {
        caution.push("Маңызды мәтінде екі құралмен салыстыру ұсынылады.");
      }

      // Output
      const statusColor = (useCheck && useDouble) ? "ok" : (!useCheck && !useDouble) ? "danger" : "warn";

      resultBox.innerHTML = `
        <h3 style="margin:0 0 8px">Ұсынылған құрал: <span class="${statusColor}">${tool}</span></h3>
        <div class="small"><b>Неге:</b>
          <ul style="margin:8px 0 0 18px">
            ${why.map(x => `<li>${x}</li>`).join("")}
          </ul>
        </div>
        ${caution.length ? `
        <div class="small" style="margin-top:10px"><b>Ескерту:</b>
          <ul style="margin:8px 0 0 18px">
            ${caution.map(x => `<li>${x}</li>`).join("")}
          </ul>
        </div>` : ""}
      `;

      promptBox.textContent = prompt;
      copyMsg.textContent = "";
    }

    function resetAll(){
      goal.value = "study";
      textType.value = "short";
      document.querySelector('input[name="priority"][value="speed"]').checked = true;
      checklist.checked = false;
      doubleCheck.checked = false;
      resultBox.innerHTML = `
        <h3 style="margin:0 0 8px">Ұсыныс осында шығады</h3>
        <p class="small" style="margin:0">Сол жақтан параметрлерді таңда да, <b>“Ұсыныс беру”</b> батырмасын бас.</p>
      `;
      promptBox.textContent = "Мұнда prompt пайда болады…";
      copyMsg.textContent = "";
    }

    async function copyPrompt(){
      try{
        await navigator.clipboard.writeText(promptBox.textContent);
        copyMsg.textContent = "✅ Prompt көшірілді.";
        copyMsg.className = "small ok";
      } catch(e){
        copyMsg.textContent = "Көшіру мүмкін болмады. Prompt-ты қолмен белгіле де көшір.";
        copyMsg.className = "small warn";
      }
    }

    el("btnSuggest").addEventListener("click", suggest);
    el("btnReset").addEventListener("click", resetAll);
    el("btnCopyPrompt").addEventListener("click", copyPrompt);
  </script>
</body>
</html>
