## 🎭 Генератор НПС

Нажмите кнопку ниже, чтобы создать случайного персонажа:

<div id="npc-result" style="background:#3a2a1a; padding:15px; border-radius:8px; margin:15px 0; font-style:italic;">
  Здесь появится НПС...
</div>

<button onclick="generateNPC()" style="background:#d4af37; color:#1a110a; border:none; padding:10px 20px; font-size:1em; border-radius:6px; cursor:pointer; font-weight:bold;">
  🎲 Сгенерировать НПС
</button>

<script>
  const names = [
    "Альдред", "Бриззарда", "Громвальд", "Лира", "Морган", "Талия", "Фенрис", "Зельда", "Дроган", "Элария"
  ];
  const races = [
    "человек", "эльф", "гном", "полурослик", "орк", "тифлинг", "драконорождённый", "халфлинг", "голиаф", "генази"
  ];
  const roles = [
    "торговец зельями", "бродячий бард", "старый маг", "шпион", "священник", "наёмник", "пират", "археолог", "шут", "лесной страж"
  ];
  const traits = [
    "говорит загадками", "всегда врёт", "обожает золото", "боится темноты", "постоянно чихает", "носит маску", "поёт при каждой возможности", "верит в призраков", "влюблён в героя", "искренне добр"
  ];
  const secrets = [
    "на самом деле — беглый принц", "ищет пропавшего брата", "служит тайному культисту", "украл артефакт", "помнит прошлую жизнь", "владеет запретным заклинанием", "живёт под чужим именем", "видит духов", "проклят", "работает на Мастера игры"
  ];

  function generateNPC() {
    const name = names[Math.floor(Math.random() * names.length)];
    const race = races[Math.floor(Math.random() * races.length)];
    const role = roles[Math.floor(Math.random() * roles.length)];
    const trait = traits[Math.floor(Math.random() * traits.length)];
    const secret = secrets[Math.floor(Math.random() * secrets.length)];

    const result = `
      <strong>👤 Имя:</strong> ${name}<br>
      <strong>🧝‍♂️ Раса:</strong> ${race}<br>
      <strong>💼 Роль:</strong> ${role}<br>
      <strong>🎭 Черта:</strong> ${trait}<br>
      <strong>🤫 Секрет:</strong> ${secret}
    `;
    document.getElementById("npc-result").innerHTML = result;
  }
</script>
