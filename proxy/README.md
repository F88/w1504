# 中継機

構成管理領域における拠点間中継機など、実現された IT BPR　における様々な中継機。

## インベントリ拠点間中継機
./inventory_proxy

### 説明
Ansible - CouchDB 間の通信を中継する。
実装は Varnish.

## 構成情報利用ユーザクエリ中継機
./userquery_proxy

### 説明
ユーザ端末 - CouchDB 間の通信を中継する。
実装は Varnish + vmod_ldap. 大きな範囲でのセキュリティ GW として機能する。

#### 補足
認証・認可の実体(正)は AD 連携した CouchDBの予定。
但し現時点では、CouchDB をローカルに閉じ込める Varnish セキュリティ・ラッパー側で認証・認可をコントロールする可能性がある。
