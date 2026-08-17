<div class="wrap">

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=JetBrains+Mono:wght@400;500;600&display=swap');

.wrap{
  --ink:#e8efe9;
  --muted:#7f8d86;
  --dim:#4d5a54;
  --line:#1f2d26;
  --panel:#0f1613;
  --bg:#0a0e0c;
  --green:#9fe870;
  --amber:#f0b35a;
  --serif:'DM Serif Display',Georgia,serif;
  --mono:'JetBrains Mono',ui-monospace,Consolas,monospace;
  background:var(--bg);
  color:var(--ink);
  font-family:var(--mono);
  font-size:14px;
  line-height:1.7;
  max-width:880px;
  margin:0 auto;
  padding:48px 28px 32px;
}
a{color:inherit}
kbd{font-family:inherit;font-size:.85em;border:1px solid var(--line);border-bottom-width:2px;padding:1px 6px;border-radius:3px;color:var(--muted)}

/* header */
.hero{display:grid;grid-template-columns:1fr auto;gap:32px;align-items:start}
.eyebrow{font-size:11px;letter-spacing:.22em;color:var(--dim);text-transform:uppercase;margin:0 0 18px}
.hero h1{
  font-family:var(--serif);font-weight:400;
  font-size:clamp(64px,10vw,116px);
  line-height:.82;letter-spacing:-.015em;
  margin:0;text-align:left;
  animation:rise .9s cubic-bezier(.2,.7,.2,1) both;
}
.hero h1 .lt{display:block}
.hero h1 .lt2{display:block;font-style:italic;color:var(--green);padding-left:.2em}
@keyframes rise{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:none}}
.tag{color:var(--muted);font-size:13px;max-width:540px;margin:22px 0 0;text-align:left;animation:rise .9s .15s cubic-bezier(.2,.7,.2,1) both}
.tag b{color:var(--ink);font-weight:500}

.status{
  border:1px solid var(--line);background:var(--panel);
  padding:14px 18px;font-size:11px;color:var(--muted);
  line-height:2.1;white-space:nowrap;min-width:230px;
  animation:rise .9s .25s cubic-bezier(.2,.7,.2,1) both;
}
.status .row{display:flex;align-items:center;gap:9px}
.dot{width:7px;height:7px;border-radius:50%;background:var(--green);box-shadow:0 0 12px var(--green);flex:none;animation:pulse 1.6s infinite}
@keyframes pulse{50%{opacity:.35;transform:scale(.7)}}
.status b{color:var(--ink);font-weight:500}
.status a{color:var(--green);text-decoration:none;border-bottom:1px solid var(--green)}
.status a:hover{color:var(--ink);border-color:var(--ink)}

/* section headers */
h2{font-family:var(--serif);font-weight:400;font-size:30px;line-height:1;margin:0 0 18px}
.idx{font-family:var(--mono);font-size:12px;color:var(--dim);letter-spacing:.18em;margin-right:14px;vertical-align:middle}
.lede{color:var(--muted);font-size:13px;max-width:600px;margin:-8px 0 22px}

.divider{height:1px;background:var(--line);position:relative;overflow:hidden;margin:44px 0}
.divider:after{content:'';position:absolute;inset:0;background:var(--green);transform:scaleX(0);transform-origin:left;animation:fill 9s linear infinite}
@keyframes fill{0%{transform:scaleX(0)}72%{transform:scaleX(1)}100%{transform:scaleX(1)}}

/* shipping log */
.log{
  border:1px solid var(--line);background:var(--panel);
  height:46px;position:relative;overflow:hidden;
  padding:12px 16px;
}
.log span{
  position:absolute;left:16px;right:16px;top:12px;margin:0;
  font-size:12.5px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;
  opacity:0;
  animation:logline 15s linear infinite;
}
.log .k{display:inline-block;width:52px;font-weight:600}
.log .k.build{color:var(--green)}
.log .k.ship{color:var(--ink)}
.log .k.play{color:var(--amber)}
.log .m{color:var(--muted)}
.log span:nth-child(1){animation-delay:0s}
.log span:nth-child(2){animation-delay:3s}
.log span:nth-child(3){animation-delay:6s}
.log span:nth-child(4){animation-delay:9s}
.log span:nth-child(5){animation-delay:12s}
@keyframes logline{
  0%{opacity:0;transform:translateY(10px)}
  3%{opacity:1;transform:translateY(0)}
  17%{opacity:1}
  20%{opacity:0;transform:translateY(-10px)}
  100%{opacity:0;transform:translateY(-10px)}
}

/* game frame */
.frame{
  border:1px solid var(--line);background:var(--panel);
  padding:20px 22px 18px;position:relative;
}
.frame:before{content:'';position:absolute;left:0;right:0;top:0;height:2px;background:var(--green)}
.frame .top{display:flex;justify-content:space-between;align-items:center;gap:16px;flex-wrap:wrap;margin-bottom:4px}
.frame h3{font-family:var(--serif);font-weight:400;font-size:24px;margin:6px 0 0}
.frame .mini{font-size:10px;letter-spacing:.2em;text-transform:uppercase;color:var(--dim)}
.play{
  display:inline-block;border:1px solid var(--green);color:var(--green);
  padding:8px 16px;font-family:inherit;font-size:12px;text-decoration:none;
  transition:background .25s,color .25s,transform .15s;
}
.play:hover{background:var(--green);color:#0a0e0c;transform:translateY(-1px)}
.play:active{transform:translateY(1px)}
.frame .img{text-align:center;margin:12px 0 14px;line-height:0}
.frame .note{color:var(--muted);font-size:12px;text-align:center;margin:0}

/* work table */
table.work{width:100%;border-collapse:collapse;font-size:13px}
.work th{font-size:10px;font-weight:500;letter-spacing:.16em;text-transform:uppercase;color:var(--dim);text-align:left;padding:10px 12px;border-bottom:1px solid var(--line)}
.work td{padding:13px 12px;border-bottom:1px solid var(--line);vertical-align:top}
.work td:first-child{border-left:2px solid transparent;transition:border-color .2s}
.work tr:hover td{background:#0e1511}
.work tr:hover td:first-child{border-left-color:var(--green)}
.work .name{color:var(--ink);text-decoration:none;font-weight:500}
.work .name:hover{color:var(--green)}
.work .meta{color:var(--muted);font-size:12px}
.work .where{color:var(--dim);font-size:12px}

/* stats + tools */
.row2{display:flex;gap:18px;flex-wrap:wrap;justify-content:center}
.row2 img{max-width:100%}

/* how I work */
.steps{display:grid;gap:26px}
.step{display:grid;grid-template-columns:76px 1fr;gap:16px;align-items:baseline}
.step .n{font-family:var(--serif);font-style:italic;font-size:30px;color:var(--dim);line-height:1}
.step h4{font-size:14px;margin:0 0 4px;font-weight:600;letter-spacing:.01em}
.step p{color:var(--muted);font-size:13px;margin:0;max-width:560px}

/* footer */
.foot{text-align:center;color:var(--dim);font-size:12px;letter-spacing:.2em;margin-top:44px}
.foot .views{margin-top:18px;line-height:0}
.foot .hand{display:inline-block;margin-top:16px;font-size:10.5px;letter-spacing:.14em;color:var(--dim);border-top:1px solid var(--line);padding-top:14px}

@media (max-width:720px){
  .hero{grid-template-columns:1fr}
  .status{white-space:normal;min-width:0}
}
@media (prefers-reduced-motion: reduce){
  .hero h1,.tag,.status{animation:none}
  .log span{animation:none}
  .log span:first-child{opacity:1}
  .divider:after{animation:none;transform:scaleX(1);background:var(--line)}
  .dot{animation:none}
}
</style>

<section class="hero">
  <div>
    <p class="eyebrow">Naufal Almahi &middot; Full-Stack Developer &middot; Indonesia</p>
    <h1><span class="lt">Naufal</span><span class="lt2">Almahi</span></h1>
    <p class="tag">I build SaaS products with <b>Laravel</b> and <b>Next.js</b> &mdash; the kind where the hard parts are invisible: tenant isolation, checkout states, the edge cases real users find.</p>
  </div>
  <div class="status">
    <div class="row"><span class="dot"></span><span><b>open to work</b> &middot; remote friendly</span></div>
    <div class="row">&nbsp;</div>
    <div class="row"><span style="color:var(--dim)">github</span> <a href="https://github.com/Naufalmahi">Naufalmahi</a></div>
    <div class="row"><span style="color:var(--dim)">zoneline</span> <a href="https://github.com/Naufalmahi/zoneline">multi-tenant commerce</a></div>
    <div class="row"><span style="color:var(--dim)">wisesa</span> <a href="https://github.com/Naufalmahi/wisesa-frontend">product frontend</a></div>
  </div>
</section>

<div class="divider"></div>

<section>
  <h2><span class="idx">01</span>Shipping log</h2>
  <p class="lede">Not a dashboard &mdash; an actual log of what is being built and shipped right now.</p>
  <div class="log">
    <span><span class="k build">build</span><span class="m">zoneline &mdash; tenant isolation: green</span></span>
    <span><span class="k ship">ship</span><span class="m">wisesa-frontend &mdash; product shell live</span></span>
    <span><span class="k ship">ship</span><span class="m">wisesa-backend &mdash; api services up</span></span>
    <span><span class="k build">build</span><span class="m">jual-baju &mdash; checkout flow wired</span></span>
    <span><span class="k play">play</span><span class="m">contribution run &mdash; it is a real game, not a badge</span></span>
  </div>
</section>

<div class="divider"></div>

<section>
  <h2><span class="idx">02</span>Play the graph</h2>
  <p class="lede">This contribution graph is not decoration. It drives a browser game &mdash; playable right here on the profile.</p>
  <div class="frame">
    <div class="top">
      <div>
        <p class="mini">playground 01</p>
        <h3>Contribution Run</h3>
      </div>
      <a class="play" href="https://naufalmahi.github.io/Naufalmahi/game/">Play the game &rarr;</a>
    </div>
    <p class="img"><img src="https://raw.githubusercontent.com/Naufalmahi/Naufalmahi/output/github-contribution-grid-snake.svg" alt="Animated contribution graph" /></p>
    <p class="note">Eat the commits, don&rsquo;t hit the wall &mdash; same rules as shipping. Move with <kbd>WASD</kbd> or swipe.</p>
  </div>
</section>

<div class="divider"></div>

<section>
  <h2><span class="idx">03</span>Selected work</h2>
  <p class="lede">The boring edge cases are where the real engineering starts.</p>
  <table class="work">
    <tr><th>Project</th><th>Problem space</th><th>Stack</th><th>Where the hard parts live</th></tr>
    <tr>
      <td><a class="name" href="https://github.com/Naufalmahi/zoneline">Zoneline</a></td>
      <td class="meta">Multi-tenant commerce</td>
      <td class="meta">Laravel &middot; PHP &middot; MySQL</td>
      <td class="where">tenant isolation, checkout states, payment flow</td>
    </tr>
    <tr>
      <td><a class="name" href="https://github.com/Naufalmahi/wisesa-frontend">Wisesa Frontend</a></td>
      <td class="meta">Product frontend</td>
      <td class="meta">Next.js &middot; React</td>
      <td class="where">app shell, state across a real product flow</td>
    </tr>
    <tr>
      <td><a class="name" href="https://github.com/Naufalmahi/wisesa-backend">Wisesa Backend</a></td>
      <td class="meta">API and data services</td>
      <td class="meta">Node.js &middot; SQL Server</td>
      <td class="where">schema decisions, query paths that stay fast</td>
    </tr>
    <tr>
      <td><a class="name" href="https://github.com/Naufalmahi/jual-baju">Jual Baju</a></td>
      <td class="meta">E-commerce workflow</td>
      <td class="meta">Laravel &middot; PHP &middot; MySQL</td>
      <td class="where">order flow from cart to confirmation</td>
    </tr>
  </table>
</section>

<div class="divider"></div>

<section>
  <h2><span class="idx">04</span>Recent output</h2>
  <p class="lede">A graph, because graphs keep score.</p>
  <div class="row2">
    <img height="180" src="https://github-readme-stats.vercel.app/api?username=Naufalmahi&show_icons=true&hide_border=true&theme=github_dark&rank_icon=github&include_all_commits=true&title_color=9FE870&icon_color=9FE870" alt="GitHub statistics" />
    <img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Naufalmahi&layout=compact&hide_border=true&theme=github_dark&langs_count=8&title_color=9FE870" alt="Top languages" />
  </div>
</section>

<div class="divider"></div>

<section>
  <h2><span class="idx">05</span>Tools I reach for</h2>
  <div class="row2">
    <img src="https://skillicons.dev/icons?i=php,laravel,js,ts,react,nextjs,python,mysql,mssql,git,github,docker,vscode&perline=13" alt="Development tools" />
  </div>
</section>

<div class="divider"></div>

<section>
  <h2><span class="idx">06</span>How I work</h2>
  <div class="steps">
    <div class="step">
      <span class="n">01</span>
      <div><h4>Find the constraint</h4><p>What actually makes the product hard?</p></div>
    </div>
    <div class="step">
      <span class="n">02</span>
      <div><h4>Build the smallest useful path</h4><p>Make the core flow work before polishing the edges.</p></div>
    </div>
    <div class="step">
      <span class="n">03</span>
      <div><h4>Ship it</h4><p>A deployed imperfect product teaches more than an unfinished perfect one.</p></div>
    </div>
    <div class="step">
      <span class="n">04</span>
      <div><h4>Fix what users expose</h4><p>The weird cases are usually where the real engineering starts.</p></div>
    </div>
  </div>
</section>

<div class="foot">
  <div>BUILD &middot; SHIP &middot; LEARN &middot; REPEAT</div>
  <div class="views"><img src="https://komarev.com/ghpvc/?username=Naufalmahi&style=flat-square&color=9FE870" alt="Profile views" /></div>
  <div class="hand">hand-built &middot; no templates</div>
</div>

</div>
