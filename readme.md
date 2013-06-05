������ ����� �������������� ����������� ���-1� - .msi �����
============================================================

������ ������ - .msi ����� ��� ������������ � ������ ������ ������������ �������� ��� ����������
������� ����� �������������� ����������� ���-1�.

� ������ ������ �������� ��� �� � �������� ��� ����������� ������ � ����������.

����������� ��� ������ .msi ������
----------------------------------

��� �������� ��������� � ����� � ��������� ������ ������ ����������� ��������� ��������:

- Microsoft Visual Studio 2012 Shell:
  - [Isolated](http://www.microsoft.com/ru-ru/download/details.aspx?id=30670)
  - [Integrated](http://www.microsoft.com/ru-ru/download/details.aspx?id=30663)
- [Windows Installer XML Toolset - WIX](http://wixtoolset.org/)

���������� ���������� ��� ������ � ��������� �������. � ���������� - ������� MS Visual Studio 2012 � ���������������
��������� �������� WiX. ����� ����� ��������� ���� ������� `MLP-1E.sln` � �������� �������.

�������� �������
----------------

### ���������������� ����� ���������

� ����� `bin\Admin image\x86\ru-RU` ������ ������, �������������� � ���� ���������������� ����� ���������.
� ��� ����������� ��������� ������������.

### .msi ����� � ���� ������� �����

� ����� `bin\Single .msi file\x86\ru-RU` ������ .msi ����� � ���� ������� �����.
� ������� �� ����������� ��������, � ������ �������� ������������ ��������� ������������,
����������� �������� � ������ ��������, � ����� ��� ���������.

��� ������������� �������� ���������������� ����� ��������� � ����������� ������������ ������� ���������������
��������� ������� �� ���������� �������:

    msiexec -a "bin\Single .msi file\x86\ru-RU\mlp-1e.msi" TARGETDIR="adm\x86"

���������� ���������������� ����� ���������
-------------------------------------------

��� ���������� ���������������� ����� ��������� �������� � ��������� ������������� ��������.

### ALLUSERS

�� ��������� - `"1"`. ��� ��������� `"0"` ����������� ����� ������������ � ������� ������������, � �� � ������� ����������.

### DISABLESHORTCUTS

�� ��������� - `"No"`. ��� ��������� �������� `"Yes"` ��� ��������� �� ����� ������������ ������.
������ ��������� ������� ���������������, ���� �� ���������� ��������� ���������� ��� ������������� ����� ������ ��
`.csmdb23` ����� (� ������ �������������� ������������ ������ ������� �����).

### DISABLEDESKTOPSHORTCUTS

�� ��������� - `"No"`. ��� ��������� �������� `"Yes"` ��� ��������� �� ����� ������������ ������ �� ������� �����.
��� `DISABLESHORTCUTS="Yes"` �������� ������� �������� ���� �� ������.

### DISABLEMENUSHORTCUTS

�� ��������� - `"No"`. ��� ��������� �������� `"Yes"` ��� ��������� �� ����� ������������ ������ � ����.
��� `DISABLESHORTCUTS="Yes"` �������� ������� �������� ���� �� ������.

### DISABLESTARTUPSHORTCUTS

�� ��������� - `"Yes"`. ��� ��������� �������� `"Yes"` ��� ��������� �� ����� ������������ ����� �� ��� �������������
� ���� ������������. ��� `DISABLESHORTCUTS="Yes"` �������� ������� �������� ���� �� ������.

### APPLICATIONFOLDER

���� � �����, � ������� ����� ���������� ����������� �������. �� ��������� - `%ProgramFiles(x86)%\���\�������������\2.3%`.
������������� � �������� �������� ������� �������� ��������� ������ ���� �� ��������� � `%ProgramFiles%`.

### INSTALLLEVEL

�� ��������� - `"100"`. �� �������� ����� ����������� ������ ���������� "��� �������������" � "���� �����".
��� ��������� `INSTALLLEVEL` ������ 200 ����� ����������� � ���������� "������������� - �������������".

### �������

��������� �������� ���������� ���������������� ����� ���������:

	msiexec -a mlp-1e.msi DISABLEDESKTOPSHORTCUTS=Yes ALLUSERS=0

������ ��������� ������ ������� ����� ��������� � "������������" �������� �������� �����, � ���������� ���������� ��� ������������
(� �� ��� ����������).

	msiexec -a mlp-1e.msi DISABLESHORTCUTS=Yes

������ ��������� ������ ������� ����� ��������� � "������������" ��������.