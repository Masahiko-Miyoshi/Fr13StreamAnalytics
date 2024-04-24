# Fr13StreamAnalytics ローカルでのクエリー編集手順

1．本リポジトリーのクローンを作成（例：projects/Fr13StreamAnalytics)  
2．VScodeでローカルフォルダ（projects/Fr13StreamAnalytics）を開く  
3. ルートに配置されているTransformation.asaqlがクエリーファイルになるので、編集する  
4．編集画面上部に位置する「Submit to azure]をクリックするとAzureにアップロードします

<img width="584" alt="image" src="https://github.com/Otsuka-Electronics/Fr13StreamAnalytics/assets/138413956/6fd7a1f0-e2ab-4c25-b415-2fb7baaecefb">

5. エラーが出る場合があるが、アップロードは完了できている　<＝何回か繰り返すとエラーが発生しなくなる

# Fr13StreamAnalytics ローカルでの出力（Outputs）追加
1. エディタ上で他のoutputsファイルを参考にして複製を作成し、適切なファイル名で保存する
2. 以下のコードにおいて、”Name”プロパティを編集する。このプロパティが出力エイリアス名に相当する。
 ```
   {
    "Name": "tFileBackup",
    "DataSourceType": "SQL Database",
    "SQLDatabaseProperties": {
        "Database": "FR13SqlDatabase",
        "Server": "fr13-sql-database-server",
        "User": "otsuka",
        "Password": "********",
        "Table": "t_file_backup",
        "MaxWriterCount": 1,
        "MaxBatchCount": 10000,
        "AuthenticationMode": "ConnectionString"
    },
    "DataSourceCredentialDomain": "f4298651-6f61-4f5f-8069-5056c64a0280.StreamAnalystics",
    "ScriptType": "Output"
}
```
3．編集画面上部に位置する「Submit to azure]をクリックするとAzureにアップロードします  

<img width="584" alt="image" src="https://github.com/Otsuka-Electronics/Fr13StreamAnalytics/assets/138413956/6fd7a1f0-e2ab-4c25-b415-2fb7baaecefb">

④. エラーが出る場合があるが、アップロードは完了できている　<＝何回か繰り返すとエラーが発生しなくなる

