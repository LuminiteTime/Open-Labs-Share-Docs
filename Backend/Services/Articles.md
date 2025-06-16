### Зачем нужен
Articles Service является центральным хранилищем всех научных статей в системе. Он обеспечивает единую точку управления научным контентом и доступом к файловым ресурсам.

### Сохранение данных в S3

```text
Bucket:
article_id
	├── asset_file.extension
	├── example.png
	└── content.md
```

Link example: `...\bucket\article_id\filename`
