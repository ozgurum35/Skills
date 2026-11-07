# Proje Notları

## Güncel durum

- Kişisel Claude Code skill koleksiyonu; skill'ler `.claude/skills/`, alt ajanlar `.claude/agents/` altında.
- Kurulu: ui-ux-pro-max 2.15.0 (+ design, design-system, brand, slides, banner-design, ui-styling), karpathy-guidelines, superpowers'tan 4 skill (v7.0.2). Kaynak sürümleri `UPSTREAM.json`'da.
- ui-ux-pro-max kaynakta da 2.15.0 (2026-11-07 kontrolü); `search.py` bu oturumda çalıştırılıp doğrulandı.
- Anayasa: `docs/anayasa.md` = sürüm 2.6, claude.ai tercihleriyle aynı.
- Bulut ortamı kurulum betiği skill'leri her oturumda `~/.claude/` altına kopyalıyor.

## Kararlar

- Skill betik yolları `${CLAUDE_SKILL_DIR}` ile yazılır (plugin olmadan, her projede çalışsın).
- Kaynaklardaki `tests/` klasörleri alınmaz.
- superpowers'ın oturum başı hook'u ve `using-superpowers` alınmadı (her yanıtta skill çağırmayı zorunlu kılıyor, token maliyeti yüksek).
- Kaynak güncellemesi: haftalık workflow yalnızca issue açar; güncellemeyi "skill'leri güncelle" denince Claude Code yapar (inceleme + `CLAUDE_SKILL_DIR` düzeltmesi + test).
- `kod-tarayici` alt ajanı Haiku ile, salt okunur.

## Başarısız / alınmayan yöntemler

- (henüz yok)

## Açık işler

- (henüz yok)
