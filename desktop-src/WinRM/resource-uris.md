---
title: URI ресурсов
description: URI ресурса — это идентификатор для отдельного типа операции управления или значение, используемое службами управления, которые реализуют протокол WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533197"
---
# <a name="resource-uris"></a><span data-ttu-id="2055f-103">URI ресурсов</span><span class="sxs-lookup"><span data-stu-id="2055f-103">Resource URIs</span></span>

<span data-ttu-id="2055f-104">[*URI ресурса*](windows-remote-management-glossary.md) — это идентификатор для отдельного типа операции управления или значение, используемое службами управления, которые реализуют протокол WS-Management.</span><span class="sxs-lookup"><span data-stu-id="2055f-104">A [*resource URI*](windows-remote-management-glossary.md) is an identifier for a distinct type of management operation or value used by management services that implement the WS-Management protocol.</span></span> <span data-ttu-id="2055f-105">Значением управления может быть температура внутри компьютера.</span><span class="sxs-lookup"><span data-stu-id="2055f-105">A management value could be the temperature inside a computer.</span></span> <span data-ttu-id="2055f-106">Примером операции управления является запуск остановленной службы или задание квоты пользователя на дисковый том.</span><span class="sxs-lookup"><span data-stu-id="2055f-106">An example of a management operation is starting a stopped service or setting a disk volume user quota.</span></span>

## <a name="resource-uri-format"></a><span data-ttu-id="2055f-107">Формат URI ресурса</span><span class="sxs-lookup"><span data-stu-id="2055f-107">Resource URI Format</span></span>

<span data-ttu-id="2055f-108">URI состоит из префикса и пути к ресурсу, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="2055f-108">A URI consists of a prefix and a path to a resource as is shown in the following example:</span></span>

<span data-ttu-id="2055f-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span><span class="sxs-lookup"><span data-stu-id="2055f-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span></span>

<span data-ttu-id="2055f-110">Эта спецификация схемы указывает на то, что универсальный код ресурса (URI) основан на версии 1 официального протокола WS-Management и что ресурс является [**консолью Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в \\ пространстве имен root cimv2 репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="2055f-110">This schema specification indicates that the URI is based on version 1 of the official WS-Management protocol and that the resource is a [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in the "root\\cimv2" namespace of the WMI repository.</span></span> <span data-ttu-id="2055f-111">Префиксы URI содержат спецификацию схемы, например "schemas.microsoft.com/wbem/wsman/1/wmi", и конкретный тип ресурса, например **Win32 \_ LogicalDisk**.</span><span class="sxs-lookup"><span data-stu-id="2055f-111">URI prefixes contain a schema specification, such as "schemas.microsoft.com/wbem/wsman/1/wmi" and a specific type of resource, such as **Win32\_LogicalDisk**.</span></span> <span data-ttu-id="2055f-112">Дополнительные сведения об идентификации конкретного экземпляра класса WMI см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2055f-112">For more information about identifying a specific instance of a WMI class, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="2055f-113">Дополнительные сведения см. в разделе [префиксы URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="2055f-113">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

## <a name="types-of-resource-uris"></a><span data-ttu-id="2055f-114">Типы URI ресурсов</span><span class="sxs-lookup"><span data-stu-id="2055f-114">Types of Resource URIs</span></span>

<span data-ttu-id="2055f-115">Хотя [*инструментарий управления Windows (WMI) (WMI)*](windows-remote-management-glossary.md) является основным источником данных управления для операционных систем на основе Windows, также существуют и другие источники схемы управления.</span><span class="sxs-lookup"><span data-stu-id="2055f-115">While [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) is the primary source of management data for Windows-based operating systems, other sources of management schema also exist.</span></span>

<span data-ttu-id="2055f-116">В следующем списке описываются несколько типов URI ресурсов, используемых служба удаленного управления Windows.</span><span class="sxs-lookup"><span data-stu-id="2055f-116">The following list describes several types of resource URIs used by Windows Remote Management:</span></span>

-   <span data-ttu-id="2055f-117">URI WMI</span><span class="sxs-lookup"><span data-stu-id="2055f-117">WMI URIs</span></span>

    <span data-ttu-id="2055f-118">Эта группа URI представляет собой [*модель CIM*](/windows/desktop/WmiSdk/gloss-c) путь к классу, включающий пространство имен и класс.</span><span class="sxs-lookup"><span data-stu-id="2055f-118">This group of URIs represent a [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) class path which includes namespace and class.</span></span>

    <span data-ttu-id="2055f-119">URI WMI можно использовать в:</span><span class="sxs-lookup"><span data-stu-id="2055f-119">WMI URIs can be used in:</span></span>

    -   <span data-ttu-id="2055f-120">Методы [**сеанса**](session.md)</span><span class="sxs-lookup"><span data-stu-id="2055f-120">[**Session**](session.md) methods</span></span>
    -   <span data-ttu-id="2055f-121">Методы [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="2055f-121">[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) methods</span></span>
    -   <span data-ttu-id="2055f-122">Методы [**WSMan. креатересаурцелокатор**](wsman-createresourcelocator.md) или [**ивсман. креатересаурцелокатор**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="2055f-122">[**WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) or [**IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) methods</span></span>
    -   <span data-ttu-id="2055f-123">Методы [**ResourceLocator**](resourcelocator.md) или [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="2055f-123">[**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) methods</span></span>

-   <span data-ttu-id="2055f-124">URI IPMI</span><span class="sxs-lookup"><span data-stu-id="2055f-124">IPMI URIs</span></span>

    <span data-ttu-id="2055f-125">Эта группа URI представляет стандартные универсальные коды ресурса (URI) на основе CIM версии 2,9.</span><span class="sxs-lookup"><span data-stu-id="2055f-125">This group of URIs represent industry standard URIs based upon CIM version 2.9.</span></span> <span data-ttu-id="2055f-126">URI IPMI можно использовать в методах сеанса [**Get**](session-get.md), [**WHERE**](session-put.md), [**Enumerate**](session-enumerate.md) и [](session.md) [**Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="2055f-126">IPMI URIs can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) , and [**Invoke**](session-invoke.md).</span></span>

    <span data-ttu-id="2055f-127">Например, https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span><span class="sxs-lookup"><span data-stu-id="2055f-127">An example is https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span></span> <span data-ttu-id="2055f-128">Этот ресурс определяется в соответствии со схемой CIM [DMTF.org](https://www.dmtf.org/home) .</span><span class="sxs-lookup"><span data-stu-id="2055f-128">This resource is defined according to the [DMTF.org](https://www.dmtf.org/home) CIM schema.</span></span>

-   <span data-ttu-id="2055f-129">URI конфигурации WinRM</span><span class="sxs-lookup"><span data-stu-id="2055f-129">WinRM configuration URIs</span></span>

    <span data-ttu-id="2055f-130">Эта группа URI — это операции настройки для конфигурации [*прослушивателя*](windows-remote-management-glossary.md) WinRM.</span><span class="sxs-lookup"><span data-stu-id="2055f-130">This group of URIs are configuration operations for the WinRM [*listener*](windows-remote-management-glossary.md) configuration.</span></span>

    <span data-ttu-id="2055f-131"> https://schemas.microsoft.com/wbem/wsman/1/config/listener может использоваться в методах [**сеанса**](session.md) [**Get**](session-get.md), [**помещает**](session-put.md), [**создает**](session-create.md), [**удаляет**](session-delete.md)и [**перечисляет**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="2055f-131">https://schemas.microsoft.com/wbem/wsman/1/config/listener can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md), and [**Enumerate**](session-enumerate.md).</span></span>

-   <span data-ttu-id="2055f-132">URI [*журнала системных событий*](windows-remote-management-glossary.md) (SEL)</span><span class="sxs-lookup"><span data-stu-id="2055f-132">[*System Event Log*](windows-remote-management-glossary.md) (SEL) URIs</span></span>

    <span data-ttu-id="2055f-133">Эта группа URI подписывается на события сборщика событий из BMC.</span><span class="sxs-lookup"><span data-stu-id="2055f-133">This group of URIs subscribes to Event Collector events from the BMC.</span></span> <span data-ttu-id="2055f-134">Вы можете подписываться на эти события с помощью программы командной строки **wevtutil** .</span><span class="sxs-lookup"><span data-stu-id="2055f-134">You can subscribe to these events using the **Wevtutil** command-line tool.</span></span> <span data-ttu-id="2055f-135">Для получения дополнительной информации см. https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span><span class="sxs-lookup"><span data-stu-id="2055f-135">For more information, see https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span></span>

## <a name="case-sensitivity"></a><span data-ttu-id="2055f-136">Чувствительность к регистру</span><span class="sxs-lookup"><span data-stu-id="2055f-136">Case Sensitivity</span></span>

<span data-ttu-id="2055f-137">[*Подключаемый модуль WMI*](windows-remote-management-glossary.md) сохраняет регистр URI ресурса, полученного в запросе.</span><span class="sxs-lookup"><span data-stu-id="2055f-137">The [*WMI plug-in*](windows-remote-management-glossary.md) preserves the case of the resource URI received in a request.</span></span> <span data-ttu-id="2055f-138">Однако для обеспечения взаимодействия с другими реализациями протокола WS-Management используйте правильный регистр для запрошенного ресурса в URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="2055f-138">However, to ensure interoperability with other implementations of WS-Management protocol, use the correct case for the requested resource in resource URI.</span></span> <span data-ttu-id="2055f-139">Правильный вариант — это проверка орфографии, определяемая поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2055f-139">The correct case is the spelling defined by the resource provider.</span></span>

<span data-ttu-id="2055f-140">В то время как для URI ресурсов не требуется учитывать регистр, [*фрагмент*](windows-remote-management-glossary.md) кода XML делает это.</span><span class="sxs-lookup"><span data-stu-id="2055f-140">While resource URIs do not require case-sensitivity, [*fragment*](windows-remote-management-glossary.md) XML does.</span></span> <span data-ttu-id="2055f-141">Фрагмент указывает только одно свойство, а не весь набор свойств ресурса.</span><span class="sxs-lookup"><span data-stu-id="2055f-141">A fragment specifies just one property, rather than the entire set of properties for a resource.</span></span> <span data-ttu-id="2055f-142">В случае ресурсов WMI синтаксис фрагмента получает одно свойство из экземпляра ресурса.</span><span class="sxs-lookup"><span data-stu-id="2055f-142">In the case of WMI resources, fragment syntax gets one property from a resource instance.</span></span> <span data-ttu-id="2055f-143">Например, для получения только свойства **Version** из [**Win32 от \_ операционной**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) системы необходимо использовать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="2055f-143">For example, getting only the **Version** property from [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requires using a fragment.</span></span> <span data-ttu-id="2055f-144">Дополнительные сведения о фрагментах см. в разделе "Добавление селектора в объект ResourceLocator или Ивсманресаурцелокатор" в [Служба удаленного управления Windows и WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2055f-144">For more information about fragments, see "Adding a selector to a ResourceLocator or IWSManResourceLocator object" in [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="2055f-145">В соответствии со [](windows-remote-management-glossary.md) стандартами XML и XPath [*подключаемый модуль WMI*](windows-remote-management-glossary.md) применяет чувствительность к регистру для фрагментов и XML, определяющих входные параметры для метода.</span><span class="sxs-lookup"><span data-stu-id="2055f-145">Following XML and [*XPath*](windows-remote-management-glossary.md) standards, the [*WMI plug-in*](windows-remote-management-glossary.md) enforces case-sensitivity for fragments and XML that defines the input parameters for a method.</span></span> <span data-ttu-id="2055f-146">Для поддержки стандарта XPath 1.0/Level 1 требуется учитывать регистр.</span><span class="sxs-lookup"><span data-stu-id="2055f-146">Case-sensitivity is required to support the XPath 1.0/Level 1 standard.</span></span> <span data-ttu-id="2055f-147">Чтобы получить данные WMI с помощью WinRM, учет регистра означает, что имена классов, свойств и методов WMI должны соответствовать регистру имен, найденных в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="2055f-147">To get WMI data through WinRM, case-sensitivity means that the names of WMI classes, properties, and methods must match the case of the name found in the WMI repository.</span></span>

<span data-ttu-id="2055f-148">Дополнительные сведения см. в разделе [Синтаксис XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="2055f-148">For more information, see [XPath Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span></span>

## <a name="case-sensitivity-examples"></a><span data-ttu-id="2055f-149">Примеры чувствительности к регистру</span><span class="sxs-lookup"><span data-stu-id="2055f-149">Case Sensitivity Examples</span></span>

<span data-ttu-id="2055f-150">Например, скрипт, получающий свойство **\_ дескриптора безопасности** из экземпляра класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) инструментария WMI, не может использовать для имен в пути фрагмента верхний регистр, а только URI.</span><span class="sxs-lookup"><span data-stu-id="2055f-150">For example, a script that obtains the **SECURITY\_DESCRIPTOR** property from an instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class cannot use upper-case for the names in the fragment path, only the URI.</span></span> <span data-ttu-id="2055f-151">[*Подключаемый модуль WinRM WMI*](windows-remote-management-glossary.md) возвращает ошибку для следующего примера VBScript, поскольку XML-код XPath, указанный для **фрагментпас** , не использует правильный регистр.</span><span class="sxs-lookup"><span data-stu-id="2055f-151">The WinRM [*WMI plug-in*](windows-remote-management-glossary.md) returns an error for the following VBScript example because the XPath XML supplied for the **FragmentPath** does not use the correct case.</span></span> <span data-ttu-id="2055f-152">В репозитории WMI класс написан как " \_ служба Win32".</span><span class="sxs-lookup"><span data-stu-id="2055f-152">In the WMI repository, the class is spelled "Win32\_Service".</span></span>


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



<span data-ttu-id="2055f-153">В следующей версии того же примера показано правильное использование варианта для класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) и свойства **\_ дескриптора безопасности** .</span><span class="sxs-lookup"><span data-stu-id="2055f-153">The following version of the same example shows the correct use of case for the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class and **SECURITY\_DESCRIPTOR** property.</span></span>


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a><span data-ttu-id="2055f-154">См. также</span><span class="sxs-lookup"><span data-stu-id="2055f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2055f-155">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="2055f-155">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="2055f-156">Удаленное управление оборудованием</span><span class="sxs-lookup"><span data-stu-id="2055f-156">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> <dt>

[<span data-ttu-id="2055f-157">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="2055f-157">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 