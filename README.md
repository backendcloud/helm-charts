# helm-charts

要开发一个app实例化的模块，时间特别紧，就没去部署harbor管理chart，直接托管github当chart仓库。

因为chart仓库只是一个HTTP服务，通过HTTP GET获取YAML文件和chart的压缩包，所以可以将这些文件存储在web服务器中，例如GCS、Amazon S3、GitHub Pages等。

做了app实例化的实例化，实例化终止(优雅/强制)，实例扩缩容，实例版本更新。
直接后台调用命令行
* helm install
* helm upgrade -f tt.yaml 文件里写上新的名称和扩缩容
* helm upgrade -f tt.yaml 文件里写上版本名称
* helm uninstall [--wait] [--timeout time]

选了个怎样快就怎样操作的方案，2天时间完成全部开发和调试。确实快。
