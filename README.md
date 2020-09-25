# GitHub actions for aliyun OSS toolkit

> update/download/upload files from/to aliyun oss


## Inputs

### `ossArgs`
**Required** ossArgs to run ossutil command.

### `accessKey`
**Required** accessKey to authentication.

### `accessSecret`
**Required** accessSecret to authentication.

### `endpoint`
**Optional** endpoint to run ossutil command.


## Outputs

### `command`
the final command.

## Example usage

```yaml
uses: doggycool/ossutil-github-action@master
with:
    ossArgs: 'cp -r -u ./ oss://demo-bukcet/path/'
    accessKey: ${{ secrets.ALIYUN_ACCESS_KEY }}
    accessSecret: ${{ secrets.ALIYUN_ACCESS_SECRET }}
    endpoint: oss-cn-shanghai.aliyuncs.com
```
