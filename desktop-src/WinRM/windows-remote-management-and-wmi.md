---
title: служба удаленного управления Windows и WMI
description: Служба удаленного управления Windows можно использовать для получения данных, предоставляемых инструментарий управления Windows (WMI).
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105693938"
---
# <a name="windows-remote-management-and-wmi"></a><span data-ttu-id="e51c3-103">служба удаленного управления Windows и WMI</span><span class="sxs-lookup"><span data-stu-id="e51c3-103">Windows Remote Management and WMI</span></span>

<span data-ttu-id="e51c3-104">Служба удаленного управления Windows можно использовать для получения данных, предоставляемых инструментарий управления Windows (WMI) ([WMI](/windows/desktop/WmiSdk/wmi-start-page) и [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span><span class="sxs-lookup"><span data-stu-id="e51c3-104">Windows Remote Management can be used to retrieve data exposed by Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) and [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span></span> <span data-ttu-id="e51c3-105">Данные WMI можно получить с помощью скриптов или приложений, использующих [API-интерфейсы WinRM](winrm-scripting-api.md) или с помощью программы командной строки **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="e51c3-105">You can obtain WMI data with scripts or applications that use the [WinRM Scripting API](winrm-scripting-api.md) or through the **Winrm** command-line tool.</span></span>

<span data-ttu-id="e51c3-106">WinRM поддерживает большинство знакомых классов и операций WMI, включая внедренные объекты.</span><span class="sxs-lookup"><span data-stu-id="e51c3-106">WinRM supports most of the familiar WMI classes and operations, including embedded objects.</span></span> <span data-ttu-id="e51c3-107">WinRM может использовать инструментарий WMI для получения данных о [*ресурсах*](windows-remote-management-glossary.md) или управлении ресурсами в операционной системе на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="e51c3-107">WinRM can leverage WMI to collect data about [*resources*](windows-remote-management-glossary.md) or to manage resources on a Windows-based operating system.</span></span> <span data-ttu-id="e51c3-108">Это означает, что вы можете получать данные об объектах, таких как диски, сетевые адаптеры, службы или процессы в Организации, с помощью существующего набора [классов WMI](/windows/desktop/WmiSdk/wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="e51c3-108">That means that you can obtain data about objects such as disks, network adapters, services, or processes in your enterprise through the existing set of [WMI classes](/windows/desktop/WmiSdk/wmi-classes).</span></span> <span data-ttu-id="e51c3-109">Вы также можете получить доступ к данным оборудования, доступным в стандартном [поставщике IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.</span><span class="sxs-lookup"><span data-stu-id="e51c3-109">You can also access the hardware data that is available from the standard WMI [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

## <a name="identifying-a-wmi-resource"></a><span data-ttu-id="e51c3-110">Определение ресурса WMI</span><span class="sxs-lookup"><span data-stu-id="e51c3-110">Identifying a WMI Resource</span></span>

<span data-ttu-id="e51c3-111">Вы можете ссылаться на класс WMI в качестве [*ресурса*](windows-remote-management-glossary.md) в WinRM и в протоколе WS-Management: тип управляемого объекта, например службы или диска.</span><span class="sxs-lookup"><span data-stu-id="e51c3-111">You can reference a WMI class as a [*resource*](windows-remote-management-glossary.md) in WinRM and in the WS-Management protocol: a type of managed entity, like a service or a disk.</span></span>

<span data-ttu-id="e51c3-112">Класс или метод WMI идентифицируется по [*универсальному коду ресурса (URI*](windows-remote-management-glossary.md)), как и любой другой ресурс при использовании протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="e51c3-112">A WMI class or method is identified by a [*URI*](windows-remote-management-glossary.md), just as any other resource is when using the WS-Management protocol.</span></span> <span data-ttu-id="e51c3-113">Универсальный код ресурса (URI) может указывать ресурс WMI (класс), действие WMI (метод) или определять конкретный экземпляр класса в [*сообщениях*](windows-remote-management-glossary.md) , отправляемых по сети.</span><span class="sxs-lookup"><span data-stu-id="e51c3-113">The URI can specify a WMI resource (class), a WMI action (method), or identify a specific instance of a class in [*messages*](windows-remote-management-glossary.md) sent over a network.</span></span> <span data-ttu-id="e51c3-114">Дополнительные сведения см. в разделе [URI ресурсов](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="e51c3-114">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a><span data-ttu-id="e51c3-115">Создание префикса URI для классов WMI</span><span class="sxs-lookup"><span data-stu-id="e51c3-115">Constructing the URI Prefix for WMI Classes</span></span>

<span data-ttu-id="e51c3-116">Префикс URI содержит фиксированную часть и пространство имен WMI.</span><span class="sxs-lookup"><span data-stu-id="e51c3-116">The URI prefix contains a fixed part and the WMI namespace.</span></span> <span data-ttu-id="e51c3-117">Например, префикс URI в Windows Server, содержащий фиксированную часть префикса, — это: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` .</span><span class="sxs-lookup"><span data-stu-id="e51c3-117">For example, the URI prefix in Windows Server that contains the fixed part of the prefix is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>`.</span></span> <span data-ttu-id="e51c3-118">Это позволяет создать префикс URI для любого пространства имен WMI.</span><span class="sxs-lookup"><span data-stu-id="e51c3-118">This allows the URI prefix to be generated for any WMI namespace.</span></span> <span data-ttu-id="e51c3-119">Например, чтобы получить доступ к корневому пространству имен WMI **\\ по умолчанию** , используйте следующий префикс URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .</span><span class="sxs-lookup"><span data-stu-id="e51c3-119">For example, to access the **root\\default** WMI namespace, use the following URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/`.</span></span>

<span data-ttu-id="e51c3-120">Большинство классов WMI для управления находятся в корневом пространстве имен **\\ CIMV2** .</span><span class="sxs-lookup"><span data-stu-id="e51c3-120">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="e51c3-121">Чтобы получить доступ к классам и экземплярам в **корневом пространстве имен \\ CIMV2** , используйте префикс URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` .</span><span class="sxs-lookup"><span data-stu-id="e51c3-121">To access classes and instances in **root\\cimv2** namespace, use the URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`.</span></span> <span data-ttu-id="e51c3-122">Дополнительные сведения см. в разделе [URI ресурсов](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="e51c3-122">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="generating-a-complete-uri-for-wmi-classes"></a><span data-ttu-id="e51c3-123">Создание полного URI для классов WMI</span><span class="sxs-lookup"><span data-stu-id="e51c3-123">Generating a Complete URI for WMI Classes</span></span>

<span data-ttu-id="e51c3-124">Предоставленный универсальный код ресурса (URI) для программы командной строки **WinRM** или скрипта состоит из префикса и спецификации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e51c3-124">The URI that you supply, either to the **Winrm** command-line tool or to a script, consists of the prefix plus the resource specification.</span></span>

<span data-ttu-id="e51c3-125">В следующей процедуре описывается создание URI ресурса для получения класса WMI или для использования в операции перечисления.</span><span class="sxs-lookup"><span data-stu-id="e51c3-125">The following procedure describes how to generate a resource URI either to get a WMI class or to use in an enumerate operation.</span></span>

<span data-ttu-id="e51c3-126">**Создание URI ресурса для класса WMI**</span><span class="sxs-lookup"><span data-stu-id="e51c3-126">**To generate a resource URI for a WMI class**</span></span>

1.  <span data-ttu-id="e51c3-127">Начните с префикса, указывающего на необходимость использования схемы протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="e51c3-127">Start with the prefix that indicates the WS-Management protocol schema should be used.</span></span>

    https://schemas.microsoft.com/wbem/wsman/1

    <span data-ttu-id="e51c3-128">Префикс URI ресурса для классов WMI всегда совпадает.</span><span class="sxs-lookup"><span data-stu-id="e51c3-128">The resource URI prefix for WMI classes is always the same.</span></span> <span data-ttu-id="e51c3-129">Дополнительные сведения см. в разделе [префиксы URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="e51c3-129">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

2.  <span data-ttu-id="e51c3-130">Добавьте пространство имен WMI к префиксу.</span><span class="sxs-lookup"><span data-stu-id="e51c3-130">Add the WMI namespace to the prefix.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  <span data-ttu-id="e51c3-131">Добавьте имя класса.</span><span class="sxs-lookup"><span data-stu-id="e51c3-131">Add the class name.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  <span data-ttu-id="e51c3-132">Чтобы задать значение свойства или вызвать конкретный метод, добавьте требуемое значение ключа или значения для класса.</span><span class="sxs-lookup"><span data-stu-id="e51c3-132">To set the value of a property, or to invoke a specific method, add the required key value or values for the class.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    <span data-ttu-id="e51c3-133">Если оставить значение ключа пустым, исходное значение свойства не будет изменено.</span><span class="sxs-lookup"><span data-stu-id="e51c3-133">If you leave the key value blank, you will not alter the original property value.</span></span>

    > [!Note]  
    > <span data-ttu-id="e51c3-134">Если оставить значение ключа пустым, значение свойства будет равно **null**.</span><span class="sxs-lookup"><span data-stu-id="e51c3-134">Leaving the key value blank sets the property value to **NULL**.</span></span>

     

## <a name="locating-a-wmi-resource-with-winrm"></a><span data-ttu-id="e51c3-135">Поиск ресурса WMI с помощью WinRM</span><span class="sxs-lookup"><span data-stu-id="e51c3-135">Locating a WMI Resource with WinRM</span></span>

<span data-ttu-id="e51c3-136">Данные WMI можно получить с помощью программы командной строки, **WinRM** или скрипта Visual Basic, использующего [API-интерфейс для сценариев WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e51c3-136">You can obtain WMI data either through the command-line tool, **Winrm**, or through a Visual Basic script that uses the [WinRM Scripting API](winrm-scripting-api.md).</span></span> <span data-ttu-id="e51c3-137">Не используйте [путь WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) для поиска ресурса.</span><span class="sxs-lookup"><span data-stu-id="e51c3-137">You do not use a [WMI path](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) to locate a resource.</span></span> <span data-ttu-id="e51c3-138">Вместо этого необходимо преобразовать пространство имен и иерархию WMI в [*универсальный код ресурса (URI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="e51c3-138">Instead, you convert the WMI namespace and hierarchy to a [*URI*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="e51c3-139">URI WinRM для класса WMI содержит две части: [префикс URI](uri-prefixes.md) и класс, к которому требуется получить доступ.</span><span class="sxs-lookup"><span data-stu-id="e51c3-139">The WinRM URI for a WMI class contains two parts: the [URI prefix](uri-prefixes.md) and the class that you want to access.</span></span>

<span data-ttu-id="e51c3-140">Например, следующий универсальный код ресурса (URI) может быть передано методу [**Session. Enumerate**](session-enumerate.md) для вывода списка всех служб на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e51c3-140">For example, the following URI can be supplied to the [**Session.Enumerate**](session-enumerate.md) method to list all the services on a computer.</span></span> <span data-ttu-id="e51c3-141">Префикс URI — `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , а класс — [**\_ служба Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="e51c3-141">The URI prefix is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`, and the class is [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

<span data-ttu-id="e51c3-142">В инструментарии WMI перечислите данные для всех экземпляров ресурса или класса несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="e51c3-142">In WMI, list the data for all of the instances of a resource or class in several ways:</span></span>

-   <span data-ttu-id="e51c3-143">Запрос для всех экземпляров этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="e51c3-143">A query for all the instances of that resource.</span></span>

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   <span data-ttu-id="e51c3-144">Вызов [**SwbemServices. инстанцесоф**](/windows/desktop/WmiSdk/swbemservices-instancesof) или [**\_ SWbemObject. Instances**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="e51c3-144">A call to [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) or [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span>

    `Set colServices = InstancesOf("Win32_Service")`

<span data-ttu-id="e51c3-145">В WinRM существует один способ перечисления всех экземпляров ресурса: [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="e51c3-145">In WinRM, there is one way to list all of the instances of a resource: [**Session.Enumerate**](session-enumerate.md).</span></span>


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a><span data-ttu-id="e51c3-146">Поиск конкретного экземпляра ресурса WMI</span><span class="sxs-lookup"><span data-stu-id="e51c3-146">Locating a Specific Instance of a WMI Resource</span></span>

<span data-ttu-id="e51c3-147">В инструментарии WMI можно назначить определенный экземпляр класса либо путем указания значений для ключевых свойств, либо путем запроса экземпляра, который соответствует списку значений свойств.</span><span class="sxs-lookup"><span data-stu-id="e51c3-147">In WMI, you can designate a particular instance of a class either by specifying values for the key properties or by querying for an instance that matches a list of property values.</span></span> <span data-ttu-id="e51c3-148">Ключевые свойства имеют [**квалификатор ключа**](/windows/desktop/WmiSdk/key-qualifier)WMI.</span><span class="sxs-lookup"><span data-stu-id="e51c3-148">Key properties have the WMI [**Key qualifier**](/windows/desktop/WmiSdk/key-qualifier).</span></span>

<span data-ttu-id="e51c3-149">Получить конкретный экземпляр класса можно несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="e51c3-149">You can obtain a specific instance of a class in several ways:</span></span>

-   <span data-ttu-id="e51c3-150">Вызов [**Session. Enumerate**](session-enumerate.md) с параметрами *Filter* и *диалект* для создания запроса.</span><span class="sxs-lookup"><span data-stu-id="e51c3-150">A call to [**Session.Enumerate**](session-enumerate.md) with the *filter* and *dialect* parameters to create a query.</span></span>

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   <span data-ttu-id="e51c3-151">Вызов [**SwbemServices. Get**](/windows/desktop/WmiSdk/swbemservices-get).</span><span class="sxs-lookup"><span data-stu-id="e51c3-151">A call to [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get).</span></span> <span data-ttu-id="e51c3-152">Для [**сеанса. Get**](session-get.md)необходимо указать одно или несколько конкретных ключевых значений, перед которыми стоит вопросительный знак (?).</span><span class="sxs-lookup"><span data-stu-id="e51c3-152">For [**Session.Get**](session-get.md), you must supply one or more specific key values, preceded by a question mark (?).</span></span>

    <span data-ttu-id="e51c3-153">Формат URI для конкретного экземпляра — `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .</span><span class="sxs-lookup"><span data-stu-id="e51c3-153">The format of the URI for a specific instance is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    <span data-ttu-id="e51c3-154">Класс WMI может иметь более одного ключа.</span><span class="sxs-lookup"><span data-stu-id="e51c3-154">A WMI class may have more than one key.</span></span> <span data-ttu-id="e51c3-155">Пары "имя-значение" ключа разделяются знаком "+".</span><span class="sxs-lookup"><span data-stu-id="e51c3-155">Key name-value pairs are separated by a "+" sign.</span></span> <span data-ttu-id="e51c3-156">В этом случае используется формат: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .</span><span class="sxs-lookup"><span data-stu-id="e51c3-156">In that case, the format is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2`.</span></span>

    <span data-ttu-id="e51c3-157">Синтаксис WinRM для получения Singleton-объекта WMI отличается от WMI.</span><span class="sxs-lookup"><span data-stu-id="e51c3-157">The WinRM syntax to obtain a singleton WMI object is different from WMI.</span></span> <span data-ttu-id="e51c3-158">Singleton — это класс WMI, определенный таким образом, что допускается только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e51c3-158">A singleton is a WMI class defined so that only one instance is allowed.</span></span> <span data-ttu-id="e51c3-159">[**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) или [**Win32 \_ вмисеттинг**](/windows/desktop/CIMWin32Prov/win32-wmisetting) являются примерами одноэлементного класса WMI.</span><span class="sxs-lookup"><span data-stu-id="e51c3-159">[**Win32\_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) or [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) are examples of a WMI singleton class.</span></span>

    <span data-ttu-id="e51c3-160">Синтаксис WMI для Singleton показан в следующем примере кода VBScript.</span><span class="sxs-lookup"><span data-stu-id="e51c3-160">The WMI syntax for singletons is shown in the following VBScript code example.</span></span>

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    <span data-ttu-id="e51c3-161">В следующем примере показан одноэлементный синтаксис WinRM, в котором не используется символ "@".</span><span class="sxs-lookup"><span data-stu-id="e51c3-161">The following example shows the WinRM singleton syntax which does not use "@".</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   <span data-ttu-id="e51c3-162">Добавление [*селектора*](windows-remote-management-glossary.md) к объекту [**ResourceLocator**](resourcelocator.md) или [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .</span><span class="sxs-lookup"><span data-stu-id="e51c3-162">Adding a [*selector*](windows-remote-management-glossary.md) to a [**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object.</span></span>

    <span data-ttu-id="e51c3-163">В следующем примере кода VBScript показано, как использовать селектор для получения конкретного экземпляра [**\_ процессора Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="e51c3-163">The following VBScript code example shows how to use a selector to get a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e51c3-164">См. также</span><span class="sxs-lookup"><span data-stu-id="e51c3-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e51c3-165">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="e51c3-165">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="e51c3-166">Префиксы URI</span><span class="sxs-lookup"><span data-stu-id="e51c3-166">URI Prefixes</span></span>](uri-prefixes.md)
</dt> <dt>

[<span data-ttu-id="e51c3-167">URI ресурсов</span><span class="sxs-lookup"><span data-stu-id="e51c3-167">Resource URIs</span></span>](resource-uris.md)
</dt> <dt>

[<span data-ttu-id="e51c3-168">Создание сценариев в служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="e51c3-168">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>
