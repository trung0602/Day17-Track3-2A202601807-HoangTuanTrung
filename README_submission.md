# Lab 17 Submission

## Ket qua

Student benchmark dat 11/11 PASS, hit rate 100.0%. No-memory baseline dat 2/11 PASS, chi qua short-term E01/E10; chen lech +9 case va +81.8 diem phan tram.

Layer quan trong nhat trong bo test nay la long-term/declarative memory vi no bao phu E02, E03, E08, E09 va gop evidence cho E07. E08 cho thay recency/scoping quan trong: BLUEBIRD-42 phai dung TypeScript/NestJS, trong khi Python chi con dung cho demo ca nhan ORCHID-27.

Khong co layer nao fail trong student run. Neu xet rui ro/chi phi, long-term la layer can theo doi nhat vi retrieve nhieu token nhat: E03 dung 1441 tokens, E08 dung 1430, E02 dung 1421. Case E07 la mixed case, can ket hop long-term preference cua Minh (`Python`) voi semantic policy cho payment retry (`Idempotency-Key`).

Average token reduction cua memory-enabled la 14.2%, no-memory la 81.8%. No-memory co reduction cao hon vi gan nhu retrieve rong, nhung hit rate thap; token reduction chi co y nghia khi evidence van dung.

Context Block/Zep phu hop cho user graph, cross-session facts, recency va provenance ma khong phai tu ghep Redis+Qdrant. Redis+Qdrant linh hoat, re hon va tot cho baseline/local control, nhung minh phai tu xu ly schema, ranking, invalidation, conflict va privacy deletion.

Guardrail chong memory poisoning: chi durable-write khi user opt-in, redact PII qua `privacy_guard`, khong ghi instruction/quyen moi tu memory, va can review high-impact preference update truoc write-back. Deletion request phai xoa user-scoped memory va verify tren moi store.

E10 compaction giu constraint `REVIEW-DEADLINE-1600`, Friday va 16:00 trong durable notes du raw turn cu bi evict. Buffer giu du lieu nhung token tang tuyen tinh; sliding + durable notes giu state/decision/TODO/constraint quan trong hon transcript day du.
