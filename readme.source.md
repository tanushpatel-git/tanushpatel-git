<p align="center">

```aura width=860 height=200
<div style={{
  width: '100%', height: '100%', background: '#08080c',
  display: 'flex', alignItems: 'center', fontFamily: 'Inter',
  position: 'relative', overflow: 'hidden', borderRadius: 16,
  border: '1px solid rgba(59,130,246,0.18)'
}}>

  <style>
    {`
      @keyframes float-slow {
        0%, 100% { transform: translateX(0px); opacity: 0.8; }
        50% { transform: translateX(350px); opacity: 1.2; }
      }
      @keyframes float-medium {
        0%, 100% { transform: translateX(0px); opacity: 0.7; }
        50% { transform: translateX(-250px); opacity: 1.1; }
      }
      @keyframes float-fast {
        0%, 100% { transform: translateX(0px); opacity: 0.9; }
        50% { transform: translateX(200px); opacity: 0.6; }
      }
      @keyframes float-diagonal {
        0%, 100% { transform: translateX(0px); opacity: 0.75; }
        50% { transform: translateX(300px); opacity: 1.0; }
      }
      @keyframes float-wave {
        0%, 100% { transform: translateX(0px); opacity: 0.65; }
        33% { transform: translateX(-160px); opacity: 0.9; }
        66% { transform: translateX(80px); opacity: 1.0; }
      }
      @keyframes float-pulse {
        0%, 100% { transform: scale(1); opacity: 0.8; }
        50% { transform: scale(1.3); opacity: 0.4; }
      }
      #glow-1 { animation: float-slow 8s ease-in-out infinite; }
      #glow-2 { animation: float-medium 12s ease-in-out infinite; }
      #glow-3 { animation: float-fast 9s ease-in-out infinite; }
      #glow-4 { animation: float-slow 11s ease-in-out infinite reverse; }
      #glow-5 { animation: float-medium 14s ease-in-out infinite reverse; }
      #glow-6 { animation: float-diagonal 10s ease-in-out infinite; }
      #glow-7 { animation: float-wave 13s ease-in-out infinite; }
      #glow-8 { animation: float-pulse 7s ease-in-out infinite; }
    `}
  </style>

  <svg width="860" height="200" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="g1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(37,99,235,0.72)" />
        <stop offset="40%" stopColor="rgba(29,78,216,0.35)" />
        <stop offset="70%" stopColor="rgba(29,78,216,0)" />
      </radialGradient>
      <radialGradient id="g2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(59,130,246,0.6)" />
        <stop offset="45%" stopColor="rgba(37,99,235,0.25)" />
        <stop offset="70%" stopColor="rgba(37,99,235,0)" />
      </radialGradient>
      <radialGradient id="g3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(96,165,250,0.45)" />
        <stop offset="50%" stopColor="rgba(59,130,246,0.18)" />
        <stop offset="70%" stopColor="rgba(59,130,246,0)" />
      </radialGradient>
      <radialGradient id="g4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(147,197,253,0.32)" />
        <stop offset="70%" stopColor="rgba(147,197,253,0)" />
      </radialGradient>
      <radialGradient id="g5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(191,219,254,0.38)" />
        <stop offset="70%" stopColor="rgba(191,219,254,0)" />
      </radialGradient>
      <radialGradient id="g6" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(37,99,235,0.55)" />
        <stop offset="45%" stopColor="rgba(29,78,216,0.22)" />
        <stop offset="70%" stopColor="rgba(29,78,216,0)" />
      </radialGradient>
      <radialGradient id="g7" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(59,130,246,0.42)" />
        <stop offset="50%" stopColor="rgba(37,99,235,0.16)" />
        <stop offset="70%" stopColor="rgba(37,99,235,0)" />
      </radialGradient>
      <radialGradient id="g8" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(96,165,250,0.40)" />
        <stop offset="50%" stopColor="rgba(59,130,246,0.15)" />
        <stop offset="70%" stopColor="rgba(59,130,246,0)" />
      </radialGradient>
    </defs>
    <ellipse id="glow-1" cx="180" cy="230" rx="260" ry="190" fill="url(#g1)" />
    <ellipse id="glow-2" cx="300" cy="240" rx="220" ry="160" fill="url(#g2)" />
    <ellipse id="glow-3" cx="420" cy="240" rx="180" ry="140" fill="url(#g3)" />
    <ellipse id="glow-4" cx="550" cy="250" rx="150" ry="120" fill="url(#g4)" />
    <ellipse id="glow-5" cx="750" cy="250" rx="130" ry="110" fill="url(#g5)" />
    <ellipse id="glow-6" cx="300" cy="240" rx="180" ry="140" fill="url(#g6)" />
    <ellipse id="glow-7" cx="490" cy="230" rx="220" ry="170" fill="url(#g7)" />
    <ellipse id="glow-8" cx="590" cy="250" rx="150" ry="130" fill="url(#g8)" />
  </svg>

  <div style={{
    position: 'absolute', left: 48, top: 52, width: 96, height: 96,
    borderRadius: 48, background: 'linear-gradient(135deg, #3B82F6, #ffffff)',
    display: 'flex', alignItems: 'center', justifyContent: 'center',
  }}>
    <img src={github.user.avatarUrl} width={88} height={88} style={{ borderRadius: 44 }} />
  </div>

  <div style={{ display:'flex', flexDirection:'column', marginLeft:168, gap:8, zIndex: 10 }}>
    <div style={{ display:'flex', fontSize:38, fontWeight:800, color:'#ffffff', letterSpacing:'-1px', lineHeight:1 }}>
      {github.user.name || github.user.login}
    </div>
    <div style={{ display:'flex', fontSize:15, color:'rgba(191,219,254,0.8)', fontWeight:400, letterSpacing:'0.3px' }}>
      {github.user.bio || 'Full Stack Developer · Building clean, fast, modern web experiences'}
    </div>
    <div style={{ display:'flex', gap:8, marginTop:6 }}>
      {['Full-Stack', 'React', 'Next.js', 'TypeScript'].map(function(tag) {
        return (
          <div key={tag} style={{
            display:'flex', padding:'4px 12px', borderRadius:20,
            background:'rgba(59,130,246,0.18)', border:'1px solid rgba(59,130,246,0.32)',
            color:'rgba(191,219,254,0.85)', fontSize:12, fontWeight:600,
          }}>{tag}</div>
        );
      })}
    </div>
  </div>
</div>
```

</p>

<br>

```aura width=860 height=140
(function() {
  var stats = [
    { label: 'Repos', value: String(github.stats.totalRepos), color: '#93C5FD' },
    { label: 'Stars', value: String(github.stats.totalStars), color: '#60A5FA' },
    { label: 'Commits', value: String(github.stats.totalCommits), color: '#3B82F6' },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#08080c',
      display: 'flex', alignItems: 'center', justifyContent: 'center',
      fontFamily: 'Inter', borderRadius: 16,
      border: '1px solid rgba(59,130,246,0.18)',
      position: 'relative', overflow: 'hidden',
    }}>

      <style>
        {`
          @keyframes float-slow {
            0%, 100% { transform: translateX(0px); opacity: 0.8; }
            50% { transform: translateX(350px); opacity: 1.2; }
          }
          @keyframes float-medium {
            0%, 100% { transform: translateX(0px); opacity: 0.7; }
            50% { transform: translateX(-250px); opacity: 1.1; }
          }
          @keyframes float-fast {
            0%, 100% { transform: translateX(0px); opacity: 0.9; }
            50% { transform: translateX(200px); opacity: 0.6; }
          }
          @keyframes float-diagonal {
            0%, 100% { transform: translate(0px, 0px); opacity: 0.75; }
            50% { transform: translate(120px, 30px); opacity: 1.0; }
          }
          @keyframes float-wave {
            0%, 100% { transform: translateX(0px); opacity: 0.65; }
            33% { transform: translateX(-160px); opacity: 0.9; }
            66% { transform: translateX(80px); opacity: 1.0; }
          }
          #glow-1 { animation: float-slow 8s ease-in-out infinite; }
          #glow-2 { animation: float-medium 12s ease-in-out infinite; }
          #glow-3 { animation: float-fast 9s ease-in-out infinite; }
          #glow-4 { animation: float-diagonal 10s ease-in-out infinite; }
          #glow-5 { animation: float-wave 14s ease-in-out infinite; }
        `}
      </style>

      <svg width="860" height="140" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="g1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(37,99,235,0.65)" />
            <stop offset="45%" stopColor="rgba(29,78,216,0.28)" />
            <stop offset="70%" stopColor="rgba(29,78,216,0)" />
          </radialGradient>
          <radialGradient id="g2" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(59,130,246,0.55)" />
            <stop offset="45%" stopColor="rgba(37,99,235,0.22)" />
            <stop offset="70%" stopColor="rgba(37,99,235,0)" />
          </radialGradient>
          <radialGradient id="g3" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(96,165,250,0.42)" />
            <stop offset="70%" stopColor="rgba(96,165,250,0)" />
          </radialGradient>
          <radialGradient id="g4" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(147,197,253,0.30)" />
            <stop offset="70%" stopColor="rgba(147,197,253,0)" />
          </radialGradient>
          <radialGradient id="g5" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(191,219,254,0.40)" />
            <stop offset="70%" stopColor="rgba(191,219,254,0)" />
          </radialGradient>
        </defs>
        <ellipse id="glow-1" cx="710" cy="150" rx="210" ry="150" fill="url(#g1)" />
        <ellipse id="glow-2" cx="550" cy="140" rx="190" ry="140" fill="url(#g2)" />
        <ellipse id="glow-3" cx="400" cy="130" rx="170" ry="130" fill="url(#g3)" />
        <ellipse id="glow-4" cx="250" cy="140" rx="150" ry="120" fill="url(#g4)" />
        <ellipse id="glow-5" cx="100" cy="150" rx="130" ry="110" fill="url(#g5)" />
      </svg>

      {stats.map(function(s, i) {
        return (
          <div key={s.label} style={{
            flexGrow: 1, display: 'flex', flexDirection: 'column',
            alignItems: 'center', justifyContent: 'center',
            padding: '16px 8px',
            borderRight: i < stats.length - 1 ? '1px solid rgba(255,255,255,0.06)' : 'none',
            gap: 5,
          }}>
            <div style={{ display:'flex', fontSize:30, fontWeight:800, color:s.color, lineHeight:1 }}>
              {s.value}
            </div>
            <div style={{ display:'flex', fontSize:11, color:'rgba(147,197,253,0.45)', fontWeight:600, letterSpacing:'1.5px' }}>
              {s.label.toUpperCase()}
            </div>
          </div>
        );
      })}
    </div>
  );
})()
```

<br>

```aura width=860 height=290
(function() {
  var categories = [
    { title: 'Languages', color: '#93C5FD', items: ['JavaScript', 'TypeScript', 'Python', 'Java', 'Go'] },
    { title: 'Frontend', color: '#60A5FA', items: ['React', 'Next.js', 'Tailwind CSS', 'Bootstrap'] },
    { title: 'Backend', color: '#3B82F6', items: ['Node.js', 'Express.js', 'GraphQL'] },
    { title: 'Databases', color: '#2563EB', items: ['MongoDB', 'Redis', 'SQL'] },
    { title: 'DevOps & Cloud', color: '#1D4ED8', items: ['Docker', 'Kubernetes', 'Git'] },
    { title: 'Tools & Design', color: '#DBEAFE', items: ['Figma', 'VS Code', 'Postman'] },
  ];

  return (
    <div style={{
      width: '100%', height: '100%',
      background: '#08080c',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter', padding: '18px 32px', gap: 14,
      borderRadius: 16, border: '1px solid rgba(59,130,246,0.18)',
      position: 'relative', overflow: 'hidden',
    }}>

      <style>
        {`
          @keyframes float-slow {
            0%, 100% { transform: translateX(0px); opacity: 0.8; }
            50% { transform: translateX(350px); opacity: 1.2; }
          }
          @keyframes float-medium {
            0%, 100% { transform: translateX(0px); opacity: 0.7; }
            50% { transform: translateX(-250px); opacity: 1.1; }
          }
          @keyframes float-fast {
            0%, 100% { transform: translateX(0px); opacity: 0.9; }
            50% { transform: translateX(200px); opacity: 0.6; }
          }
          @keyframes float-diagonal {
            0%, 100% { transform: translate(0px, 0px); opacity: 0.75; }
            50% { transform: translate(120px, 30px); opacity: 1.0; }
          }
          @keyframes float-wave {
            0%, 100% { transform: translateX(0px); opacity: 0.65; }
            33% { transform: translateX(-160px); opacity: 0.9; }
            66% { transform: translateX(80px); opacity: 1.0; }
          }
          @keyframes float-pulse {
            0%, 100% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.3); opacity: 0.4; }
          }
          #glow-1 { animation: float-slow 9s ease-in-out infinite; }
          #glow-2 { animation: float-medium 12s ease-in-out infinite; }
          #glow-3 { animation: float-fast 8s ease-in-out infinite; }
          #glow-4 { animation: float-diagonal 11s ease-in-out infinite reverse; }
          #glow-5 { animation: float-wave 14s ease-in-out infinite reverse; }
          #glow-6 { animation: float-pulse 6s ease-in-out infinite; }
        `}
      </style>

      <svg width="860" height="290" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="g1" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(37,99,235,0.68)" />
            <stop offset="42%" stopColor="rgba(29,78,216,0.30)" />
            <stop offset="70%" stopColor="rgba(29,78,216,0)" />
          </radialGradient>
          <radialGradient id="g2" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(59,130,246,0.55)" />
            <stop offset="45%" stopColor="rgba(37,99,235,0.22)" />
            <stop offset="70%" stopColor="rgba(37,99,235,0)" />
          </radialGradient>
          <radialGradient id="g3" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(96,165,250,0.42)" />
            <stop offset="50%" stopColor="rgba(59,130,246,0.16)" />
            <stop offset="70%" stopColor="rgba(59,130,246,0)" />
          </radialGradient>
          <radialGradient id="g4" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(147,197,253,0.32)" />
            <stop offset="70%" stopColor="rgba(147,197,253,0)" />
          </radialGradient>
          <radialGradient id="g5" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(191,219,254,0.42)" />
            <stop offset="70%" stopColor="rgba(191,219,254,0)" />
          </radialGradient>
          <radialGradient id="g6" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(219,234,254,0.35)" />
            <stop offset="70%" stopColor="rgba(219,234,254,0)" />
          </radialGradient>
        </defs>
        <ellipse id="glow-1" cx="170" cy="290" rx="260" ry="170" fill="url(#g1)" />
        <ellipse id="glow-2" cx="320" cy="300" rx="220" ry="140" fill="url(#g2)" />
        <ellipse id="glow-3" cx="460" cy="300" rx="190" ry="130" fill="url(#g3)" />
        <ellipse id="glow-4" cx="590" cy="310" rx="160" ry="110" fill="url(#g4)" />
        <ellipse id="glow-5" cx="750" cy="310" rx="140" ry="100" fill="url(#g5)" />
        <ellipse id="glow-6" cx="420" cy="260" rx="100" ry="80" fill="url(#g6)" />
      </svg>

      <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(147,197,253,0.5)', letterSpacing:'3px' }}>
        TECH STACK
      </div>
      <div style={{ display:'flex', flexDirection:'column', gap:14 }}>
        {categories.map(function(cat) {
          return (
            <div key={cat.title} style={{ display:'flex', alignItems:'center', gap:16 }}>
              <div style={{ display:'flex', fontSize:10, fontWeight:700, color:cat.color, letterSpacing:'1px', width:110 }}>
                {cat.title.toUpperCase()}
              </div>
              <div style={{ display:'flex', flexWrap:'wrap', gap:7 }}>
                {cat.items.map(function(item) {
                  return (
                    <div key={item} style={{
                      display:'flex', padding:'4px 13px', borderRadius:6,
                      background:cat.color + '15', border:'1px solid ' + cat.color + '35',
                      color:'rgba(225,220,255,0.85)', fontSize:12, fontWeight:600,
                    }}>{item}</div>
                  );
                })}
              </div>
            </div>
          );
        })}
      </div>
    </div>
  );
})()
```

<br>

```aura width=860 height=200
<div style={{
  width: '100%', height: '100%', background: '#08080c',
  display: 'flex', flexDirection: 'column',
  fontFamily: 'Inter', padding: '18px 28px', gap: 14,
  borderRadius: 16, border: '1px solid rgba(59,130,246,0.18)',
  position: 'relative', overflow: 'hidden',
}}>
  <style>
    {`
      @keyframes floatP1 {
        0%, 100% { transform: translateX(0px); opacity: 0.55; }
        50% { transform: translateX(30px); opacity: 0.7; }
      }
      @keyframes floatP2 {
        0%, 100% { transform: translateX(0px); opacity: 0.35; }
        50% { transform: translateX(-25px); opacity: 0.5; }
      }
      @keyframes floatP3 {
        0%, 100% { transform: translateX(0px); opacity: 0.25; }
        50% { transform: translateX(20px); opacity: 0.4; }
      }
      #gp-glow-1 { animation: floatP1 7s ease-in-out infinite; }
      #gp-glow-2 { animation: floatP2 9s ease-in-out infinite; }
      #gp-glow-3 { animation: floatP3 8s ease-in-out infinite; }
    `}
  </style>
  <svg width="860" height="190" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="gp1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(37,99,235,0.55)" />
        <stop offset="45%" stopColor="rgba(29,78,216,0.22)" />
        <stop offset="70%" stopColor="rgba(29,78,216,0)" />
      </radialGradient>
      <radialGradient id="gp2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(59,130,246,0.35)" />
        <stop offset="45%" stopColor="rgba(37,99,235,0.14)" />
        <stop offset="70%" stopColor="rgba(37,99,235,0)" />
      </radialGradient>
      <radialGradient id="gp3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(96,165,250,0.25)" />
        <stop offset="70%" stopColor="rgba(96,165,250,0)" />
      </radialGradient>
    </defs>
    <ellipse id="gp-glow-1" cx="140" cy="160" rx="220" ry="170" fill="url(#gp1)" />
    <ellipse id="gp-glow-2" cx="430" cy="150" rx="200" ry="160" fill="url(#gp2)" />
    <ellipse id="gp-glow-3" cx="720" cy="140" rx="180" ry="150" fill="url(#gp3)" />
  </svg>

  <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(147,197,253,0.5)', letterSpacing:'3px', zIndex:1 }}>
    TOP PROJECTS
  </div>

  <div style={{
    display: 'flex', flexWrap: 'wrap', gap: 10, zIndex: 1,
  }}>
    {[
      { name: 'TluxAi', desc: 'AI Embedding Pipeline', url: 'https://github.com/tanushpatel-git/Ai-Embedding-Tlux.git' },
      { name: 'CodeEra', desc: 'Collaborative Coding Platform', url: 'https://github.com/tanushpatel-git/CodeEra.git' },
      { name: 'Topmate', desc: '1-on-1 Mentorship Platform', url: 'https://github.com/tanushpatel-git/Topmate-1-1-.git' },
      { name: 'Github_tanu', desc: 'GitHub Profile Tools', url: 'https://github.com/tanushpatel-git/Github_tanu.git' },
    ].map(function(p) {
      return (
        <a key={p.name} href={p.url} style={{ textDecoration: 'none' }}>
          <div style={{
            display: 'flex', flexDirection: 'column', gap: 3,
            padding: '12px 16px', borderRadius: 10,
            background: 'rgba(59,130,246,0.08)',
            border: '1px solid rgba(59,130,246,0.15)',
            width: 182, minWidth: 182,
          }}>
            <div style={{
              display:'flex', fontSize:13, fontWeight:700, color:'rgba(191,219,254,0.9)',
            }}>{p.name}</div>
            <div style={{
              display:'flex', fontSize:10, color:'rgba(148,163,184,0.6)', fontWeight:500,
            }}>{p.desc}</div>
          </div>
        </a>
      );
    })}
  </div>
</div>
```

<br>

```aura width=860 height=200
(function() {
  var days = ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat'];
  var today = new Date();
  var dayLabels = [];
  var heights = [18, 42, 35, 58, 24, 66, 48, 72, 30, 55, 80, 44, 62, 90, 38];
  for (var i = 14; i >= 0; i--) {
    var d = new Date(today);
    d.setDate(d.getDate() - i);
    dayLabels.push(days[d.getDay()] + ' ' + d.getDate());
  }
  var barW = 38;
  var gap = 12;
  var startX = 32;

  return (
    <div style={{
      width: '100%', height: '100%', background: '#08080c',
      display: 'flex', flexDirection: 'column',
      fontFamily: 'Inter', borderRadius: 16,
      border: '1px solid rgba(59,130,246,0.18)',
      position: 'relative', overflow: 'hidden', padding: '16px 24px 12px',
    }}>
      <svg width="860" height="200" style={{ position: 'absolute', top: 0, left: 0 }}>
        <defs>
          <radialGradient id="g-day" cx="50%" cy="50%" r="50%">
            <stop offset="0%" stopColor="rgba(37,99,235,0.15)" />
            <stop offset="70%" stopColor="rgba(37,99,235,0)" />
          </radialGradient>
        </defs>
        <ellipse cx="430" cy="120" rx="380" ry="160" fill="url(#g-day)" />
      </svg>

      <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(147,197,253,0.5)', letterSpacing:'3px', zIndex:1 }}>
        LAST 15 DAYS
      </div>

      <div style={{
        display: 'flex', justifyContent: 'center', alignItems: 'flex-end',
        gap: 12, marginTop: 10, height: 110, zIndex: 1,
      }}>
        {heights.map(function(h, i) {
          var isMax = h === 90;
          return (
            <div key={i} style={{
              display: 'flex', flexDirection: 'column', alignItems: 'center', gap: 4, width: 38,
            }}>
              <div style={{
                display:'flex', fontSize:9, fontWeight:600,
                color: isMax ? 'rgba(96,165,250,0.9)' : 'rgba(148,163,184,0.6)',
              }}>{h}</div>
              <div style={{
                width: 22, height: h + 4, borderRadius: '4px 4px 2px 2px',
                background: isMax
                  ? 'linear-gradient(180deg, #3B82F6, #60A5FA)'
                  : 'linear-gradient(180deg, rgba(59,130,246,0.6), rgba(96,165,250,0.25))',
                opacity: isMax ? 1 : 0.8,
                transition: 'opacity 0.2s',
              }} />
              <div style={{
                fontSize: 7, fontWeight: 500, color: 'rgba(100,116,139,0.5)',
                letterSpacing: '0.5px', textAlign: 'center', marginTop: 2,
                whiteSpace: 'nowrap',
              }}>{dayLabels[i]}</div>
            </div>
          );
        })}
      </div>
    </div>
  );
})()
```

<br>

## 🌐 Connect With Me

<p align="center">

```aura width=120 height=44 link="https://github.com/tanushpatel-git" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/github/ffffff"
  text="GitHub"
  backgroundColor="#000000"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#3B82F6' },
    { offset: '30%', color: '#000000' },
    { offset: '60%', color: '#2563EB' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#60A5FA' },
  ]}
/>
```

```aura width=130 height=44 link="https://tanushportfolioo.netlify.app" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/vercel/ffffff"
  text="Portfolio"
  backgroundColor="#000000"
  width={130}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#60A5FA' },
    { offset: '30%', color: '#000000' },
    { offset: '60%', color: '#3B82F6' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#93C5FD' },
  ]}
/>
```

```aura width=110 height=44 link="https://wa.me/919729348173" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/whatsapp/ffffff"
  text="WhatsApp"
  backgroundColor="#000000"
  width={110}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#93C5FD' },
    { offset: '30%', color: '#000000' },
    { offset: '60%', color: '#60A5FA' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#BFDBFE' },
  ]}
/>
```

```aura width=110 height=44 link="mailto:tanush000patel@gmail.com" inline align=center
<SocialMediaButton
  icon="https://cdn.simpleicons.org/gmail/ffffff"
  text="Email"
  backgroundColor="#000000"
  width={110}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#ffffff' },
    { offset: '30%', color: '#000000' },
    { offset: '60%', color: '#3B82F6' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#93C5FD' },
  ]}
/>
```

</p>

<br>

<p align="center"><sub>powered by <a href="https://github.com/collectioneur/readme-aura">readme-aura</a></sub></p>
