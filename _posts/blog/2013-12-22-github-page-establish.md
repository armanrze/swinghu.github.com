---
layout: post
title: github ������վ�
description: ʹ��github�������ҳ,GitExtensions,RailInstaller��
category: blog
---
д��ƪ������Ҫ���ܽ��Լ�ѧϰ�web page�Ĺ��̣������´Σ��ܽ����������������⣬
Ҳ�ǰ���û��ʹ�ù�github��Jekyll��ͯЬ���Կ������մ���̣��������顣

������ruby��ȫû���˽⣬������html�г������˽⣬�ⶼû�й�ϵ��ֻҪ�㶮һ���linux�������
����ls,cd,mkdir,cp,ssh�����(����Ҳû�й�ϵ),�������õ�ʱGoogle��һ�����������ؼ�������������ܣ����岽�����£�

1����װGit
��windows�°�װgit����ѡ�����GitExtensions233SetupComplete.msiĬ�ϰ�װ���С�

2����װruby����
��װRailInstaller����ѧϰ�Ĺ����У������������Ϸ��ִ�����Ƽ���װRuby2.0.0���������汾����ʵ���������
�����ٴ���һЩ����(��Щ�����������������µ��£���Щ����д�Ĳ�����ϸ������)������rubyinstaller-1.9.3-p448.exe
ѡ��Ĭ�ϰ�װ(������װ·����Ҫ���ֿո������)��Ϊʲôѡ����Ϊ�伯����Ruby��Rails��Bundler��Git��Sqlite��TinyTDS��SQL Server support��DevKit������
(������Ҫʹ�õĵ�Devkit)������RailInstaller�ĺô��������ͻ����֡�

3������Git
��RailInstaller��װ��ɽ���(����װ�����һ��)����ʾ�Ƿ����Git���������ã�Ĭ�������ѡ���ǣ�ѡ��ȷ�������С�
�����֮ǰ���ú���git����߻��Զ���⵽��������Ϣ����git�ʺţ����䣬key���Լ�����ʾһЩ������Ϣ�磺ruby��git�汾֮���
�����Զ�cd��Ŀ¼ /c/Sites���棬�����ֻҪ�����ͷ��ڸ�Ŀ¼�¾��С�
�ڿ�ʼ�˵����ҵ�RailsInstaller �C> Git Bash��ִ�������ʹ������������ڣ��Ժ�����ò�����������������½��е�
���Ȳ����Ƿ�git�����������ӣ�������ܣ���ص���һ������Git������(�����������У���ʼ->����->RailsInstaller �C> Git Bash ����̨��ִ��(�ÿ���̨����Ҫ��Ϊ���û�����))��
	ssh -T git@github.com
��ʾ������Ϣ��ʾ���ӳɹ���

	$  ssh -T git@github.com
	Hi user_name! You've successfully authenticated, but GitHub does not provide shell
	access.
	
4����װJekyll����ذ�
���ȸ���һ�������ļ��ĵ�ַ��

	gem sources --remove http://rubygems.org/
	gem sources -a http://ruby.taobao.org/
	
Ȼ����gem sources -l��������Դ�б�(�ҵĵ����������˶�Σ������ж����)
	$ gem sources -l
	
	*** CURRENT SOURCES ***
	http://ruby.taobao.org/
	http://ruby.taobao.org/
	http://ruby.taobao.org/
	http://ruby.taobao.org/
	http://ruby.taobao.org/

��װjekyll

	gem install jekyll
	
��װ�����Jekyll��Ҫ�õ�directory_watcher��liquid��open4��maruku��classifier�⼸������
���������������Զ���װ��JekyllĬ����maruku������markdown���ԣ���Ҳ�����ñ�ĳ�����������
����rdiscount��kramdown

	gem install rdiscount kramdown

5������github pages
��github.com�ϴ�������⣬��¼���Լ���Github�˻���ѡ��New repository,�����½�һ�����磺name.github.com�Ĵ����
Ȼ���ڴ����ҳ��ѡ���Ҳ�������б���Settings���ͻ�Ը���Ŀ�����޸ģ��ҵ�Github Pagesһ��������Ҳ�Automatic Page Generator��ť
������ҳ���Ե�Ƭ��ϵͳ�ͻὫ��ҳ���ɺá������ɺú󣬿�¡�Լ��Ĵ����
	git clone git@github.com:user_name/dkd.git
ִ���Ժ�git��Ѵ����github�ϵĴ�����ļ����ص����صģ�������Ϊdkd��Ŀ¼��ɾ��.gitĿ¼�����ҽ���վ�ļ������ڸ��ļ�����

6��д���ģ�������(��򿪣���ʼ->����->RailsInstaller �C> Command Prompt with Ruby and Rails����̨Ӧ�ó��򣬽�����ǵĲ������Ͷ�����ͨ���������̨����)
�༭���ͣ������ļ���׺.md���������Ŀ�ͷ��ʽ����

	---
	layout: post
	title: MathJax���
	category: blog
	description: Shell���û���Linux����ϵͳ��ͨ����������ÿһ��Linux�û��ı��޹���֮һ��
	---

�ļ�������ʽ����:
	2013-12-8-Linux-Shell.md
��ȷ������ļ�������Ϊ���� BOM �� UTF-8(�����ǽ������������ʹ��notepad++ �����и�ʽת��) 
ʹ��git�������͵�git�������ϣ��ȼ��뱾�ؿ���
	git add .
	git commit -m"��ע�޸���Ϣ��
	git push
������������������޸Ĺ�����ô��Ҫִ�� git pull�������ʾ�� non-fast-forward����

	C:\Sites\username.github.com>git push
	To git@github.com:username/username.github.com.git
	! [rejected]        master -> master (non-fast-forward)
	error: failed to push some refs to 'git@github.com:username/username.github.com.git'
	To prevent you from losing history, non-fast-forward updates were rejected
	Merge the remote changes (e.g. 'git pull') before pushing again.  See the
	'Note about fast-forwards' section of 'git push --help' for details.
7������������username.github.io
�Ե�Ƭ�̣�github�ͻ�Ϊ��������ҳ�������������ַ��username.github.com


�������ܣ�
- msygit���ӣ�[msygit][msygit]
- RailInstall�������ӣ�[RailInstall-1.9.3-p448][rail]

[msygit]: http://code.google.com/p/msysgit/downloads/list
[rail]: http://inwake.com/ypchen/files/upload/railsinstaller-2.0.1.exe