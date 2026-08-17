# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **820.5 ms**
- Average token reduction vs full source context: **1.6%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.3 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| G06 | long_term | PASS | 1134.6 | 849 | 0.0% |  |
| G09 | semantic | PASS | 208.4 | 644 | 0.0% |  |
| G10 | semantic | PASS | 202.8 | 496 | 0.0% |  |
| G14 | mixed | PASS | 1336.2 | 581 | 0.0% |  |
| G03 | long_term | PASS | 1065.0 | 1401 | 0.0% |  |
| G04 | long_term | PASS | 1142.2 | 1397 | 0.0% |  |
| G07 | episodic | PASS | 218.9 | 461 | 0.0% |  |
| G08 | episodic | PASS | 215.0 | 457 | 0.0% |  |
| G11 | mixed | PASS | 1314.3 | 581 | 0.0% |  |
| G13 | mixed | PASS | 403.6 | 500 | 11.5% |  |
| G15 | mixed | PASS | 1588.6 | 831 | 0.0% |  |
| G16 | mixed | PASS | 1328.2 | 581 | 0.0% |  |
| G17 | mixed | PASS | 1337.8 | 581 | 0.0% |  |
| G18 | mixed | PASS | 421.9 | 500 | 11.5% |  |
| G19 | mixed | PASS | 1323.1 | 581 | 0.0% |  |
| G05 | long_term | PASS | 576.3 | 634 | 0.0% |  |
| G12 | mixed | PASS | 1291.4 | 581 | 8.1% |  |
| G20 | mixed | PASS | 1301.7 | 756 | 0.0% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G06 - long_term

`LOCAL_USER_MEMORY [lan-s1]: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend. <USER_SUMMARY> Lan's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python.  Lan prefers to use Java and Spring Boot for backend development and explicitly avoids using Python in this context. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOT`

### G09 - semantic

`LOCAL_SEMANTIC [kb-payment-retry]: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. LOCAL_SEMANTIC [kb-context-budget]: Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodic 3 percent, semantic 3 percent; trim lower-priority memory first. Marker: BUDGET-10-4-3-3. LOCAL_SEMANTIC [kb-memory-privacy]: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. LOCAL_SEMANTIC [kb-async-http`

### G10 - semantic

`LOCAL_SEMANTIC [kb-context-budget]: Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodic 3 percent, semantic 3 percent; trim lower-priority memory first. Marker: BUDGET-10-4-3-3. LOCAL_SEMANTIC [kb-payment-retry]: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. LOCAL_SEMANTIC [kb-async-http]: When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST. `

### G14 - mixed

`<LONG_TERM> LOCAL_USER_MEMORY [lan-s1]: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend. <USER_SUMMARY> Lan's project is LOTUS-88. They prioritize Java and Spring Boot for backend development and do not use Python.  Lan prefers to use Java and Spring Boot for backend development and explicitly avoids using Python in this context. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cu`

### G03 - long_term

`LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. LOCAL_USER_MEMORY [minh-s1]: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. LOCAL_USER_MEMORY [mi`

### G04 - long_term

`LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s1]: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s2]: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat conc`

### G07 - episodic

`LOCAL_EPISODE [minh-s2]: user: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. assistant: Hay kiem tra connection pool, lifecycle cua client va concurrency. user: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. assistant: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. LOCAL_EPISODE [minh-s1]: user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tran`

### G08 - episodic

`LOCAL_EPISODE [minh-s1]: user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. LOCAL_EPISODE [minh-s2]: user: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. assistant: Hay kiem tra connection pool, lifecycle cua client va co`

### G11 - mixed

`<LONG_TERM> LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. LOCAL_USER_MEMORY [minh-s1]: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. LOCAL_USE`

### G13 - mixed

`<EPISODIC> LOCAL_EPISODE [minh-s1]: user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. LOCAL_EPISODE [minh-s2]: user: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. assistant: Hay kiem tra connection pool, lifecycle cua c`

### G15 - mixed

`<LONG_TERM> LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s2]: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. LOCAL_USER_MEMORY [minh-`

### G16 - mixed

`<LONG_TERM> LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s1]: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich ba`

### G17 - mixed

`<LONG_TERM> LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s1]: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co A`

### G18 - mixed

`<EPISODIC> LOCAL_EPISODE [minh-s1]: user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. LOCAL_EPISODE [minh-s2]: user: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. assistant: Hay kiem tra connection pool, lifecycle cua c`

### G19 - mixed

`<LONG_TERM> LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s2]: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. LOCAL_USER_MEMORY [minh-`

### G05 - long_term

`LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. LOCAL_USER_MEMORY [minh-s1]: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline.`

### G12 - mixed

`<LONG_TERM> LOCAL_USER_MEMORY [minh-s3]: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHID-27. LOCAL_USER_MEMORY [minh-s1]: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. LOCAL_USER_MEMORY [minh-s2]: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. LOCAL_USER_MEMORY [minh-s1]: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. LOCAL_USE`

### G20 - mixed

`<SHORT_TERM> <SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Filler about dashboard widgets. | assistant: Filler. | user: Filler about CSS variables. | assistant: Filler. | user: Filler about copy review. | assistant: Filler. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler about empty charts. assistant: Filler. user: Filler about telemetry. assistant: Filler. user: Filler about a11y labels. assistant: Filler. </RECENT_TURNS> </SHORT_TERM>`
