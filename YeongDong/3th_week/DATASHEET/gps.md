UBlox M8 GPS����

================


GPS���, POSLLH �޽��� ��Ŷ ������ ������ ����, Endian�̶�?

-----------------------------------------------------------


#1. GPS�� �۵� ����?

##2. POSLLH �޽��� ��Ŷ ����

###3.  POSLLH �޽����� ������ �ִ� �������� ����

####4. Endian�� ����


1. GPS�� �۵� ����?

--------------------

>GPS��?
>>GPS Global Positioning System�� ���ڷ� **��������ġ�����ý���**�� �ǹ� �Ѵ�. �� GPS�� ��������
������ ��ȣ�� ������ �������� ������� ���� ��ġ�� �˷��ִ� �ý����̴�. 1970��� ������ ��Ȯ����
���̱� ���� �̱� ���漺���� ������ ���� �����̸� ���� �ΰ��ο��Ե� ����Ǹ鼭 �� ���迡�� �����
��� ������ �ý����̴�.

>GPS�� �۵�����?  
>>GPS�� ���� �ٽ� ����� �ٷ� 4���� GSP������ ���Žð��� �޷��ִ�. GPS������ �����̶�� ������ �̿���
������ ���ڽð谡 ����ִ�. �׷��� �� ������ �� ��Ȯ�� �ð��� ������ ��ġ�� ������ ���ű�� �����µ�
���� ���ĸ� �����Ҷ��� �ð����� ����� �ȴ�. �̶� ��Ÿ���� �ۼ��� �ð��� �ð� ���� �̿��� �Ÿ��� ���ϰ� 
4���� GPS������ �����Ÿ��� ������ ������ ���� ���� ��ġ�� �� �� �ְ� �Ǵ� ���̴�.

>���� ����
>>3���� ��鿡���� X, Y, Z�࿡ ���� ������ �˸� ��Ȯ�� ��ġ�� ���� �� �־� ���� GPS������ 4�����̳� �����
�ʿ䰡 �����ٵ� ���� GPS������ 4�����̳� ����ϴ� ������ ������ ��Ȳ�� ���� ��ġ ���� �� ������ �����ϱ�
���� �ʿ��ϴ�. �׷��� �������� GPS�ý����� ���ؼ��� GPS������ 4����  �ʿ��� ���̴�.      


2. POSLLH �޽��� ��Ŷ ����

---------------------------

������������������������������������������������������������������������������
��                  ��Header    ��Length (Bytes)    ��Payload   ��Checksum  ��
��Message Structure ����������������������������������������������������������
��                  ��0xB5 0x62 ��28                ��see below ��CK_A CK_B ��
������������������������������������������������������������������������������

>NAV-POSLLH �޼��� ��Ŷ�� ���� ���� ������ ��Ÿ����.
>�߰� : NAV Class��� ���� ID ������ ���� �� �� ������ POSLLH Message��� ������ ��Ÿ�� �ش�.

>NAV-POSLLH �޼����� �̿��� Serial Port ��� ������ ��

>>GPSInfo.satfix = 3
>>GPSInfo.satnum = 7
>>GPSInfo.longitude = 1270251885
>>GPSInfo.latitube = 374938144
>>GPSInfo.altitube = 48981

>>GPSInfo.satfix = 3
>>GPSInfo.satnum = 7
>>GPSInfo.longitude = 1270251886
>>GPSInfo.latitube = 374938136
>>GPSInfo.altitube = 48899


3. POSLLH �޽����� ������ �ִ� �������� ����

---------------------------------------------

>POSLLH �޽����� Geodetic Position Solution(���� ��ġ �ذ�å)������ ��Ÿ���ش�.
>�� POSLLH �޽����� ������ ���� 5���� �����͸� �����ϰ� �ִ�.

>>(1)�ð� ������
 
>>(2)���� ������

>>(3)�浵 ������

>>(4)���� �� Ÿ���� �ؼ����� �������� �� ����(����) ������

>>(5)����� ������ ���� ��Ȯ�� ������


4. Endian�� ����
-----------------

>Endian�� ����
>>Endian�� ��ǻ�� �޸𸮿� ���� 1���� ������ �������� ���ӵ� ����� �迭�ϴ� ����� ���Ѵ�. �� �ܾ 
�����ϴ� 2�� ����Ʈ���� �����ϴ� ����Ʈ�� ������ �����´� ����̴�.
>>Endian�� ���� ū ������ �տ� ������ Big-endianrhk ���� ������ �տ� ������ Little-endian���� ���� �� �ִ�.
���� ���� ���� �� ��쿡 ������ �ʰų� ���� ��� �����ϴ� Mibble-endian���� ������.