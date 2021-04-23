---
title: Префиксы URI
description: Префикс URI ресурса различается в зависимости от того, какая схема XML описывает ресурс.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "103891212"
---
# <a name="uri-prefixes"></a><span data-ttu-id="6dc9f-103">Префиксы URI</span><span class="sxs-lookup"><span data-stu-id="6dc9f-103">URI prefixes</span></span>

<span data-ttu-id="6dc9f-104">Префикс [*URI ресурса*](windows-remote-management-glossary.md) различается в зависимости от того, какая схема XML описывает ресурс.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-104">The [*resource URI*](windows-remote-management-glossary.md) prefix is different depending on which XML schema describes the resource.</span></span>

## <a name="prefixes"></a><span data-ttu-id="6dc9f-105">Префиксы</span><span class="sxs-lookup"><span data-stu-id="6dc9f-105">Prefixes</span></span>

<span data-ttu-id="6dc9f-106">Если вы обращаетесь к классу [*cim*](windows-remote-management-glossary.md) 2,1, например к [**\_ файлу данных CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), префикс URI отличается от префикса для класса CIM 2,9, например **CIM \_ админдомаин**.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-106">If you access a [*CIM*](windows-remote-management-glossary.md) 2.1 class, such as [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), the prefix of the URI differs from the prefix for a CIM 2.9 class, such as **CIM\_AdminDomain**.</span></span> <span data-ttu-id="6dc9f-107">Классы CIM 2,1 описаны в разделе [классы cim](/windows/desktop/WmiSdk/cimclas) инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6dc9f-107">CIM 2.1 classes are documented in the [CIM Classes](/windows/desktop/WmiSdk/cimclas) section of Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="6dc9f-108">Большинство [классов WMI](/windows/desktop/WmiSdk/wmi-classes) находятся в **корневом \\** пространстве имен CIMV2 WMI.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-108">Most [WMI classes](/windows/desktop/WmiSdk/wmi-classes) are in the **root\\cimv2** WMI namespace.</span></span> <span data-ttu-id="6dc9f-109">Классы для поставщика [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)(Майкрософт) находятся в **корневом \\ оборудовании**.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-109">Classes for the Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) provider are in **root\\hardware**.</span></span>

<span data-ttu-id="6dc9f-110">Следующий список содержит префиксы URI ресурса для этих схем:</span><span class="sxs-lookup"><span data-stu-id="6dc9f-110">The following list contains the resource URI prefixes for these schemas:</span></span>

-   <span data-ttu-id="6dc9f-111">Классы WMI или CIM 2,1 в **корневом \\** пространстве имен CIMV2</span><span class="sxs-lookup"><span data-stu-id="6dc9f-111">WMI or CIM 2.1 classes in the **root\\cimv2** namespace</span></span>

    <span data-ttu-id="6dc9f-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span><span class="sxs-lookup"><span data-stu-id="6dc9f-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span></span>

-   <span data-ttu-id="6dc9f-113">Классы CIM 2,9 или классы IPMI</span><span class="sxs-lookup"><span data-stu-id="6dc9f-113">CIM 2.9 classes or IPMI classes</span></span>

    <span data-ttu-id="6dc9f-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span><span class="sxs-lookup"><span data-stu-id="6dc9f-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span></span>

-   <span data-ttu-id="6dc9f-115">Альтернативный способ доступа к классам поставщика IPMI</span><span class="sxs-lookup"><span data-stu-id="6dc9f-115">Alternate way to access IPMI provider classes</span></span>

    <span data-ttu-id="6dc9f-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span><span class="sxs-lookup"><span data-stu-id="6dc9f-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span></span>

<span data-ttu-id="6dc9f-117">Дополнительные сведения см. в разделе [URI ресурсов](resource-uris.md) и [строки UrlPrefix](/windows/desktop/Http/urlprefix-strings).</span><span class="sxs-lookup"><span data-stu-id="6dc9f-117">For more information, see [Resource URIs](resource-uris.md) and [UrlPrefix Strings](/windows/desktop/Http/urlprefix-strings).</span></span> <span data-ttu-id="6dc9f-118">Дополнительные сведения о создании универсального кода ресурса (URI) для класса или метода WMI см. в разделе [Служба удаленного управления Windows и WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6dc9f-118">For more information about generating a URI for a WMI class or method, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="prefix-aliases"></a><span data-ttu-id="6dc9f-119">Псевдонимы префиксов</span><span class="sxs-lookup"><span data-stu-id="6dc9f-119">Prefix Aliases</span></span>

<span data-ttu-id="6dc9f-120">Псевдоним префикса — это ярлык, представляющий длинный префикс URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-120">A prefix alias is a shortcut that represents the long resource URI prefix.</span></span> <span data-ttu-id="6dc9f-121">Псевдонимы также можно использовать в командной строке **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="6dc9f-121">You can also use aliases in the **Winrm** command-line.</span></span> <span data-ttu-id="6dc9f-122">Чтобы просмотреть список доступных псевдонимов, введите **WinRM Help псевдонимы**.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-122">To view a list of available aliases, type **Winrm help aliases**.</span></span>

<span data-ttu-id="6dc9f-123">Имейте в виду, что псевдоним нельзя использовать внутри ссылки на конечную точку (EPR) при указании URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-123">Be aware that an alias cannot be used inside an endpoint reference (EPR) when specifying a resource URI.</span></span> <span data-ttu-id="6dc9f-124">Служба удаленного управления Windows не может расширить псевдоним, если он внедрен в XML.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-124">Windows Remote Management is unable to expand the alias when it is embedded in XML.</span></span>

<span data-ttu-id="6dc9f-125">В следующем примере кода псевдоним WinRM используется в EPR вместо полного URI ресурса, то есть `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` .</span><span class="sxs-lookup"><span data-stu-id="6dc9f-125">In the following code example, the winrm alias is used in an EPR instead of the complete resource URI, which is `http://schemas.microsoft.com/wbem/wsman/1/config/Listener`.</span></span> <span data-ttu-id="6dc9f-126">В этом случае WinRM возвращает ошибку, указывающую, что службе не удается обработать запрос.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-126">In this case, WinRM returns an error that indicates the service cannot process the request.</span></span>


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



<span data-ttu-id="6dc9f-127">Ниже перечислены определенные псевдонимы и URI ресурсов, для которых они заменяются.</span><span class="sxs-lookup"><span data-stu-id="6dc9f-127">The following lists defined aliases and resource URIs for which they substitute.</span></span>

<dl> <dt>

<span data-ttu-id="6dc9f-128"><span id="wmi"></span><span id="WMI"></span>интерфейса</span><span class="sxs-lookup"><span data-stu-id="6dc9f-128"><span id="wmi"></span><span id="WMI"></span>wmi</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span data-ttu-id="6dc9f-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span><span class="sxs-lookup"><span data-stu-id="6dc9f-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span data-ttu-id="6dc9f-130"><span id="cimv2"></span><span id="CIMV2"></span>CIMV2</span><span class="sxs-lookup"><span data-stu-id="6dc9f-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span></span>
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span data-ttu-id="6dc9f-131"><span id="winrm"></span><span id="WINRM"></span>службе</span><span class="sxs-lookup"><span data-stu-id="6dc9f-131"><span id="winrm"></span><span id="WINRM"></span>winrm</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="6dc9f-132"><span id="wsman"></span><span id="WSMAN"></span>ведущий</span><span class="sxs-lookup"><span data-stu-id="6dc9f-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="6dc9f-133"><span id="shell"></span><span id="SHELL"></span>консоль</span><span class="sxs-lookup"><span data-stu-id="6dc9f-133"><span id="shell"></span><span id="SHELL"></span>shell</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6dc9f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="6dc9f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dc9f-135">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="6dc9f-135">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="6dc9f-136">служба удаленного управления Windows и WMI</span><span class="sxs-lookup"><span data-stu-id="6dc9f-136">Windows Remote Management and WMI</span></span>](windows-remote-management-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="6dc9f-137">URI ресурсов</span><span class="sxs-lookup"><span data-stu-id="6dc9f-137">Resource URIs</span></span>](resource-uris.md)
</dt> </dl>
