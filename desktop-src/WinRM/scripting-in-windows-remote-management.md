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
# <a name="scripting-in-windows-remote-management"></a><span data-ttu-id="90ba3-105">Создание сценариев в служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="90ba3-105">Scripting in Windows Remote Management</span></span>

<span data-ttu-id="90ba3-106">[API скриптов в WinRM](winrm-scripting-api.md) и СОПУТСТВУЮЩИЙ API COM для C++ предназначены для точного отражения операций протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="90ba3-106">The [Scripting API in WinRM](winrm-scripting-api.md) and the accompanying COM API for C++ are designed to closely reflect the operations of the WS-Management protocol.</span></span>

<span data-ttu-id="90ba3-107">API скриптов WinRM в служба удаленного управления Windows поддерживает все операции WS-Management протоколов, кроме одного.</span><span class="sxs-lookup"><span data-stu-id="90ba3-107">The WinRM Scripting API in Windows Remote Management supports all the WS-Management protocol operations except one.</span></span> <span data-ttu-id="90ba3-108">Он не допускает подписки на события.</span><span class="sxs-lookup"><span data-stu-id="90ba3-108">It does not allow subscriptions to events.</span></span> <span data-ttu-id="90ba3-109">Чтобы подписываться на события из журнала системных событий BMC, необходимо использовать программы командной строки wecutil или wevtutil.</span><span class="sxs-lookup"><span data-stu-id="90ba3-109">To subscribe to events from the BMC System Event Log, you must use the Wecutil or Wevtutil command-line tools.</span></span> <span data-ttu-id="90ba3-110">Дополнительные сведения см. в статье [Events (Visual Basic)](events.md) (События в Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="90ba3-110">For more information, see [Events](events.md).</span></span>

<span data-ttu-id="90ba3-111">API-интерфейс сценариев WinRM вызывается Winrm.vbs, программой командной строки, написанной в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="90ba3-111">The WinRM Scripting API is called by Winrm.vbs, a command-line tool, which is written in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="90ba3-112">В Winrm.vbs приводятся примеры использования [API-интерфейса сценариев WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="90ba3-112">Winrm.vbs provides examples of how to use the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

## <a name="using-wsman-compared-to-using-wmi-scripting"></a><span data-ttu-id="90ba3-113">Использование WSman по сравнению с использованием сценариев WMI</span><span class="sxs-lookup"><span data-stu-id="90ba3-113">Using WSman Compared to Using WMI Scripting</span></span>

<span data-ttu-id="90ba3-114">WMI подключается к удаленным компьютерам через DCOM, что требует настройки, описанной в разделе [Подключение к WMI на удаленном компьютере](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="90ba3-114">WMI connects to remote computers through DCOM, which requires the configuration described in [Connecting to WMI on a Remote Computer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span></span> <span data-ttu-id="90ba3-115">WinRM не использует DCOM для подключения к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="90ba3-115">WinRM does not use DCOM to connect to a remote computer.</span></span> <span data-ttu-id="90ba3-116">Вместо этого протокол WS-Management отправляет сообщения SOAP, а служба использует один порт для HTTP и порт для транспорта HTTPS.</span><span class="sxs-lookup"><span data-stu-id="90ba3-116">Instead, the WS-Management protocol sends SOAP messages and the service uses a single port for HTTP and a port for HTTPS transport.</span></span>

<span data-ttu-id="90ba3-117">В отличие от программы командной строки **WinRM** , скрипты должны предоставлять XML-код, необходимый для передачи в сообщения протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="90ba3-117">Unlike the **winrm** command-line tool, scripts must provide the XML required to pass to the WS-Management protocol messages.</span></span> <span data-ttu-id="90ba3-118">Они также должны предоставлять URI.</span><span class="sxs-lookup"><span data-stu-id="90ba3-118">They must also provide URIs.</span></span> <span data-ttu-id="90ba3-119">Дополнительные сведения см. в разделе [URI ресурсов](resource-uris.md) , [Служба удаленного управления Windows и WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="90ba3-119">For more information, see [Resource URIs](resource-uris.md) and [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="90ba3-120">API сценариев WMI работает с объектами, такими как экземпляры [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), которые представляют ресурсы на компьютере.</span><span class="sxs-lookup"><span data-stu-id="90ba3-120">The WMI Scripting API works with objects, such as instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which represent resources on a computer.</span></span> <span data-ttu-id="90ba3-121">Этот класс WMI определен в файлах [*MOF-файл (MOF)*](/windows/desktop/WmiSdk/gloss-m) , которые хранятся в двоичном формате в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="90ba3-121">This WMI class is defined in [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) files, which are stored in binary form in the WMI repository.</span></span> <span data-ttu-id="90ba3-122">В WMI операция получения для отдельного ресурса или запроса для нескольких экземпляров возвращает объекты WMI.</span><span class="sxs-lookup"><span data-stu-id="90ba3-122">In WMI, a Get operation for a single resource or a query for multiple instances returns WMI objects.</span></span>

<span data-ttu-id="90ba3-123">Сценарий WinRM не возвращает объекты, а потоки XML-текста.</span><span class="sxs-lookup"><span data-stu-id="90ba3-123">A WinRM script does not return objects, but rather streams of XML text.</span></span> <span data-ttu-id="90ba3-124">Дополнительные сведения см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="90ba3-124">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="90ba3-125">Отображение выходных данных XML из скриптов WinRM</span><span class="sxs-lookup"><span data-stu-id="90ba3-125">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="90ba3-126">API сценариев WinRM получает и получает XML-строки, описывающие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="90ba3-126">The WinRM Scripting API gets and receives XML strings that describe resources.</span></span> <span data-ttu-id="90ba3-127">Результирующий XML-код представлен в виде текстового потока и требует, чтобы преобразование XML было представлено каким-либо другим способом.</span><span class="sxs-lookup"><span data-stu-id="90ba3-127">The resultant XML is in the form of a text stream and requires an XML transform to be displayed in some other way.</span></span>

<span data-ttu-id="90ba3-128">Следующий сценарий WinRM создает необработанные выходные данные в формате XML.</span><span class="sxs-lookup"><span data-stu-id="90ba3-128">The following WinRM script produces raw XML output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



<span data-ttu-id="90ba3-129">Следующий блок текста показывает выходные XML-данные сценария WinRM.</span><span class="sxs-lookup"><span data-stu-id="90ba3-129">The following block of text shows the XML output from the WinRM script.</span></span>


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



<span data-ttu-id="90ba3-130">Скрипты могут использовать преобразование XML, чтобы сделать эти выходные данные более удобочитаемыми.</span><span class="sxs-lookup"><span data-stu-id="90ba3-130">Your scripts can use an XML transform to make this output more readable.</span></span> <span data-ttu-id="90ba3-131">Дополнительные сведения см. [в разделе вывод XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="90ba3-131">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="90ba3-132">Следующая версия скрипта форматирует XML-код в виде выходного человека.</span><span class="sxs-lookup"><span data-stu-id="90ba3-132">The following version of the script formats the XML into human-readable output.</span></span>


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



<span data-ttu-id="90ba3-133">Преобразование «XSL» создает следующие выходные данные.</span><span class="sxs-lookup"><span data-stu-id="90ba3-133">The XSL transform creates the following output.</span></span>


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



## <a name="winrm-script-and-winrmcmd-output"></a><span data-ttu-id="90ba3-134">Сценарий WinRM и выходные данные WinRM. cmd</span><span class="sxs-lookup"><span data-stu-id="90ba3-134">WinRM Script and Winrm.cmd Output</span></span>

<span data-ttu-id="90ba3-135">Выходные данные сценария WinRM кодируются в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="90ba3-135">The output from a WinRM script is encoded in Unicode.</span></span> <span data-ttu-id="90ba3-136">При создании [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) и записи файла из скрипта полученный файл будет иметь кодировку Unicode.</span><span class="sxs-lookup"><span data-stu-id="90ba3-136">If you create a [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) and write a file from the script, the resulting file is Unicode.</span></span> <span data-ttu-id="90ba3-137">Однако при перенаправлении выходных данных в файл используется кодировка ANSI.</span><span class="sxs-lookup"><span data-stu-id="90ba3-137">However, if you redirect the output to a file, the encoding is ANSI.</span></span> <span data-ttu-id="90ba3-138">При перенаправлении выходных данных в XML-файл и наличии в выходных данных символов Юникода XML-код будет недопустимым.</span><span class="sxs-lookup"><span data-stu-id="90ba3-138">If you redirect the output to an XML file and there are Unicode characters in the output, the XML will be invalid.</span></span> <span data-ttu-id="90ba3-139">Имейте в виду, что программа командной строки **WinRM** выводит значение ANSI.</span><span class="sxs-lookup"><span data-stu-id="90ba3-139">Be aware that the **Winrm** command-line tool outputs ANSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90ba3-140">См. также</span><span class="sxs-lookup"><span data-stu-id="90ba3-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ba3-141">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="90ba3-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="90ba3-142">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="90ba3-142">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

<span data-ttu-id="90ba3-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90ba3-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="90ba3-144">[Справочник по модели DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90ba3-144">[DOM Reference](/previous-versions/windows/desktop/ms764730(v=vs.85))</span></span>
</dt> </dl>

 

 