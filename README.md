Q: What would happen if in LimitWorker we had four BlinkWorkers but only two tokens?
A: 這個程式裡，共有 4 個 BlinkWorker，但 Semaphore 只有 2 個 token。因此同一時間只能有 2 個 Worker 執行，其餘 2 個 Worker 會被阻擋，直到有 token 被釋放後才能繼續執行。這個機制可限制同時執行的 Task 數量，達到資源控管的效果。
<img width="2826" height="332" alt="image" src="https://github.com/user-attachments/assets/d7a9f043-daa4-4aea-ab9a-045a52ed5ddf" />
# OS-5
