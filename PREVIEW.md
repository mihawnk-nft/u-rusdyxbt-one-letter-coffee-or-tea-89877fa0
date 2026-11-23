# Preview — One Letter: Coffee or Tea

- **Bounty:** [u-rusdyxbt-one-letter-coffee-or-tea-89877fa0](https://make.fun/bounty/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0) — Growth, $5 (1st $2, 2nd $2, 3rd $1), gratis
- **Deadline:** 2026-11-24T22:45:00Z (05:45 WIB, 25 Nov 2026)
- **Entry:** satu huruf **`A`** (kopi) di `/output/entry.txt` — tepat 1 byte, tanpa newline
- **Program:** `main.py`, pure Python stdlib, tanpa network, tanpa baca file

## Kenapa A (kopi), bukan B (teh)

Diuji langsung ke model juri (z-ai/glm-5.3-flash, sesuai RULES), dua arah:

| Call | Verdict | Margin |
|------|---------|--------|
| A vs B | A (kopi) | 2 |
| B vs A | B = A (kopi) | 2 |

Skor game kopi **0,70** — menang di kedua urutan. Alasan juri: "A" terbaca berani, gelap, dan pasti — seperti satu shot espresso — sementara "B" (teh) lebih lembut dan kalah hidup.

## Status

- [x] Kit diunduh & RULES dibaca
- [x] `main.py` ditulis & dites lokal (tulis `A`, 1 byte, round-trip lolos)
- [x] Repo GitHub dibuat & dipush (commit `1be8acf`, dibuat 2026-11-23T22:58:20Z — setelah buka 22:50:01Z)
- [x] Kit check: 4 pass (competition_open, snapshot, license_osi, entrypoint); 1 fail = `transcripts_present` (bundle belum dibuat — lihat catatan)
- [ ] Submit — MENUNGGU lampu hijau user (tidak dilakukan dari run ini)

## Catatan transcripts (penting sebelum submit)

Kit check gagal HANYA di `transcripts_present`: bundle transcripts harus dibuat
oleh agen top-level SETELAH subagent ini selesai, karena usage row sesi subagent
ini baru ditulis saat run-nya selesai. Perintahnya (dari dalam kit):

```
node cli/makefun.mjs bundle --repo ~/workspace/makefun/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0-dev --system-prompt ~/workspace/system/system_prompt.md --effort default --out transcripts.tar.gz --muse-usage <usage-rows-dari-muse.db>
```

lalu `check` ulang dengan `--transcripts transcripts.tar.gz` sampai lolos penuh.
