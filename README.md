# actions-demo

## based on node-demo

```bash
COVERALLS_REPO_TOKEN=0wCesQawgGWGdAPPL2KzS5lN6JjZSud5q COVERALLS_ENDPOINT=http://localhost:3000 make test-coveralls
```

Actually:

```bash
Secrets.GITHUB_TOKEN COVERALLS_ENDPOINT=http://1234567.ngrok.com make test-coveralls
```

Format:

```yaml
steps:
  - name: Coveralls
      uses: ./.github/coveralls-action
      env:
        NODE_COVERALLS_DEBUG: 1
      with:
        github-token: ${{ secrets.github_token }}
        parallel: true
        flag-name: run-${{ matrix.test_number }}
        # coveralls-endpoint: https://coveralls.ngrok.io
        # env:
        #   COVERALLS_DEBUG: 1
        #   NODE_COVERALLS_DEBUG: 1
```
