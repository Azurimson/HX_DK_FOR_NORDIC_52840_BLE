# ǰ��
С��֮ǰ������Ⱥ�������˵����ʮ��Ǯ��׽��������׽Mesh���ݰ��Ļ�����Ellisys��Frontline���͵������𣿡���������С�໹��̫�����ʡ��ˣ�
![](./local_pics/too_hasty.png)

���ſƼ��ز��Ϸ�չ��Ŀǰ�ǿ���ʹ�õͳɱ���Ӳ����ʵ��Mesh���ݵ�׽������ܵģ���ô��������ô�����أ�Here we go!

# ǰ��׼��
���ȣ�������Ҫ���¼������ߣ�
- [�������ߵ�52840 Dongle](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4023-22232069203.13.753f3551e5TkFc&id=598472801867) 
	![](./local_pics/hx_52840_dongle.png)

- ����������Э��������[Wireshark](https://www.wireshark.org/)
	
    ![](./local_pics/wireshark.png)

	> ��װ���µİ汾����

- [Python 3.6](https://www.python.org/downloads/)����
    > ע�⣺��װʱ��Ҫ��pipҲ��װ��
- [nRF Sniffer for Bluetooth LE](https://www.nordicsemi.com/Software-and-Tools/Development-Tools/nRF-Sniffer-for-Bluetooth-LE/Download#infotabs)
    > �������µİ汾����
- [nRF Connect for Desktop](https://www.nordicsemi.com/Software-and-Tools/Development-Tools/nRF-Connect-for-desktop)
    > �������µİ汾����

���ڣ������ἰ����Python��Wireshark�Լ�nRF Connect for Desktop�������װ���ﲻ����Ϊ��ʵ���벻����������������ᰲװ�Ĺ���ʦΪʲô������������������

![](./local_pics/i_dont_understand.png)
# ��¼ץ���̼�
����¼֮ǰ�����ǻ���Ҫ��nRF Connect for Desktop�а�װnRF Connect Programmer����װ���̲�������װ��Ľ�������ͼ��ʾ��
![](./local_pics/nRF_programmer.png)
��Programmer����ԶԺ����52840 Dongle����׽���̼�����¼������׽���Ĺ̼���nRF Sniffer for Bluetooth LE�п����ҵ�������ͼ��ʾ��
![](./local_pics/sniffer_firmware.png)
![](./local_pics/downloading.png)
1. ����ץ���Ĺ̼�
2. ץ���̼���·��
3. ���װ�سɹ������ʾ

����ץ���̼�֮�󣬲���[�������ߵ�52840 Dongle](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4023-22232069203.13.753f3551e5TkFc&id=598472801867)�����������װ�����Ļ���һ���ʱProgrammer���ҵ�ӳ��Ĵ��ڣ�����ͼ��ʾ��
![](./local_pics/COM_Port.png)
���ǣ���ʱ��**�ݲ�ѡ�񴮿�**������Ҫ������ͼ��ɫ�����İ�������USB DFUģʽ��
![](./local_pics/dongle_red_highlghted.png)
�����ʱ�����������˵��Dongle�Ѿ�������USB DFUģʽ�����ڿ���ѡ�и��豸������ץ���̼�����¼��
![](./local_pics/dongle_blink.gif)
���������ͼ��ʾ���棬��˵������Dongle�ɹ��ҿ����������й̼���¼��
![](./local_pics/firmware_download.png)
1.  ��ʾ��Dongle�������ӳɹ�
1. ��¼ץ���̼�

��������Ĳ�������ȷ�������Ļ�����ô���ջ�������½��棺
![](./local_pics/download_successfully.png)
��ʱ��ץ���̼��Ѿ���¼����ˣ����������Ǽ������������
# �������
��Ϊ���������ǵ���Wireshark��ץȡ�������ݰ�����Э��������������Ǵ�ʱ����Ҫ���������ص�
[nRF Sniffer for Bluetooth LE](https://www.nordicsemi.com/Software-and-Tools/Development-Tools/nRF-Sniffer-for-Bluetooth-LE/Download#infotabs)�������ã�����������ʾ:
1. ��**Sniffer_Software/extcap/** �ļ����д�CMD����װ��Ӧ����������������С���·����
	> F:\Bluetooth\Nordic\Sniffer\nrf_sniffer_for_bluetooth_le_3.1.0_7cc811f\extcap

	�Լ�����

	> pip3 install -r requirements.txt
	
	![](./local_pics/open_floder_with_cmd.gif)
��ΪС���Ѿ���װ���ˣ�������ʾ˵�Ѿ���װ��ɣ�����ǵ�һ�ΰ�װ�Ļ��ͻ��Զ�������Ӧ����������
2. ����Nordic��׽�����ߵ�Wireshark���ļ��У�

    a. ��Wireshark�������ѡ��**Help** --> **About Wireshark**
![](./local_pics/wireshark_extcap.png)
b. ѡ�� **��Floders��** ����˫��**Global Extcap path**�ͻ��������Ӧ��·����������**Sniffer_Software/extcap/**�ļ����е����ݣ�
![](./local_pics/wireshark_extcap_copy.png)
c. �����ϣ����ʱ����������Ѿ�����ˣ���ʱ�����ڸ��ƺ�����Ŀ¼�£��������������������֤�Ƿ����óɹ���
	> nrf_sniffer_ble.bat --extcap-interfaces

	���������ڱ�Ŀ¼�´�CMD�ķ���������������ָ�������������Ľ�����˵�����óɹ���
	![���������ͼƬ����](https://img-blog.csdnimg.cn/202012232211396.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3hpYW9sb25nYmE=,size_16,color_FFFFFF,t_70)
# ץ��ԭ��
�����ж��ߴ�ʱ�е㲻�ͷ��ˣ������ڿ�ʼץ��֮ǰ��С����û��Ǻ��б�Ҫ����ҽ������ץ��ԭ��������ô���ģ��ϻ�����˵���Ϲ��---��ͼ������
![](./local_pics/plugin_confirmation.png)
����ͼ��֪�����������ץȡ�㲥���Ļ�����ô��ʡ�¶��ˣ�ֱ�Ӷ���37��38��39�����㲥�ŵ�ɨ�裬Ȼ���ץȡ�������ݽ��н������ɣ���Ȼ�������չ�㲥���Ļ������ܻ�Ƚ��鷳Щ���������С���Ժ��ר�ſ����½ڽ��н��⣻������֪��BLE������֮��ÿ�����Ӽ�����ǻ���Ƶ�ģ���ô���ʱ��ץ����������ô׽���أ�BLE 5.0֮ǰ����Ƶ�Ĳ����ǹ̶��ģ�����5.0֮����Ƶ�Ĳ�����������ˣ�������ץ������Ҫ��͸����ˣ����ǣ��ٸ���Ҳ��ͨ����ѧ��ʽ��������ģ����ں��û�а���ѧѧ�ðɣ�
![](./local_pics/math_makes_me_happy.png)
����5.0֮�����Ƶ�㷨�Ƚϸ��ӣ�С�����ﲻ������Ȥ�Ķ��߿��������Ķ�Spec�����ǣ���С��������ѧ����˵����û�а취ͨ������ĳЩֵ�����������Ƶ���б��أ��𰸣���Ȼ���еģ����ʱ��Ͳ��ò�����һ�������ˣ����ô�￴��Ч����
![](./local_pics/hopping_selection_2.png)
��ɫ�����Ǽ����������Ƶ�б�����ͼ��ʵ��ץ��ʱ������ͨ���б�
![](./local_pics/channel_capture.png)
������������ͼ�����ǿ��Կ�����0~4�������¼�����Ƶ�ŵ���ץ���õ��������ŵ�����ȫһ���ģ�����**CONNECT_IND**����ϢЯ����**Access Address**��������������ֻҪ��**Access Address**ֵ�����������ȥ���ɼ����������Ƶ�б�ͬ��ץ�������������**CONNECT_IND**����Ϣ���������һ���ŵ������**�Ӷ�ʵ��ץ����Ŀ�ģ���Ҳ��Ϊʲô��ץȡ���ݰ�ʱ��һ��Ҫ�ڹ㲥ǰ�ʹ�Sniffer������ץȡ�������ݰ�**��
# ��ʼץ��
��������С����ʽ���⿪ʼ��ƪ���µ��ص㣬Ҳ�Ǵ����ϲ���Ļ��ڣ���ô��ôʹ��[�������ߵ�52840 Dongle](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4023-22232069203.13.753f3551e5TkFc&id=598472801867)����ץȡMesh���ݰ��������أ�
1. ���ȣ���Wiresharkѡ��[�������ߵ�52840 Dongle](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4023-22232069203.13.753f3551e5TkFc&id=598472801867)������ͼ��ʾ��
![](./local_pics/dongle_open.png)
2. ˫����ͼ�е� **��nRF Sniffer for Bluetooth LE COM22��**�����ɿ�ʼץ��
3. ���������ܱ߻���������������ǲ���Ҫ��BLE���ݰ�����ô���ʱ�����Ҫ����һ�£�����С���������ͨ��BLE���ݰ���ֻ������Mesh��ص����ݰ��Լ����ڲ����Ǹ��豸�����˵��������£�
	> ((pbadv) || (provisioning)||(btmesh)||(beacon) ) && ((btle.advertising_address == eb:7b:7a:14:1c:02)||(btle.advertising_address == d3:31:5a:db:35:91))

	![](./local_pics/sniffer_filter.png)
4. ����һ�� [HX-DK-�� Z1A00](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4004-22261057662.6.43ba2c2cqFeXqh&id=608555326842)����Nordic�ٷ���Light_Switch�̼�������һ�� [HX-DK-�� Z1A00](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w4004-22261057662.6.43ba2c2cqFeXqh&id=608555326842)����Nordic�ٷ���Provisioner�̼�
5. ����Provisioner�Ǹ��������**Button 1**����ʱProvisioner���������Ϳ�ʼ��δ�������豸��������
6. ���ʱ��[�������ߵ�52840 Dongle](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4023-22232069203.13.753f3551e5TkFc&id=598472801867)�ͻὫ������������ץȡ������ʾ��Wireshark�����ϣ�Ȼ�������Ǵ�Ҷ�֪����Mesh����֮�����е����ݶ���ͨ�����ܵģ���ô��������أ������ʵ��Ellisys��һ���ģ�ֻҪ����Netkey,Appkey,DevKey�Լ�IV Index���ɣ����ѡ��һ�����ܺ��Mesh���ݰ�����ǰ���ᵽ����������ȥ������������£�
![](./local_pics/sniffer_key.png)
������ͼ�еĲ������Netkey,Appkey,DevKey�Լ�IV Index��������С���Ϊ����
![](./local_pics/sniffer_net_app_key.png)
![](./local_pics/sniffer_devkey.png)
��Ҫע����ǣ�**���е�Key��Ҫ��ǰ����ϡ�0x��������SRC Addressָ���ǽڵ�Ԫ�ص��׵�ַ**�����ˣ�Wireshark�Ϳ��Խ�������Mesh����֮��������ˣ�
# ʵ����
������С����[�������ߵ�52840 Dongle](https://item.taobao.com/item.htm?spm=a1z10.3-c-s.w4023-22232069203.13.753f3551e5TkFc&id=598472801867)ץȡ����Mesh�����Լ����õ��������̣�
![](./local_pics/test_result.png)
