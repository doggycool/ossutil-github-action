# GitHub actions for aliyun OSS toolkit

![CI for ossutil github action](https://github.com/doggycool/ossutil-github-action/workflows/CI%20for%20ossutil%20github%20action/badge.svg)

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
