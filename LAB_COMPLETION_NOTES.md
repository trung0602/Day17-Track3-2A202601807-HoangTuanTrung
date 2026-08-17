# Lab Completion Notes

## Checklist da lam

- [x] Doc README.md, LAB.md, VALIDATION.md va control_plane.
- [x] Hoan thien 4 ham trong `src/memory_student.py`.
- [x] Unit tests bang `.venv`: 11 passed, 1 skipped.
- [x] Smoke test Docker: Redis OK, Qdrant OK, dataset 11 evaluations, ZEP_API_KEY present.
- [x] Seed Zep thanh cong voi `ZEP_POLL_TIMEOUT=600`.
- [x] Demo short-term: durable note giu `REVIEW-DEADLINE-1600`, Friday, 16:00.
- [x] No-memory baseline: 2/11 PASS.
- [x] Student benchmark: 11/11 PASS, hit rate 100.0%.
- [x] Comparison report da tao: `reports/comparison.md`.
- [x] README_submission.md da tao, 284 tu.
- [x] Heartbeat dry-run va episodic maintenance da chay.
- [x] Privacy drill: delete + verify-only deu bao `Zep user absent: True`, Redis keys remaining 0.
- [x] Golden v3: copy `data/golden_eval_v3.json` -> `data/golden_eval.json`, chay `--golden` va dat 20/20 PASS.

## Luong chay chinh

1. Cai/chay local services: Redis va Qdrant qua Docker Compose.
2. Smoke test de kiem tra Redis, Qdrant, dataset va ZEP_API_KEY.
3. Seed dataset vao Zep:
   - user graph cho `minh-lab17` va `lan-lab17`;
   - standalone semantic graph cho domain KB.
4. Query benchmark di qua tung layer:
   - short-term local memory cho E01/E10;
   - long-term Context Block + edge facts cho E02/E03/E08/E09;
   - episodic user graph search cho E04/E05;
   - semantic standalone graph search cho E06/E11;
   - mixed assembly cho E07.
5. `ContextBudgetManager` ghep context theo thu tu short-term -> long-term -> episodic -> semantic voi budget 10/4/3/3.
6. Tao baseline no-memory, benchmark student va comparison report.
7. Chay privacy drill sau khi da luu benchmark.
8. Neu co golden v3, copy vao `data/golden_eval.json`, seed lai neu da forget user, roi chay golden benchmark.

## Luu y sau privacy

User-scoped memory cua `minh-lab17` da bi xoa. Neu can chay lai benchmark/golden/UI voi user Minh, seed lai truoc bang:

```bash
docker compose run --rm -e ZEP_POLL_TIMEOUT=600 app python -m src.seed
```
