# 問題9 「レプリケーションが出来ない!」

出題大会: ICTSC6

出題時間: 2日目午前

問題技術: MySQL replication

点数: 20点満点

### 問題文

とある企業にてWebサイトの構築を行う業務があった。Aさんはデータベース周りの設定を担当していたが、初めてのレプリケーション設定と慣れないMYSQLの為悪戦苦闘していた。

納期が迫る中、Aさんは私事でどうしても本国に帰らないと行けなくなってしまった。試行錯誤が垣間見えるconfigを元にレプリケーションの設定を完了して欲しい。

![トポロジ](http://i0.wp.com/icttoracon.net/tech-blog/wp-content/uploads/2016/09/problem-09.png?resize=768%2C504)

[ICTSC tech blog - ICTSC6 全問題の解説](http://icttoracon.net/tech-blog/2016/09/23/ictsc6-problems-explanation/) からコピー

### 環境

#### 構成情報
* Master
  - CentOS 6.8
  - IP: 192.168.11.3
* Slave
  - CentOS 6.8
  - IP: 192.168.11.4

### 使い方

#### Vagrant

```
$ git clone https://github.com/naoki912/ictsc-past-questions.git
$ cd ictsc-past-questions/ictsc6-q9/vagrant
$ vagrant up

$ vagrant ssh master
$ vagrant ssh slave
```

#### Ansible

Ansibleを使用する際に、IPを変更したい場合はhostsファイルをいじってください。ただしIPを変更すると問題に影響が出るかもです。

```
$ cd ictsc-past-questions/ictsc6-q9/ansible
$ vim hosts
$ ansible-playbook -i hosts playbook.yml
```

### 注意点

* 部分点で10点しかもらえていなかったのでもしかしたら再現に足りない部分があるかも

### 解答

[Answer.md](Answer.md)

### 備考
* 使用した vagrant box
  - https://atlas.hashicorp.com/kaorimatz/boxes/centos-6.8-x86_64/
