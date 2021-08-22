---
description: Сценарии WMI могут быть уплотнены во многих шагах, необходимых для программы C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Подключение к WMI с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b4e71f4225a55e24432562d4c35754080b9746386489b7dbf7061cb65c9771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131616"
---
# <a name="connecting-to-wmi-with-vbscript"></a>Подключение к WMI с помощью VBScript

Сценарии WMI могут быть уплотнены во многих шагах, необходимых для программы C++. Они могут подключаться к WMI, не только через объект [**SWbemLocator**](swbemlocator.md) , но и через моникер "винмгмтс:". Моникер — это короткое имя, которое находит пространство имен, класс или экземпляр в WMI. имя "винмгмтс:" является моникером WMI, сообщающим серверу сценариев Windows использовать объекты WMI, подключается к пространству имен по умолчанию и получает объект [**SWbemServices**](swbemservices.md) . Другие сведения о соединении, например уровень олицетворения или конкретный класс или экземпляр, отображаются в строке после имени моникера. Моникеры можно использовать в вызовах, которые создают или получают объекты WMI. Дополнительные сведения см. [в разделе Создание строки моникера](constructing-a-moniker-string.md).

В следующей процедуре описывается подключение к WMI с помощью **SWbemLocator**.

**Подключение к WMI с помощью SWbemLocator**

1.  Получение объекта локатора с помощью вызова функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Войдите в пространство имен, используя вызов метода [**коннектсервер**](swbemlocator-connectserver.md) .

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Если не указать компьютер в вызове [**коннектсервер**](swbemlocator-connectserver.md), WMI подключится к локальному компьютеру. Если не указать пространство имен, WMI подключится к пространству имен, указанному в разделе реестра.

    **HKey \_ \_** \\  \\  \\  \\  \\ **Пространство имен по умолчанию** сценариев Microsoft WBEM по локальному компьютеру

    Пространством имен по умолчанию является \\ root \\ CIMV2. Дополнительные сведения о пространствах имен см. [в разделе Создание иерархий в WMI](creating-hierarchies-within-wmi.md).

3.  Задайте уровень олицетворения с помощью вызова метода [**SwbemServices. Security \_**](swbemservices-security-.md) .

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).

4.  Реализуйте назначение сценария.

    Инструментарий WMI предоставляет разнообразные объекты сценариев, которые используются для доступа к данным по сети и управления ими. Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md) и [API сценариев для WMI](scripting-api-for-wmi.md).

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

Следующая процедура описывает, как подключиться к инструментарию WMI и получить объект с помощью моникера.

**Подключение к инструментарию WMI и получение объекта с помощью моникера**

1.  Вызовите [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) с моникером во входном параметре.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    Моиникер содержит ряд элементов, которые можно использовать для подключения к WMI:

    -   "Винмгмтс:" указывает WSH использовать [объекты API скриптов](scripting-api-objects.md). В этом конкретном примере сервер WSH будет иметь представление о том, что он должен возвращать SWbemObject, описывающий первый \_ ScheduledJob Win32 в системе. Другие возможные объекты для возврата — это объект Свбемколлектион или [**SwbemServices**](swbemservices.md) , в зависимости от того, что описано в описании моникера.

    -   При необходимости можно задать уровни безопасности для соединения. Обратите внимание, что в моникере нельзя задавать сведения о имени и пароле. Дополнительные сведения см. в разделе [Защита скриптов для клиентов](securing-scripting-clients.md).

    -   При необходимости можно определить путь к объекту WMI. Сюда входит либо локальный, либо удаленный компьютер, пространство имен, а также имя класса. Дополнительные сведения об использовании [**объектов**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) VBScript в скриптах WMI см. в разделе [Создание экземпляра](creating-an-instance.md) и [Получение экземпляра WMI](retrieving-an-instance.md).

2.  Вместо получения одного элемента или коллекции можно также выбрать извлечение объекта [**SwbemServices**](swbemservices.md) (как описано в предыдущем примере). После этого можно вызвать дополнительные запросы к возвращенному объекту.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    В предыдущем примере олицетворение или Имперсонатионлевел = 3 является уровнем безопасности процесса по умолчанию. В следующем примере нет необходимости указывать этот уровень безопасности процесса, если только не требуется изменить безопасность процесса на **Делегирование**. Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
