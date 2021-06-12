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









