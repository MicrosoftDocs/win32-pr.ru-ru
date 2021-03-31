---
title: Получение данных с локального компьютера
description: Хотя протокол служба удаленного управления Windows и WS-Management специально разработан для удаленного подключения, в самом простом случае устанавливается сеанс на локальном компьютере.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791706"
---
# <a name="obtaining-data-from-the-local-computer"></a><span data-ttu-id="ba864-103">Получение данных с локального компьютера</span><span class="sxs-lookup"><span data-stu-id="ba864-103">Obtaining Data from the Local Computer</span></span>

<span data-ttu-id="ba864-104">Хотя протокол служба удаленного управления Windows и WS-Management специально разработан для удаленного подключения, в самом простом случае устанавливается сеанс на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ba864-104">Although Windows Remote Management and WS-Management protocol are explicitly designed for remote communication, establishing a session on the local computer is the simplest case.</span></span> <span data-ttu-id="ba864-105">Для некоторых сценариев может потребоваться доступ к данным на локальном компьютере, а также к удаленным компьютерам.</span><span class="sxs-lookup"><span data-stu-id="ba864-105">Some scripts may require access data on the local computer as well as remote computers.</span></span>

<span data-ttu-id="ba864-106">**WinRM версии 2,0:  **</span><span class="sxs-lookup"><span data-stu-id="ba864-106">**WinRM version 2.0:  **</span></span>

<span data-ttu-id="ba864-107">Все операции считаются удаленными, и служба WinRM должна быть запущена до выполнения любой операции.</span><span class="sxs-lookup"><span data-stu-id="ba864-107">All operations are considered remote and the WinRM service must be started before any operation is performed.</span></span> <span data-ttu-id="ba864-108">Если удаленное назначение не указано, по умолчанию используется localhost, и все операции будут отправляться в локальную службу WinRM.</span><span class="sxs-lookup"><span data-stu-id="ba864-108">If a remote destination is not specified, then the localhost is used by default, and all operations will be sent to the local WinRM service.</span></span> <span data-ttu-id="ba864-109">Дополнительные сведения о запуске службы WinRM см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="ba864-109">For more information about starting the WinRM service, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="ba864-110">При использовании службы WinRM для локальных операций следует учитывать следующие факторы.</span><span class="sxs-lookup"><span data-stu-id="ba864-110">When using the WinRM service for local operations, the following factors should be considered:</span></span>

-   <span data-ttu-id="ba864-111">Локальная конфигурация WinRM может быть прочитана только администраторами.</span><span class="sxs-lookup"><span data-stu-id="ba864-111">The local WinRM configuration can only be read by administrators.</span></span>
-   <span data-ttu-id="ba864-112">Пространства имен WMI должны иметь набор разрешений Remote Enable.</span><span class="sxs-lookup"><span data-stu-id="ba864-112">WMI namespaces must have remote enable permissions set.</span></span> <span data-ttu-id="ba864-113">Дополнительные сведения см. [в разделе Защита удаленного WMI-подключения](../wmisdk/securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ba864-113">For more information, see [Securing a Remote WMI Connection](../wmisdk/securing-a-remote-wmi-connection.md).</span></span>
-   <span data-ttu-id="ba864-114">Если [*прослушиватель*](windows-remote-management-glossary.md) WinRM не создан, служба WinRM прослушивает локальные запросы через порт 47001.</span><span class="sxs-lookup"><span data-stu-id="ba864-114">If a WinRM [*listener*](windows-remote-management-glossary.md) is not created, then the WinRM service listens for local requests on port 47001.</span></span>

<span data-ttu-id="ba864-115">Каждый сценарий WinRM должен начаться с установления сеанса или соединения с компьютером путем создания объекта [**сеанса**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="ba864-115">Every WinRM script must start by establishing a session or connection to a computer by creating a [**Session**](session.md) object.</span></span> <span data-ttu-id="ba864-116">После создания сеанса можно использовать методы объекта **сеанса** , такие как [**Session. Enumerate**](session-enumerate.md) или [**Session. Invoke**](session-invoke.md) , для получения данных или для выполнения методов.</span><span class="sxs-lookup"><span data-stu-id="ba864-116">After the session is created, you can use the **Session** object methods, such as [**Session.Enumerate**](session-enumerate.md) or [**Session.Invoke**](session-invoke.md) to obtain data or to execute methods.</span></span>

<span data-ttu-id="ba864-117">Создание сеанса в некоторой степени похоже на [Подключение](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) к пространству имен инструментарий управления Windows (WMI) ([WMI](/windows/desktop/WmiSdk/wmi-start-page)).</span><span class="sxs-lookup"><span data-stu-id="ba864-117">The creation of a session is somewhat similar to [connecting](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) to a Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page)) namespace.</span></span> <span data-ttu-id="ba864-118">Сеанс по сути является слоем, который позволяет отправлять и получать данные через сообщения [*SOAP*](windows-remote-management-glossary.md) и протокол WS-Management.</span><span class="sxs-lookup"><span data-stu-id="ba864-118">The session is essentially a layer that allows you to send and receive data through [*SOAP*](windows-remote-management-glossary.md) messages and the WS-Management protocol.</span></span> <span data-ttu-id="ba864-119">Дополнительные сведения см. в разделе [протокол WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="ba864-119">For more information, see [WS-Management Protocol](ws-management-protocol.md).</span></span>

<span data-ttu-id="ba864-120">Вызов метода [**WSMan. CreateSession**](wsman-createsession.md) для создания объекта [**сеанса**](session.md) приведет к запуску [*сеанса*](windows-remote-management-glossary.md) , который подключается к локальному WinRM.</span><span class="sxs-lookup"><span data-stu-id="ba864-120">Calling the [**WSMan.CreateSession**](wsman-createsession.md) method to create a [**Session**](session.md) object will start a [*session*](windows-remote-management-glossary.md) that connects to the local WinRM.</span></span>

<span data-ttu-id="ba864-121">**Создание сеанса WSMan и получение данных**</span><span class="sxs-lookup"><span data-stu-id="ba864-121">**To Create a WSMan Session and Obtain Data**</span></span>

1.  <span data-ttu-id="ba864-122">Создайте объект [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="ba864-122">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="ba864-123">Создайте сеанс, вызвав метод [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="ba864-123">Create a session by calling the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="ba864-124">Этот сеанс выполняется с именем пользователя и паролем для входа и может получать данные через локальный WinRM.</span><span class="sxs-lookup"><span data-stu-id="ba864-124">This session runs under your logon username and password and can obtain data through the local WinRM.</span></span>

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  <span data-ttu-id="ba864-125">Создайте [*URI*](windows-remote-management-glossary.md) ресурса для определения [*ресурса*](windows-remote-management-glossary.md) , которым требуется управлять или для которого требуется получить данные.</span><span class="sxs-lookup"><span data-stu-id="ba864-125">Create a resource [*URI*](windows-remote-management-glossary.md) to identify the [*resource*](windows-remote-management-glossary.md) you want to manage or for which you want to obtain data.</span></span> <span data-ttu-id="ba864-126">Дополнительные сведения о форматировании URI см. в разделе [URI ресурсов](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="ba864-126">For more information about formatting a URI, see [Resource URIs](resource-uris.md).</span></span> <span data-ttu-id="ba864-127">Этот URI ресурса предназначен для конкретного экземпляра класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) WMI, службы Winmgmt.</span><span class="sxs-lookup"><span data-stu-id="ba864-127">This resource URI is for a specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the Winmgmt service.</span></span> <span data-ttu-id="ba864-128">Дополнительные сведения см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ba864-128">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  <span data-ttu-id="ba864-129">Вызывайте методы [**сеанса**](session.md) , которые получают или перечисляют данные с помощью URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba864-129">Call [**Session**](session.md) methods that get or enumerate data using the resource URI.</span></span> <span data-ttu-id="ba864-130">Дополнительные сведения см. в разделе [API сценариев WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ba864-130">For more information, see [WinRM Scripting API](winrm-scripting-api.md).</span></span>

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  <span data-ttu-id="ba864-131">Сведения о получении или управлении данными с другого компьютера или использовании различных методов проверки подлинности см. в разделе [Получение данных с удаленного компьютера](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="ba864-131">To get or manage data from another computer or use different methods of authentication, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span>

<span data-ttu-id="ba864-132">В следующем примере кода VBScript показан полный скрипт, который получает конкретный экземпляр [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) инструментария WMI с именем Winmgmt.</span><span class="sxs-lookup"><span data-stu-id="ba864-132">The following VBScript code example shows the complete script that obtains the specific instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) named "Winmgmt".</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



<span data-ttu-id="ba864-133">В следующем примере кода VBScript показан полный скрипт с преобразованием данных.</span><span class="sxs-lookup"><span data-stu-id="ba864-133">The following VBScript code example shows the complete script with the data transform.</span></span> <span data-ttu-id="ba864-134">Дополнительные сведения см. [в разделе вывод XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="ba864-134">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a><span data-ttu-id="ba864-135">См. также</span><span class="sxs-lookup"><span data-stu-id="ba864-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba864-136">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="ba864-136">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ba864-137">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="ba864-137">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ba864-138">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="ba864-138">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 