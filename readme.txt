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


