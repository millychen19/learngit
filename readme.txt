��ѩ��git�̳� ѧϰ����ժ��

Git is a version control system.
Git is free software.

ʲô�ǰ汾���أ��汾�������ֿ⣬Ӣ����repository������Լ�����һ��Ŀ¼�����Ŀ¼����������ļ������Ա�Git����������ÿ���ļ����޸ġ�ɾ����Git���ܸ��٣��Ա��κ�ʱ�̶�����׷����ʷ�������ڽ���ĳ��ʱ�̿��ԡ���ԭ����

���ԣ�����һ���汾��ǳ��򵥣����ȣ�ѡ��һ�����ʵĵط�������һ����Ŀ¼��

$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit

�ڶ�����ͨ��git init��������Ŀ¼���Git���Թ���Ĳֿ⣺

$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/

����һ���ļ��ŵ�Git�ֿ�ֻ��Ҫ������

��һ����������git add����Git�����ļ���ӵ��ֿ⣺

$ git add readme.txt
ִ����������û���κ���ʾ����Ͷ��ˣ�Unix����ѧ�ǡ�û����Ϣ���Ǻ���Ϣ����˵����ӳɹ���

�ڶ�����������git commit����Git�����ļ��ύ���ֿ⣺
$ git commit -m "wrote a readme file"
�򵥽���һ��git commit���-m����������Ǳ����ύ��˵�������������������ݣ���Ȼ�����������ģ���������ܴ���ʷ��¼�﷽����ҵ��Ķ���¼��

ΪʲôGit����ļ���Ҫadd��commitһ�������أ���Ϊcommit����һ���ύ�ܶ��ļ�����������Զ��add��ͬ���ļ������磺

$ git add file1.txt
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."
���ѽ��
Q������git add readme.txt���õ�����fatal: not a git repository (or any of the parent directories)��
A��Git���������Git�ֿ�Ŀ¼��ִ�У�git init���⣩���ڲֿ�Ŀ¼��ִ����û������ġ�
Q������git add readme.txt���õ�����fatal: pathspec 'readme.txt' did not match any files��
A�����ĳ���ļ�ʱ�����ļ������ڵ�ǰĿ¼�´��ڣ���ls����dir����鿴��ǰĿ¼���ļ��������ļ��Ƿ���ڣ������Ƿ�д�����ļ�����

С��
�����ܽ�һ�½���ѧ���������ݣ�
��ʼ��һ��Git�ֿ⣬ʹ��git init���
����ļ���Git�ֿ⣬��������

ʹ������git add <file>��ע�⣬�ɷ������ʹ�ã���Ӷ���ļ���
ʹ������git commit -m <message>����ɡ�

�޸�readme�ļ������ڣ�����git status����������
$ git status
git status�������������ʱ�����ղֿ⵱ǰ��״̬���������������������ǣ�readme.txt���޸Ĺ��ˣ�����û��׼���ύ���޸ġ�

git log����鿴��

$ git log

��HEAD��ʾ��ǰ�汾��Ҳ�������µ��ύ1094adb...��ע���ҵ��ύID����Ŀ϶���һ��������һ���汾����HEAD^������һ���汾����HEAD^^����Ȼ����100���汾д100��^�Ƚ�������������������д��HEAD~100��

���ڣ�����Ҫ�ѵ�ǰ�汾append GPL���˵���һ���汾add distributed���Ϳ���ʹ��git reset���

$ git reset --hard HEAD^

�����Լ������˵���һ���汾wrote a readme file��������������������git log�ٿ������ڰ汾���״̬��

$ git log
commit e475afc93c209a690c39c13a46716e8fa000c366 (HEAD -> master)
Author: Michael Liao <askxuefeng@gmail.com>
Date:   Fri May 18 21:03:36 2018 +0800

    add distributed

commit eaadf4e385e865d25c48e7ca9c8395c3f7dfaef0
Author: Michael Liao <askxuefeng@gmail.com>
Date:   Fri May 18 20:59:18 2018 +0800

    wrote a readme file
���µ��Ǹ��汾append GPL�Ѿ��������ˣ��ñ����21������ʱ�⴩���������19���ͣ����ٻ�ȥ�Ѿ��ز�ȥ�ˣ���ô�죿

�취��ʵ�����еģ�ֻҪ����������д��ڻ�û�б��ص�����Ϳ���˳�������Ұ��Ұ����ҵ��Ǹ�append GPL��commit id��1094adb...�����ǾͿ���ָ���ص�δ����ĳ���汾��

$ git reset --hard 1094a
HEAD is now at 83b0afe append GPL

��Git�У������к��ҩ���ԳԵġ�������$ git reset --hard HEAD^���˵�add distributed�汾ʱ������ָ���append GPL���ͱ����ҵ�append GPL��commit id��Git�ṩ��һ������git reflog������¼���ÿһ�����

$ git reflog
e475afc HEAD@{1}: reset: moving to HEAD^
1094adb (HEAD -> master) HEAD@{2}: commit: append GPL
e475afc HEAD@{3}: commit: add distributed
eaadf4e HEAD@{4}: commit (initial): wrote a readme file
�������˿������������֪��append GPL��commit id��1094adb�����ڣ����ֿ��Գ���ʱ����ص�δ���ˡ�


С��
�����ܽ�һ�£�
HEADָ��İ汾���ǵ�ǰ�汾����ˣ�Git���������ڰ汾����ʷ֮�䴩��ʹ������git reset --hard commit_id��
����ǰ����git log���Բ鿴�ύ��ʷ���Ա�ȷ��Ҫ���˵��ĸ��汾��
Ҫ�ط�δ������git reflog�鿴������ʷ���Ա�ȷ��Ҫ�ص�δ�����ĸ��汾��

�汾�⡢head��master���ݴ����ȸ��
https://www.liaoxuefeng.com/wiki/896043488029600/897271968352576

�汾�⣨Repository��
��������һ������Ŀ¼.git��������㹤����������Git�İ汾�⡣
Git�İ汾������˺ܶණ������������Ҫ�ľ��ǳ�Ϊstage�����߽�index�����ݴ���������GitΪ�����Զ������ĵ�һ����֧master���Լ�ָ��master��һ��ָ���HEAD��

ǰ�潲�����ǰ��ļ���Git�汾������ӵ�ʱ���Ƿ�����ִ�еģ�
��һ������git add���ļ���ӽ�ȥ��ʵ���Ͼ��ǰ��ļ��޸���ӵ��ݴ�����
�ڶ�������git commit�ύ���ģ�ʵ���Ͼ��ǰ��ݴ��������������ύ����ǰ��֧��
��Ϊ���Ǵ���Git�汾��ʱ��Git�Զ�Ϊ���Ǵ�����Ψһһ��master��֧�����ԣ����ڣ�git commit������master��֧���ύ���ġ�
����Լ����Ϊ����Ҫ�ύ���ļ��޸�ͨͨ�ŵ��ݴ�����Ȼ��һ�����ύ�ݴ����������޸ġ�


����Է��֣�Git������㣬git checkout -- file���Զ������������޸ģ�

$ git checkout -- readme.txt
����git checkout -- readme.txt��˼���ǣ���readme.txt�ļ��ڹ��������޸�ȫ�����������������������
һ����readme.txt���޸ĺ�û�б��ŵ��ݴ��������ڣ������޸ľͻص��Ͱ汾��һģһ����״̬��
һ����readme.txt�Ѿ���ӵ��ݴ������������޸ģ����ڣ������޸ľͻص���ӵ��ݴ������״̬��
��֮������������ļ��ص����һ��git commit��git addʱ��״̬��

git checkout -- file�����е�--����Ҫ��û��--���ͱ���ˡ��л�����һ����֧������������ں���ķ�֧�����л��ٴ�����git checkout���



Gitͬ���������ǣ�������git reset HEAD <file>���԰��ݴ������޸ĳ�������unstage�������·Żع�������

$ git reset HEAD readme.txt
Unstaged changes after reset:
M	readme.txt
git reset����ȿ��Ի��˰汾��Ҳ���԰��ݴ������޸Ļ��˵�����������������HEADʱ����ʾ���µİ汾��

����git status�鿴һ�£������ݴ����Ǹɾ��ģ����������޸ģ�

���ǵ���ζ������������޸���

$ git checkout -- readme.txt

�������������徲�ˣ�


С��
�ֵ���С��ʱ�䡣

����1����������˹�����ĳ���ļ������ݣ���ֱ�Ӷ������������޸�ʱ��������git checkout -- file��

����2�����㲻�������˹�����ĳ���ļ������ݣ�����ӵ����ݴ���ʱ���붪���޸ģ�����������һ��������git reset HEAD <file>���ͻص��˳���1���ڶ���������1������

����3���Ѿ��ύ�˲����ʵ��޸ĵ��汾��ʱ����Ҫ���������ύ���ο��汾����һ�ڣ�����ǰ����û�����͵�Զ�̿⡣

ɾ���ļ���
https://www.liaoxuefeng.com/wiki/896043488029600/900002180232448
ɾ����������
$ rm test.txt
�ݴ���ɾ����
$ git rm test.txt
�ύɾ�����ļ��Ӱ汾����ɾ��
$ git commit -m "remove"

ɾ���ˣ��Ӱ汾��ָ��ļ���
$ git checkout -- test.txt

git checkout��ʵ���ð汾����İ汾�滻�������İ汾�����۹��������޸Ļ���ɾ���������ԡ�һ����ԭ����

С��
����git rm����ɾ��һ���ļ������һ���ļ��Ѿ����ύ���汾�⣬��ô����Զ���õ�����ɾ������ҪС�ģ���ֻ�ָܻ��ļ������°汾����ᶪʧ���һ���ύ�����޸ĵ����ݡ�

��1��������SSH Key�����û���Ŀ¼�£�������û��.sshĿ¼������У��ٿ������Ŀ¼����û��id_rsa��id_rsa.pub�������ļ�������Ѿ����ˣ���ֱ��������һ�������û�У���Shell��Windows�´�Git Bash��������SSH Key��

$ ssh-keygen -t rsa -C "youremail@example.com"

���һ��˳���Ļ����������û���Ŀ¼���ҵ�.sshĿ¼��������id_rsa��id_rsa.pub�����ļ�������������SSH Key����Կ�ԣ�id_rsa��˽Կ������й¶��ȥ��id_rsa.pub�ǹ�Կ�����Է��ĵظ����κ��ˡ�

��2������½GitHub���򿪸�������ҳ��ѡ������SSHKey�Ĳ˵�������sshkey��������key���ƹ�Կ��


��github���½�Զ�ֿ̲�

����Զ�ֿ̲�
$ git remote add origin git@github.com:millychen19/learngit.git

�ѱ��ؿ�������������͵�Զ�̿��ϣ�
$ git push -u origin master
�ѱ��ؿ���������͵�Զ�̣���git push���ʵ�����ǰѵ�ǰ��֧master���͵�Զ�̡�

����Զ�̿��ǿյģ����ǵ�һ������master��֧ʱ��������-u������Git������ѱ��ص�master��֧�������͵�Զ���µ�master��֧������ѱ��ص�master��֧��Զ�̵�master��֧�������������Ժ�����ͻ�����ȡʱ�Ϳ��Լ����

��������ֻҪ���������ύ���Ϳ���ͨ�����

$ git push origin master
�ѱ���master��֧�������޸�������GitHub�����ڣ����ӵ���������ķֲ�ʽ�汾�⣡

ɾ��Զ�̿�
�����ӵ�ʱ���ַд���ˣ����߾�����ɾ��Զ�̿⣬������git remote rm <name>���ʹ��ǰ����������git remote -v�鿴Զ�̿���Ϣ��

$ git remote -v
Ȼ�󣬸�������ɾ��������ɾ��origin��

$ git remote rm origin
�˴��ġ�ɾ������ʵ�ǽ���˱��غ�Զ�̵İ󶨹�ϵ��������������ɾ����Զ�̿⡣Զ�̿Ȿ��û���κθĶ���Ҫ����ɾ��Զ�̿⣬��Ҫ��¼��GitHub���ں�̨ҳ���ҵ�ɾ����ť��ɾ����


С��
Ҫ����һ��Զ�̿⣬ʹ������git remote add origin git@server-name:path/repo-name.git��

����һ��Զ�̿�ʱ�����Զ�̿�ָ��һ�����֣�origin��Ĭ��ϰ��������

������ʹ������git push -u origin master��һ������master��֧���������ݣ�

�˺�ÿ�α����ύ��ֻҪ�б�Ҫ���Ϳ���ʹ������git push origin master���������޸ģ�

�ֲ�ʽ�汾ϵͳ�����ô�֮һ���ڱ��ع�����ȫ����Ҫ����Զ�̿�Ĵ��ڣ�Ҳ������û������������������������SVN��û��������ʱ���Ǿܾ��ɻ�ģ����������ʱ���ٰѱ����ύ����һ�¾������ͬ��������̫�����ˣ�

С��
Ҫ��¡һ���ֿ⣬���ȱ���֪���ֿ�ĵ�ַ��Ȼ��ʹ��git clone�����¡��
$ git clone git@github.com:michaelliao/gitskills.git

Git֧�ֶ���Э�飬����https����sshЭ���ٶ���졣

https://www.liaoxuefeng.com/wiki/896043488029600/900003767775424

������ϲ���֧

���ȣ����Ǵ���dev��֧��Ȼ���л���dev��֧��
$ git checkout -b dev
git checkout�������-b������ʾ�������л����൱�������������
$ git branch dev
$ git checkout dev

Ȼ����git branch����鿴��ǰ��֧��
$ git branch
git branch������г����з�֧����ǰ��֧ǰ����һ��*��