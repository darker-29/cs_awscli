# CloudFormation
## ドキュメント
https://docs.aws.amazon.com/cli/latest/reference/cloudformation/index.html


## コマンド

### スタック操作
- deploy

```shell
aws cloudformation deploy \
--stack-name スタック名 \
--template-file ファイル名 \
--parameter-overrides Key=Value \
Key=Value
```

<br>

- list-stacks

```shell
aws cloudformation list-stacks
```

<br>

- delete-stack

```shell
aws cloudformation delete-stack \
--stack-name スタック名
```

<br>

- describe-stack

```shell
aws cloudformation describe-stack \
--stack-name スタック名
```


<br>
<br>


### 変更セット操作

- create-change-set

```shell
aws cloudformation create-change-set \
--stack-name スタック名 \
--template-file ファイル名 \
--parameters ParameterKey=Key,ParameterValue=value \
ParameterKey=Key,ParameterValue=value \
--change-set-name 変更セット名

```

<br>

- describe-change-set

```shell
aws cloudformation describe-change-set \
--stack-name スタック名 \
--change-set-name 変更セット名
```

<br>

- execute-change-set

```shell
aws cloudformation execute-change-set \
--stack-name スタック名 \
--change-set-name 変更セット名
```

<br>
<br>

### テンプレートの構文チェック

- validate-template

```shell
aws cloudformation validate-template \ 
--template-body file:///
```


### スタックの削除保護有効・無効

- 削除保護の有効化

```shell
aws cloudformation update-termination-protection \
--stack-name スタック名 \
--enable-termination-protection
```

<br>


- 削除保護の無効化
```shell
aws cloudformation update-termination-protection \
--stack-name スタック名 \
--no-enable-termination-protection
```
