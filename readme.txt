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


dev�޸��ļ�
���ڣ�dev��֧�Ĺ�����ɣ����ǾͿ����л���master��֧��
$ git checkout master
���ǰ�dev��֧�Ĺ����ɹ��ϲ���master��֧�ϣ�
$ git merge dev
git merge�������ںϲ�ָ����֧����ǰ��֧��
$ git merge dev

�ϲ���ɺ󣬾Ϳ��Է��ĵ�ɾ��dev��֧�ˣ�
$ git branch -d dev
ɾ���󣬲鿴branch����ֻʣ��master��֧�ˣ�
$ git branch

switch
����ע�⵽�л���֧ʹ��git checkout <branch>����ǰ�潲���ĳ����޸�����git checkout -- <file>��ͬһ��������������ã�ȷʵ�е������Ի�
ʵ���ϣ��л���֧�����������switch����ѧ����ˣ����°汾��Git�ṩ���µ�git switch�������л���֧��

�������л����µ�dev��֧������ʹ�ã�
$ git switch -c dev
ֱ���л������е�master��֧������ʹ�ã�
$ git switch master
ʹ���µ�git switch�����git checkoutҪ��������⡣

С��
Git��������ʹ�÷�֧��
�鿴��֧��git branch
������֧��git branch <name>
�л���֧��git checkout <name>����git switch <name>
����+�л���֧��git checkout -b <name>����git switch -c <name>
�ϲ�ĳ��֧����ǰ��֧��git merge <name>
ɾ����֧��git branch -d <name>

Creating a new branch is quick AND simple.

�����ͻ
https://www.liaoxuefeng.com/wiki/896043488029600/900004111093344

�ô�������git logҲ���Կ�����֧�ĺϲ������
$ git log --graph --pretty=oneline --abbrev-commit

С��
��Git�޷��Զ��ϲ���֧ʱ���ͱ������Ƚ����ͻ�������ͻ�����ύ���ϲ���ɡ�
�����ͻ���ǰ�Git�ϲ�ʧ�ܵ��ļ��ֶ��༭Ϊ����ϣ�������ݣ����ύ��
��git log --graph������Կ�����֧�ϲ�ͼ��

��֧�������
https://www.liaoxuefeng.com/wiki/896043488029600/900005860592480

��֧����
��ʵ�ʿ����У�����Ӧ�ð��ռ�������ԭ����з�֧����

���ȣ�master��֧Ӧ���Ƿǳ��ȶ��ģ�Ҳ���ǽ����������°汾��ƽʱ����������ɻ
�����ĸɻ��أ��ɻ��dev��֧�ϣ�Ҳ����˵��dev��֧�ǲ��ȶ��ģ���ĳ��ʱ�򣬱���1.0�汾����ʱ���ٰ�dev��֧�ϲ���master�ϣ���master��֧����1.0�汾��
������С�����ÿ���˶���dev��֧�ϸɻÿ���˶����Լ��ķ�֧��ʱ��ʱ����dev��֧�Ϻϲ��Ϳ����ˡ�

С��
Git��֧ʮ��ǿ�����Ŷӿ�����Ӧ�ó��Ӧ�á�
�ϲ���֧ʱ������--no-ff�����Ϳ�������ͨģʽ�ϲ����ϲ������ʷ�з�֧���ܿ��������������ϲ�����fast forward�ϲ��Ϳ����������������ϲ���


bug��֧
https://www.liaoxuefeng.com/wiki/896043488029600/900388704535136

Git���ṩ��һ��stash���ܣ����԰ѵ�ǰ�����ֳ������ء����������Ժ�ָ��ֳ������������
$ git stash
���ڣ���git status�鿴�����������Ǹɾ��ģ�������û�б�Git������ļ�������˿��Է��ĵش�����֧���޸�bug��

�޸���bug�л�dev��֧�ɻ�
git status�������Ǹɾ��ģ��ղŵĹ����ֳ��浽��ȥ�ˣ���git stash list�������
$ git stash list
stash@{0}: WIP on dev: f52c633 add merge

�����ֳ����ڣ�Git��stash���ݴ���ĳ���ط��ˣ�������Ҫ�ָ�һ�£��������취��
һ����git stash apply�ָ������ǻָ���stash���ݲ���ɾ��������Ҫ��git stash drop��ɾ����
��һ�ַ�ʽ����git stash pop���ָ���ͬʱ��stash����Ҳɾ�ˣ�
$ git stash pop
����git stash list�鿴���Ϳ������κ�stash�����ˣ�
$ git stash list
����Զ��stash���ָ���ʱ������git stash list�鿴��Ȼ��ָ�ָ����stash�������
$ git stash apply stash@{0}

Gitר���ṩ��һ��cherry-pick����������ܸ���һ���ض����ύ����ǰ��֧��
$ git cherry-pick 4c805e2

С��
�޸�bugʱ�����ǻ�ͨ�������µ�bug��֧�����޸���Ȼ��ϲ������ɾ����
����ͷ����û�����ʱ���Ȱѹ����ֳ�git stashһ�£�Ȼ��ȥ�޸�bug���޸�����git stash pop���ص������ֳ���
��master��֧���޸���bug����Ҫ�ϲ�����ǰdev��֧��������git cherry-pick <commit>�����bug�ύ���޸ġ����ơ�����ǰ��֧�������ظ��Ͷ���



С��
����һ����feature������½�һ����֧��
���Ҫ����һ��û�б��ϲ����ķ�֧������ͨ��git branch -D <name>ǿ��ɾ����


����Э��
https://www.liaoxuefeng.com/wiki/896043488029600/900375748016320
�����Զ�ֿ̲��¡ʱ��ʵ����Git�Զ��ѱ��ص�master��֧��Զ�̵�master��֧��Ӧ�����ˣ����ң�Զ�ֿ̲��Ĭ��������origin��

Ҫ�鿴Զ�̿����Ϣ����git remote��

$ git remote
origin
���ߣ���git remote -v��ʾ����ϸ����Ϣ��

$ git remote -v


ץȡ��֧

https://www.liaoxuefeng.com/wiki/896043488029600/900375748016320
�����С����Զ�̿�cloneʱ��Ĭ������£����С���ֻ�ܿ������ص�master��֧�����ſ�����git branch�������

$ git branch
* master
���ڣ����С���Ҫ��dev��֧�Ͽ������ͱ��봴��Զ��origin��dev��֧�����أ���������������������dev��֧��

$ git checkout -b dev origin/dev
���ڣ����Ϳ�����dev�ϼ����޸ģ�Ȼ��ʱ��ʱ�ذ�dev��֧push��Զ�̣�

$ git add env.txt
$ git commit -m "add env"
$ git push origin dev

���С����Ѿ���origin/dev��֧�����������ύ����������Ҳ��ͬ�����ļ������޸ģ�����ͼ���ͣ�
����ʧ�ܣ���Ϊ���С���������ύ������ͼ���͵��ύ�г�ͻ������취Ҳ�ܼ򵥣�Git�Ѿ���ʾ���ǣ�����git pull�����µ��ύ��origin/devץ������Ȼ���ڱ��غϲ��������ͻ�������ͣ�
$ git pull
git pullҲʧ���ˣ�ԭ����û��ָ������dev��֧��Զ��origin/dev��֧�����ӣ�������ʾ������dev��origin/dev�����ӣ�
$ git branch --set-upstream-to=origin/dev dev
��pull��
$ git pull
���git pull�ɹ������Ǻϲ��г�ͻ����Ҫ�ֶ����������ķ����ͷ�֧�����еĽ����ͻ��ȫһ����������ύ����push��

$ git commit -m "fix env conflict"
$ git push origin dev

��ˣ�����Э���Ĺ���ģʽͨ����������
���ȣ�������ͼ��git push origin <branch-name>�����Լ����޸ģ�
�������ʧ�ܣ�����ΪԶ�̷�֧����ı��ظ��£���Ҫ����git pull��ͼ�ϲ���
����ϲ��г�ͻ��������ͻ�����ڱ����ύ��
û�г�ͻ���߽������ͻ������git push origin <branch-name>���;��ܳɹ���
���git pull��ʾno tracking information����˵�����ط�֧��Զ�̷�֧�����ӹ�ϵû�д�����������git branch --set-upstream-to <branch-name> origin/<branch-name>��
����Ƕ���Э���Ĺ���ģʽ��һ����Ϥ�ˣ��ͷǳ��򵥡�

С��
�鿴Զ�̿���Ϣ��ʹ��git remote -v��
�����½��ķ�֧��������͵�Զ�̣��������˾��ǲ��ɼ��ģ�
�ӱ������ͷ�֧��ʹ��git push origin branch-name���������ʧ�ܣ�����git pullץȡԶ�̵����ύ��
�ڱ��ش�����Զ�̷�֧��Ӧ�ķ�֧��ʹ��git checkout -b branch-name origin/branch-name�����غ�Զ�̷�֧���������һ�£�
�������ط�֧��Զ�̷�֧�Ĺ�����ʹ��git branch --set-upstream branch-name origin/branch-name��
��Զ��ץȡ��֧��ʹ��git pull������г�ͻ��Ҫ�ȴ����ͻ��

С��
rebase�������԰ѱ���δpush�ķֲ��ύ��ʷ�����ֱ�ߣ�
rebase��Ŀ����ʹ�������ڲ鿴��ʷ�ύ�ı仯ʱ�����ף���Ϊ�ֲ���ύ��Ҫ�����Աȡ�
$ git rebase

������ǩ
https://www.liaoxuefeng.com/wiki/896043488029600/902335212905824
��Git�д��ǩ�ǳ��򵥣����ȣ��л�����Ҫ���ǩ�ķ�֧�ϣ�
$ git branch
$ git checkout master
Ȼ��������git tag <name>�Ϳ��Դ�һ���±�ǩ��
$ git tag v1.0
����������git tag�鿴���б�ǩ��
$ git tag
Ĭ�ϱ�ǩ�Ǵ��������ύ��commit�ϵġ���ʱ��������˴��ǩ�����磬�����Ѿ��������ˣ���Ӧ������һ��ı�ǩû�д���ô�죿
�������ҵ���ʷ�ύ��commit id��Ȼ����ϾͿ����ˣ�
$ git log --pretty=oneline --abbrev-commit

�ȷ�˵Ҫ��add merge����ύ���ǩ������Ӧ��commit id��f52c633���������
$ git tag v0.9 f52c633
��������git tag�鿴��ǩ��
$ git tag

ע�⣬��ǩ���ǰ�ʱ��˳���г������ǰ���ĸ����ġ�������git show <tagname>�鿴��ǩ��Ϣ��
$ git show v0.9
�����Դ�������˵���ı�ǩ����-aָ����ǩ����-mָ��˵�����֣�
$ git tag -a v0.1 -m "version 0.1 released" 1094adb
������git show <tagname>���Կ���˵�����֣�

$ git show v0.1
 ע�⣺��ǩ���Ǻ�ĳ��commit�ҹ���������commit�ȳ�����master��֧���ֳ�����dev��֧����ô����������֧�϶����Կ��������ǩ��
С��
����git tag <tagname>�����½�һ����ǩ��Ĭ��ΪHEAD��Ҳ����ָ��һ��commit id��
����git tag -a <tagname> -m "blablabla..."����ָ����ǩ��Ϣ��
����git tag���Բ鿴���б�ǩ��

������ǩ
https://www.liaoxuefeng.com/wiki/896043488029600/902335479936480
�����ǩ����ˣ�Ҳ����ɾ����
$ git tag -d v0.1
��Ϊ�����ı�ǩ��ֻ�洢�ڱ��أ������Զ����͵�Զ�̡����ԣ����ı�ǩ�����ڱ��ذ�ȫɾ����
���Ҫ����ĳ����ǩ��Զ�̣�ʹ������git push origin <tagname>��
$ git push origin v1.0

���ߣ�һ��������ȫ����δ���͵�Զ�̵ı��ر�ǩ��
$ git push origin --tags
Total 0 (delta 0), reused 0 (delta 0)
To github.com:michaelliao/learngit.git
 * [new tag]         v0.9 -> v0.9
�����ǩ�Ѿ����͵�Զ�̣�Ҫɾ��Զ�̱�ǩ���鷳һ�㣬�ȴӱ���ɾ����

$ git tag -d v0.9
Deleted tag 'v0.9' (was f52c633)
Ȼ�󣬴�Զ��ɾ����ɾ������Ҳ��push�����Ǹ�ʽ���£�

$ git push origin :refs/tags/v0.9
To github.com:michaelliao/learngit.git
 - [deleted]         v0.9
Ҫ�����Ƿ���Ĵ�Զ�̿�ɾ���˱�ǩ�����Ե�½GitHub�鿴��

С��
����git push origin <tagname>��������һ�����ر�ǩ��
����git push origin --tags��������ȫ��δ���͹��ı��ر�ǩ��
����git tag -d <tagname>����ɾ��һ�����ر�ǩ��
����git push origin :refs/tags/<tagname>����ɾ��һ��Զ�̱�ǩ��

ʹ��GitHub
��β���һ����Դ��Ŀ�أ������������ߵ�bootstrap��Ŀ������һ���ǳ�ǿ���CSS��ܣ�����Է���������Ŀ��ҳhttps://github.com/twbs/bootstrap���㡰Fork�������Լ����˺��¿�¡��һ��bootstrap�ֿ⣬Ȼ�󣬴��Լ����˺���clone��

һ��Ҫ���Լ����˺���clone�ֿ⣬��������������޸ġ������bootstrap�����ߵĲֿ��ַgit@github.com:twbs/bootstrap.git��¡����Ϊû��Ȩ�ޣ��㽫���������޸ġ�

Bootstrap�Ĺٷ��ֿ�twbs/bootstrap������GitHub�Ͽ�¡�Ĳֿ�my/bootstrap���Լ����Լ���¡�����ص��ԵĲֿ⣬���ǵĹ�ϵ������ͼ��ʾ��������

���� GitHub ��������������������������������������������������������������������������
��                                             ��
�� ��������������������������������������     �������������������������������������� ��
�� �� twbs/bootstrap  ����������>��  my/bootstrap   �� ��
�� ��������������������������������������     �������������������������������������� ��
��                                  ��          ��
�����������������������������������������������������������������������੤��������������������
                                   ��
                          ��������������������������������������
                          �� local/bootstrap ��
                          ��������������������������������������
��������޸�bootstrap��һ��bug����������һ�����ܣ����̾Ϳ��Կ�ʼ�ɻ��������Լ��Ĳֿ����͡�

�����ϣ��bootstrap�Ĺٷ����ܽ�������޸ģ���Ϳ�����GitHub�Ϸ���һ��pull request����Ȼ���Է��Ƿ�������pull request�Ͳ�һ���ˡ�

�����û�����޸�bootstrap��������Ҫ��һ��pull request���Ǿ�Forkһ���ҵĲֿ⣺https://github.com/michaelliao/learngit��
����һ��your-github-id.txt���ı��ļ���д���Լ�ѧϰGit���ĵã�Ȼ������һ��pull request���ң��һ�����������Ƿ���ܡ�

С��
��GitHub�ϣ���������Fork��Դ�ֿ⣻
�Լ�ӵ��Fork��Ĳֿ�Ķ�дȨ�ޣ�
��������pull request���ٷ��ֿ������״��롣

ʹ��Gitee
https://www.liaoxuefeng.com/wiki/896043488029600/1163625339727712

���ع������Զ�̿⣺
���ǿ���ɾ�����е�GitHubԶ�̿⣺
git remote rm origin
Ȼ���ȹ���GitHub��Զ�̿⣺
git remote add github git@github.com:michaelliao/learngit.git
�ٹ���Gitee��Զ�̿⣨ע��·������Ҫ��д��ȷ���û�������
git remote add gitee git@gitee.com:liaoxuefeng/learngit.git
���ڣ�������git remote -v�鿴Զ�̿���Ϣ�����Կ�������Զ�̿⣺
git remote -v
gitee	git@gitee.com:liaoxuefeng/learngit.git (fetch)
gitee	git@gitee.com:liaoxuefeng/learngit.git (push)
github	git@github.com:michaelliao/learngit.git (fetch)
github	git@github.com:michaelliao/learngit.git (push)

���Ҫ���͵�GitHub��ʹ�����

git push github master
���Ҫ���͵�Gitee��ʹ�����

git push gitee master
����һ�������ǵı��ؿ�Ϳ���ͬʱ����Զ�̿⻥��ͬ����

���������������������� ����������������������
�� GitHub  �� ��  Gitee  ��
���������������������� ����������������������
     ��           ��
     �������������Щ�����������
           ��
    ������������������������������
    �� Local Repo  ��
    ������������������������������
GiteeҲͬ���ṩ��Pull request���ܣ�����������С�����뵽��Դ��Ŀ�����������ͨ��Fork�ҵĲֿ⣺https://gitee.com/liaoxuefeng/learngit������һ��your-gitee-id.txt���ı��ļ��� д���Լ�ѧϰGit���ĵã�Ȼ������һ��pull request���ң�

����ֿ����Gitee��GitHub��˫��ͬ����


