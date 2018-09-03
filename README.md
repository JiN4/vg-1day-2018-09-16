# setup

```
make up
```

# migration

## up

```
make migrate/up

Applied 2 migrations
```

`applied n migrations` みたいなメッセージが出れば成功しています。

## migration状態の確認

```
make migrate/status

+---------------------------------+-------------------------------+
|            MIGRATION            |            APPLIED            |
+---------------------------------+-------------------------------+
| 20180731131753-create_order.sql | 2018-09-03 11:03:43 +0000 UTC |
| 20180814154716-insert_data.sql  | 2018-09-03 11:03:43 +0000 UTC |
+---------------------------------+-------------------------------+
```

APPLIEDに日付が入ってればそこまで適用済み。noの場合は適用されていません。

# debug

以下でmysqlコンソールに入れます。
```
make debug
```

どうにもならなくなったら以下でDBを再作成してください。migration状態を全て吹っ飛ばしてイチからやり直せます。
```
make db/reset
```
