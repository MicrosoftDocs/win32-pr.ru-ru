---
description: Сценарии WMI могут быть уплотнены во многих шагах, необходимых для программы C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Подключение к WMI с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911515"
---
# <a name="connecting-to-wmi-with-vbscript"></a><span data-ttu-id="61b63-103">Подключение к WMI с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="61b63-103">Connecting to WMI with VBScript</span></span>

<span data-ttu-id="61b63-104">Сценарии WMI могут быть уплотнены во многих шагах, необходимых для программы C++.</span><span class="sxs-lookup"><span data-stu-id="61b63-104">WMI scripts can condense many of the steps required in a C++ program.</span></span> <span data-ttu-id="61b63-105">Они могут подключаться к WMI, не только через объект [**SWbemLocator**](swbemlocator.md) , но и через моникер "винмгмтс:".</span><span class="sxs-lookup"><span data-stu-id="61b63-105">They can connect to WMI, not only through an [**SWbemLocator**](swbemlocator.md) object, but also through the moniker "winmgmts:".</span></span> <span data-ttu-id="61b63-106">Моникер — это короткое имя, которое находит пространство имен, класс или экземпляр в WMI.</span><span class="sxs-lookup"><span data-stu-id="61b63-106">A moniker is a short name that locates a namespace, class, or instance in WMI.</span></span> <span data-ttu-id="61b63-107">Имя "винмгмтс:" является моникером WMI, сообщающим серверу сценариев Windows использовать объекты WMI, подключается к пространству имен по умолчанию и получает объект [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="61b63-107">The name "winmgmts:" is the WMI moniker that tells the Windows Script Host to use the WMI objects, connects to the default namespace, and obtains an [**SWbemServices**](swbemservices.md) object.</span></span> <span data-ttu-id="61b63-108">Другие сведения о соединении, например уровень олицетворения или конкретный класс или экземпляр, отображаются в строке после имени моникера.</span><span class="sxs-lookup"><span data-stu-id="61b63-108">Other connection information, such as an impersonation level or a specific class or instance, appears in the string following the moniker name.</span></span> <span data-ttu-id="61b63-109">Моникеры можно использовать в вызовах, которые создают или получают объекты WMI.</span><span class="sxs-lookup"><span data-stu-id="61b63-109">You can use monikers in calls that either create or get WMI objects.</span></span> <span data-ttu-id="61b63-110">Дополнительные сведения см. [в разделе Создание строки моникера](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="61b63-110">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>

<span data-ttu-id="61b63-111">В следующей процедуре описывается подключение к WMI с помощью **SWbemLocator**.</span><span class="sxs-lookup"><span data-stu-id="61b63-111">The following procedure describes how to connect to WMI using **SWbemLocator**.</span></span>

<span data-ttu-id="61b63-112">**Подключение к WMI с помощью SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="61b63-112">**To connect to WMI using SWbemLocator**</span></span>

1.  <span data-ttu-id="61b63-113">Получение объекта локатора с помощью вызова функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="61b63-113">Retrieve a locator object with a call to [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  <span data-ttu-id="61b63-114">Войдите в пространство имен, используя вызов метода [**коннектсервер**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="61b63-114">Log on to the namespace using a call to the [**ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    <span data-ttu-id="61b63-115">Если не указать компьютер в вызове [**коннектсервер**](swbemlocator-connectserver.md), WMI подключится к локальному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="61b63-115">If you do not specify a computer in the call to [**ConnectServer**](swbemlocator-connectserver.md), then WMI connects to the local computer.</span></span> <span data-ttu-id="61b63-116">Если не указать пространство имен, WMI подключится к пространству имен, указанному в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="61b63-116">If you do not specify a namespace, then WMI connects to the namespace specified in the registry key.</span></span>

    <span data-ttu-id="61b63-117">**HKey \_ \_** \\  \\  \\  \\  \\ **Пространство имен по умолчанию** сценариев Microsoft WBEM по локальному компьютеру</span><span class="sxs-lookup"><span data-stu-id="61b63-117">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**</span></span>

    <span data-ttu-id="61b63-118">Пространством имен по умолчанию является \\ root \\ CIMV2.</span><span class="sxs-lookup"><span data-stu-id="61b63-118">The default namespace is \\root\\cimv2.</span></span> <span data-ttu-id="61b63-119">Дополнительные сведения о пространствах имен см. [в разделе Создание иерархий в WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="61b63-119">For more information about namespaces, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

3.  <span data-ttu-id="61b63-120">Задайте уровень олицетворения с помощью вызова метода [**SwbemServices. Security \_**](swbemservices-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="61b63-120">Set the impersonation level with a call to the [**SWbemServices.Security\_**](swbemservices-security-.md) method.</span></span>

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    <span data-ttu-id="61b63-121">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="61b63-121">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

4.  <span data-ttu-id="61b63-122">Реализуйте назначение сценария.</span><span class="sxs-lookup"><span data-stu-id="61b63-122">Implement the purpose of your script.</span></span>

    <span data-ttu-id="61b63-123">Инструментарий WMI предоставляет разнообразные объекты сценариев, которые используются для доступа к данным по сети и управления ими.</span><span class="sxs-lookup"><span data-stu-id="61b63-123">WMI exposes a variety of scripting objects that use to access and manipulate data across your network.</span></span> <span data-ttu-id="61b63-124">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md) и [API сценариев для WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="61b63-124">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

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

    

<span data-ttu-id="61b63-125">Следующая процедура описывает, как подключиться к инструментарию WMI и получить объект с помощью моникера.</span><span class="sxs-lookup"><span data-stu-id="61b63-125">The following procedure describes how to connect to WMI and retrieve an object using a moniker.</span></span>

<span data-ttu-id="61b63-126">**Подключение к инструментарию WMI и получение объекта с помощью моникера**</span><span class="sxs-lookup"><span data-stu-id="61b63-126">**To connect to WMI and retrieve an object using a moniker**</span></span>

1.  <span data-ttu-id="61b63-127">Вызовите [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) с моникером во входном параметре.</span><span class="sxs-lookup"><span data-stu-id="61b63-127">Call [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) with a moniker in the input parameter.</span></span>

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    <span data-ttu-id="61b63-128">Моиникер содержит ряд элементов, которые можно использовать для подключения к WMI:</span><span class="sxs-lookup"><span data-stu-id="61b63-128">The moiniker contains a number of elements that you can use to connect to WMI:</span></span>

    -   <span data-ttu-id="61b63-129">"Винмгмтс:" указывает WSH использовать [объекты API скриптов](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="61b63-129">The "winmgmts:" tells WSH to use [Scripting API objects](scripting-api-objects.md).</span></span> <span data-ttu-id="61b63-130">В этом конкретном примере сервер WSH будет иметь представление о том, что он должен возвращать SWbemObject, описывающий первый \_ ScheduledJob Win32 в системе.</span><span class="sxs-lookup"><span data-stu-id="61b63-130">In this particular example, the WSH will know that it should return an SWbemObject that describes the first Win32\_scheduledJob on the system.</span></span> <span data-ttu-id="61b63-131">Другие возможные объекты для возврата — это объект Свбемколлектион или [**SwbemServices**](swbemservices.md) , в зависимости от того, что описано в описании моникера.</span><span class="sxs-lookup"><span data-stu-id="61b63-131">Other possible objects to return would be an SWbemCollection or an [**SWbemServices**](swbemservices.md) object, depending on what the moniker described.</span></span>

    -   <span data-ttu-id="61b63-132">При необходимости можно задать уровни безопасности для соединения.</span><span class="sxs-lookup"><span data-stu-id="61b63-132">You can optionally set the security levels for the connection.</span></span> <span data-ttu-id="61b63-133">Обратите внимание, что в моникере нельзя задавать сведения о имени и пароле.</span><span class="sxs-lookup"><span data-stu-id="61b63-133">Note that you cannot set name and password information in a moniker, however.</span></span> <span data-ttu-id="61b63-134">Дополнительные сведения см. в разделе [Защита скриптов для клиентов](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="61b63-134">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    -   <span data-ttu-id="61b63-135">При необходимости можно определить путь к объекту WMI.</span><span class="sxs-lookup"><span data-stu-id="61b63-135">You can optionally define the path to the WMI object.</span></span> <span data-ttu-id="61b63-136">Сюда входит либо локальный, либо удаленный компьютер, пространство имен, а также имя класса.</span><span class="sxs-lookup"><span data-stu-id="61b63-136">This includes either the local or remote computer, the namespace, as well as the name of the class.</span></span> <span data-ttu-id="61b63-137">Дополнительные сведения об использовании [**объектов**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) VBScript в скриптах WMI см. в разделе [Создание экземпляра](creating-an-instance.md) и [Получение экземпляра WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="61b63-137">For more information about using the VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI scripts, see [Creating an Instance](creating-an-instance.md) and [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="61b63-138">Вместо получения одного элемента или коллекции можно также выбрать извлечение объекта [**SwbemServices**](swbemservices.md) (как описано в предыдущем примере).</span><span class="sxs-lookup"><span data-stu-id="61b63-138">Instead of retrieving a single item or collection, you can also choose to retrieve the [**SWbemServices**](swbemservices.md) object (as described in the previous example).</span></span> <span data-ttu-id="61b63-139">После этого можно вызвать дополнительные запросы к возвращенному объекту.</span><span class="sxs-lookup"><span data-stu-id="61b63-139">Afterwards, you can then call additional queries on the returned object.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    <span data-ttu-id="61b63-140">В предыдущем примере олицетворение или Имперсонатионлевел = 3 является уровнем безопасности процесса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61b63-140">In the previous example, impersonate, or impersonationLevel=3, is the default process security level.</span></span> <span data-ttu-id="61b63-141">В следующем примере нет необходимости указывать этот уровень безопасности процесса, если только не требуется изменить безопасность процесса на **Делегирование**.</span><span class="sxs-lookup"><span data-stu-id="61b63-141">In the following example, it is not necessary to specify this process security level unless you need to change the process security to **delegate**.</span></span> <span data-ttu-id="61b63-142">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="61b63-142">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61b63-143">См. также</span><span class="sxs-lookup"><span data-stu-id="61b63-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61b63-144">Создание сценариев в WMI</span><span class="sxs-lookup"><span data-stu-id="61b63-144">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
