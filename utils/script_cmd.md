
移除檔案中 ｀[cite_start]` 字串的指令
```
sed -i '' 's/\[cite_start\]//g' ${filename}

```

移除檔案內容中 `[cite: 43]` 字串的指令

```
sed -i '' 's/\[cite: [0-9, ]*\]//g' ${filename}

```

移除檔案內容中 `[46]` 字串的指令，
sed -i '' 's/\[[0-9, ]*\]//g' ${filename}

