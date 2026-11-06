# Skills

Kişisel Claude Code skill koleksiyonu. Skill'ler `.claude/skills/` altında durur; bu repo bir oturuma eklendiğinde otomatik yüklenir.

## İçerik

| Skill | Kaynak | Lisans |
|---|---|---|
| ui-ux-pro-max | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) @ `b7d5353` | MIT (`LICENSE-ui-ux-pro-max`) |
| design | aynı repo | MIT |
| design-system | aynı repo | MIT |
| brand | aynı repo | MIT |
| slides | aynı repo | MIT |
| banner-design | aynı repo | MIT |
| ui-styling | aynı repo | Apache 2.0 (`.claude/skills/ui-styling/LICENSE.txt`) |

## Kaynaktan yapılan değişiklikler

- `ui-ux-pro-max/SKILL.md`: `${CLAUDE_PLUGIN_ROOT}/.claude/skills/ui-ux-pro-max` yolları `${CLAUDE_SKILL_DIR}` ile değiştirildi (plugin olmadan da çalışsın diye).
- `tests/` klasörleri çıkarıldı.

## Dış bağlantı kuran betikler (bilgi)

- `design/scripts/logo/generate.py`, `design/scripts/icon/generate.py`: Görsel üretimi için Gemini / AtlasCloud / MuAPI'ye istek atar. API anahtarını ortam değişkeninden veya `.env` dosyasından okur. Anahtar yoksa çalışmaz. **`.env` dosyasını asla commit etme.**
- `design-system/scripts/fetch-background.py`: Pexels görsel bağlantıları üretir.
- `ui-styling/scripts/shadcn_add.py`: Projede `npx shadcn` komutunu çalıştırır.
- `brand/scripts/sync-brand-to-tokens.cjs`: Yerel token üretim betiğini `node` ile çalıştırır.

## Güncellemeler

- Kurulu kaynak sürüm `UPSTREAM.json` dosyasında tutulur.
- `.github/workflows/upstream-check.yml` her pazartesi kaynak repoyu kontrol eder; yeni sürüm varsa **issue açar**. Kod kopyalamaz, dosya değiştirmez.
- Issue gelince Claude Code'a "skill'leri güncelle" denir: yeni sürüm indirilir, değişen betikler incelenir, `CLAUDE_SKILL_DIR` düzeltmesi yeniden uygulanır, test edilir, `UPSTREAM.json` güncellenir ve gönderilir.
- Elle tetikleme: Actions → "Kaynak sürüm kontrolü" → Run workflow.

## Kişisel bilgisayara kurulum

```bash
git clone https://github.com/ozgurum35/Skills.git
cp -r Skills/.claude/skills/* ~/.claude/skills/
```
