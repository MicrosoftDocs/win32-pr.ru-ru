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
# <a name="uri-prefixes"></a>Префиксы URI

Префикс [*URI ресурса*](windows-remote-management-glossary.md) различается в зависимости от того, какая схема XML описывает ресурс.

## <a name="prefixes"></a>Префиксы

Если вы обращаетесь к классу [*cim*](windows-remote-management-glossary.md) 2,1, например к [**\_ файлу данных CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), префикс URI отличается от префикса для класса CIM 2,9, например **CIM \_ админдомаин**. Классы CIM 2,1 описаны в разделе [классы cim](/windows/desktop/WmiSdk/cimclas) инструментарий управления Windows (WMI) (WMI).

Большинство [классов WMI](/windows/desktop/WmiSdk/wmi-classes) находятся в **корневом \\** пространстве имен CIMV2 WMI. Классы для поставщика [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)(Майкрософт) находятся в **корневом \\ оборудовании**.

Следующий список содержит префиксы URI ресурса для этих схем:

-   Классы WMI или CIM 2,1 в **корневом \\** пространстве имен CIMV2

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   Классы CIM 2,9 или классы IPMI

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Альтернативный способ доступа к классам поставщика IPMI

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Дополнительные сведения см. в разделе [URI ресурсов](resource-uris.md) и [строки UrlPrefix](/windows/desktop/Http/urlprefix-strings). Дополнительные сведения о создании универсального кода ресурса (URI) для класса или метода WMI см. в разделе [Служба удаленного управления Windows и WMI](windows-remote-management-and-wmi.md).

## <a name="prefix-aliases"></a>Псевдонимы префиксов

Псевдоним префикса — это ярлык, представляющий длинный префикс URI ресурса. Псевдонимы также можно использовать в командной строке **WinRM** . Чтобы просмотреть список доступных псевдонимов, введите **WinRM Help псевдонимы**.

Имейте в виду, что псевдоним нельзя использовать внутри ссылки на конечную точку (EPR) при указании URI ресурса. Служба удаленного управления Windows не может расширить псевдоним, если он внедрен в XML.

В следующем примере кода псевдоним WinRM используется в EPR вместо полного URI ресурса, то есть `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` . В этом случае WinRM возвращает ошибку, указывающую, что службе не удается обработать запрос.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



Ниже перечислены определенные псевдонимы и URI ресурсов, для которых они заменяются.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>интерфейса
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>CIMV2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>службе
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>ведущий
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>консоль
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[служба удаленного управления Windows и WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[URI ресурсов](resource-uris.md)
</dt> </dl>
