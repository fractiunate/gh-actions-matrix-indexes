# gh-actions-matrix-indexes
POC to get indexes by matrix strategy list entries


```bash
curl --location --request POST 'https://api.github.com/repos/{{owner}}/{{repo}}/dispatches' \
--header 'Authorization: Bearer {{PERSONAL_ACCESS_TOKEN}}' \
--header 'Content-Type: application/json' \
--data-raw '{
  "event_type": "test run",
  "client_payload": {
    "services": [
        "cat",
        "dog",
        "bird",
        "hamster"
    ],
    "versions": [2,4,6,8]
  }
}'
```


## REF
- https://thekevinwang.com/2021/09/19/github-actions-dynamic-matrix/ (base for this example)
- https://hanxiao.io/2021/01/24/Speedup-CI-Workflow-in-Github-Actions-via-Strategy-Matrix/ (dynamic directories to matrix jobs)