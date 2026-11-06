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
| karpathy-guidelines | [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) @ `64723a4` | MIT (SKILL.md ve kaynak README'de belirtilmiş; kaynakta ayrı lisans dosyası yok) |

## Kaynaktan yapılan değişiklikler

- `ui-ux-pro-max/SKILL.md`: `${CLAUDE_PLUGIN_ROOT}/.claude/skills/ui-ux-pro-max` yolları `${CLAUDE_SKILL_DIR}` ile değiştirildi (plugin olmadan da çalışsın diye).
- `tests/` klasörleri çıkarıldı.
- `design`, `design-system`, `brand`, `ui-styling` SKILL.md: göreli `scripts/...` komut yolları `"${CLAUDE_SKILL_DIR}/scripts/..."` yapıldı (skill başka projede kullanılırken de çalışsın diye).

## Dış bağlantı kuran betikler (bilgi)

- `design/scripts/logo/generate.py`, `design/scripts/icon/generate.py`: Görsel üretimi için Gemini / AtlasCloud / MuAPI'ye istek atar. API anahtarını ortam değişkeninden veya `.env` dosyasından okur. Anahtar yoksa çalışmaz. **`.env` dosyasını asla commit etme.**
- `design-system/scripts/fetch-background.py`: Pexels görsel bağlantıları üretir.
- `ui-styling/scripts/shadcn_add.py`: Projede `npx shadcn` komutunu çalıştırır.
- `brand/scripts/sync-brand-to-tokens.cjs`: Yerel token üretim betiğini `node` ile çalıştırır.

## Güncellemeler

- Kurulu kaynak sürümleri `UPSTREAM.json` dosyasında tutulur.
- `.github/workflows/upstream-check.yml` her pazartesi `UPSTREAM.json` içindeki tüm kaynakları kontrol eder; değişiklik varsa **issue açar**. Kod kopyalamaz, dosya değiştirmez.
  - `track: version`: kaynaktaki sürüm numarası karşılaştırılır (ui-ux-pro-max).
  - `track: commit`: skill klasörüne gelen son commit karşılaştırılır (karpathy-guidelines; kaynak sürüm numarasını güncellemiyor).
- Yeni kaynak eklerken `UPSTREAM.json` içindeki `sources` listesine bir kayıt eklenir.
- Issue gelince Claude Code'a "skill'leri güncelle" denir: yeni sürüm indirilir, değişen betikler incelenir, `CLAUDE_SKILL_DIR` düzeltmesi yeniden uygulanır, test edilir, `UPSTREAM.json` güncellenir ve gönderilir.
- Elle tetikleme: Actions → "Kaynak sürüm kontrolü" → Run workflow.

## Diğer

- `.claude/agents/kod-tarayici.md`: Haiku ile çalışan salt okunur kod tarama alt ajanı.
- `docs/anayasa.md`: Kişisel çalışma anayasasının güncel sürümü (claude.ai tercihlerine yapıştırılan metnin kopyası).

## Kişisel bilgisayara kurulum

```bash
git clone https://github.com/ozgurum35/Skills.git
cp -r Skills/.claude/skills/* ~/.claude/skills/
```
