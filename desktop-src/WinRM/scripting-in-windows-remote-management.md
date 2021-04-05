---
title: Создание сценариев в служба удаленного управления Windows
description: API скриптов в WinRM и сопутствующий API COM для C++ предназначены для точного отражения операций протокола WS-Management.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Создание сценариев в служба удаленного управления Windows
- Служба удаленного управления Windows, создание сценариев в
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75af10fea03853de99c884eda0a74ce340683b49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133910"
---
# <a name="scripting-in-windows-remote-management"></a>Создание сценариев в служба удаленного управления Windows

[API скриптов в WinRM](winrm-scripting-api.md) и СОПУТСТВУЮЩИЙ API COM для C++ предназначены для точного отражения операций протокола WS-Management.

API скриптов WinRM в служба удаленного управления Windows поддерживает все операции WS-Management протоколов, кроме одного. Он не допускает подписки на события. Чтобы подписываться на события из журнала системных событий BMC, необходимо использовать программы командной строки wecutil или wevtutil. Дополнительные сведения см. в статье [Events (Visual Basic)](events.md) (События в Visual Basic).

API-интерфейс сценариев WinRM вызывается Winrm.vbs, программой командной строки, написанной в Visual Basic Scripting Edition (VBScript). В Winrm.vbs приводятся примеры использования [API-интерфейса сценариев WinRM](winrm-scripting-api.md).

## <a name="using-wsman-compared-to-using-wmi-scripting"></a>Использование WSman по сравнению с использованием сценариев WMI

WMI подключается к удаленным компьютерам через DCOM, что требует настройки, описанной в разделе [Подключение к WMI на удаленном компьютере](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer). WinRM не использует DCOM для подключения к удаленному компьютеру. Вместо этого протокол WS-Management отправляет сообщения SOAP, а служба использует один порт для HTTP и порт для транспорта HTTPS.

В отличие от программы командной строки **WinRM** , скрипты должны предоставлять XML-код, необходимый для передачи в сообщения протокола WS-Management. Они также должны предоставлять URI. Дополнительные сведения см. в разделе [URI ресурсов](resource-uris.md) , [Служба удаленного управления Windows и WMI](windows-remote-management-and-wmi.md).

API сценариев WMI работает с объектами, такими как экземпляры [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), которые представляют ресурсы на компьютере. Этот класс WMI определен в файлах [*MOF-файл (MOF)*](/windows/desktop/WmiSdk/gloss-m) , которые хранятся в двоичном формате в репозитории WMI. В WMI операция получения для отдельного ресурса или запроса для нескольких экземпляров возвращает объекты WMI.

Сценарий WinRM не возвращает объекты, а потоки XML-текста. Дополнительные сведения см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md).

## <a name="displaying-xml-output-from-winrm-scripts"></a>Отображение выходных данных XML из скриптов WinRM

API сценариев WinRM получает и получает XML-строки, описывающие ресурсы. Результирующий XML-код представлен в виде текстового потока и требует, чтобы преобразование XML было представлено каким-либо другим способом.

Следующий сценарий WinRM создает необработанные выходные данные в формате XML.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



Следующий блок текста показывает выходные XML-данные сценария WinRM.


```XML
<p:Win32_Service xmlns:xsi="https://www.w3.org/2001/XMLSchema-
instance" xmlns:p="http://schemas.microsoft.com/wbem/wsman/1
/wmi/root/cimv2/Win32_Service" xmlns:cim="https://schemas.dmtf
.org/wbem/wsman/1/base" cim:Class="Win32_Service"><p:AcceptP
ause>false</p:AcceptPause><p:AcceptStop>true</p:AcceptStop>
<p:Caption>Print Spooler</p:Caption><p:CheckPoint>0</p:CheckP
oint><p:CreationClassName>Win32_Service</p:CreationClassName>
<p:Description>Loads files to memory for later printing</p:De
scription><p:DesktopInteract>true</p:DesktopInteract><p:Displ
ayName>Print Spooler</p:DisplayName><p:ErrorControl>Normal</p
:ErrorControl><p:ExitCode>0</p:ExitCode><p:InstallDate xsi:ni
l="true"/><p:Name>spooler</p:Name><p:PathName>C:\Windows\Syst
em32\spoolsv.exe</p:PathName><p:ProcessId>1720</p:ProcessId><
p:ServiceSpecificExitCode>0</p:ServiceSpecificExitCode><p:Ser
viceType>Own Process</p:ServiceType><p:Started>true</p:Starte
d><p:StartMode>Auto</p:StartMode><p:StartName>LocalSystem</p:
StartName><p:State>Running</p:State><p:Status>OK</p:Status><p
:SystemCreationClassName>Win32_ComputerSystem</p:SystemCreati
onClassName><p:SystemName>wsplab6-4</p:SystemName><p:TagId>0<
/p:TagId><p:WaitHint>0</p:WaitHint><cim:Location xmlns:cim="h
ttp://schemas.dmtf.org/wbem/wsman/1/base" xmlns:a="https://sc
hemas.xmlsoap.org/ws/2004/08/addressing" xmlns:w="https://sche
mas.dmtf.org/wbem/wsman/1/wsman"><a:Address>https://schemas.xm
lsoap.org/ws/2004/08/addressing/role/anonymous</a:Address><a:
ReferenceParameters><w:ResourceURI>https://schemas.microsoft.c
om/wbem/wsman/1/wmi/root/cimv2/Win32_Service</w:ResourceURI><
w:SelectorSet><w:Selector Name="Name">spooler</w:Selector></w
:SelectorSet></a:ReferenceParameters></cim:Location></p:Win32
_Service>
```



Скрипты могут использовать преобразование XML, чтобы сделать эти выходные данные более удобочитаемыми. Дополнительные сведения см. [в разделе вывод XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).

Следующая версия скрипта форматирует XML-код в виде выходного человека.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xslFile.Load( "WsmTxt.xsl" )
Wscript.Echo xmlFile.TransformNode( xslFile )
```



Преобразование «XSL» создает следующие выходные данные.


```XML
Win32_Service
    AcceptPause = false
    AcceptStop = true
    Caption = Print Spooler
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = Loads files to memory for later printing
    DesktopInteract = true
    DisplayName = Print Spooler
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = Spooler
    PathName = C:\Windows\System32\spoolsv.exe
    ProcessId = 1720
    ServiceSpecificExitCode = 0
    ServiceType = Own Process
    Started = true
    StartMode = Auto
    StartName = LocalSystem
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = wsplab6-4
    TagId = 0
    WaitHint = 0
```



## <a name="winrm-script-and-winrmcmd-output"></a>Сценарий WinRM и выходные данные WinRM. cmd

Выходные данные сценария WinRM кодируются в Юникоде. При создании [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) и записи файла из скрипта полученный файл будет иметь кодировку Unicode. Однако при перенаправлении выходных данных в файл используется кодировка ANSI. При перенаправлении выходных данных в XML-файл и наличии в выходных данных символов Юникода XML-код будет недопустимым. Имейте в виду, что программа командной строки **WinRM** выводит значение ANSI.

## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))
</dt> <dt>

[Справочник по модели DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))
</dt> </dl>

 

 