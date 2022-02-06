# CloudFormation
## ドキュメント
https://docs.aws.amazon.com/cli/latest/reference/cloudformation/index.html


## コマンド

### スタック操作
- create-stack

```shell
aws cloudformation create-stack \
--stack-name スタック名 \
--template-body file:/// \
--parameters ParameterKey=Key,ParameterValue=value \
ParameterKey=Key,ParameterValue=value
```

<br>

- update-stack

```shell
aws cloudformation update-stack \
--stack-name スタック名 \
--template-body file:/// \
--parameters ParameterKey=Key,ParameterValue=value \
ParameterKey=Key,ParameterValue=value
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
--template-body file:/// \
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

