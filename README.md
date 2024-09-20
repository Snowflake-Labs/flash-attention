## About
Fork of https://github.com/vllm-project/flash-attention. Daily changes should be pushed to the corvo branch.

## Sync from head

We keep track of the `main` branch of https://github.com/vllm-project/flash-attention.git in the `vllm` branch in https://github.com/Snowflake-Labs/flash-attention.git.

To sync from head, run below.

```
git branch -D main 2>/dev/null 
git checkout -b main
git remote set-url origin https://github.com/vllm-project/flash-attention.git
git fetch origin main
git reset --hard origin/main
git remote set-url origin https://github.com/Snowflake-Labs/flash-attention.git
git branch -D vllm
git branch -m vllm
git checkout origin/corvo README.md
git push origin HEAD
```
