---
description: Класс представления взаимосвязей позволяет использовать СОЕДИНИТЕЛи запросов к классам, которые находятся в разных пространствах имен.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Связывание экземпляров между пространствами имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d743b835d28af4fe0a8dd5d09858b2ba6ff0abacd0f35219c3dd90d39d0810d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557022"
---
# <a name="associating-instances-between-namespaces"></a>Связывание экземпляров между пространствами имен

Класс представления взаимосвязей позволяет использовать [соединители](associators-of-statement.md) запросов к классам, которые находятся в разных пространствах имен.

Следующая процедура описывает, как связать экземпляры между пространствами имен.

**Связывание экземпляров между пространствами имен**

1.  Начните определение класса с квалификатором строки [**связи**](meta-qualifiers.md) .

    Квалификаторы **жоинон**, [**Association**](meta-qualifiers.md)и **Union** являются взаимоисключающими.

2.  Создайте запросы, определяющие экземпляры источника, используемые в классе представления, с квалификатором [**виевсаурцес**](viewsources-qualifier.md) .
3.  Определите имена и расположение пространств имен, в которых экземпляры источника находятся с квалификатором [**виевспацес**](viewspaces-qualifier.md) .
4.  Определите необходимые свойства в классе представления ассоциаций с помощью квалификатора [**пропертисаурцес**](propertysources-qualifier.md) .

    При необходимости можно пометить любые свойства как принадлежащие исходному классу с помощью квалификатора [**хиддендефаулт**](qualifiers-specific-to-the-view-provider.md) .

5.  Пометьте все соответствующие свойства с помощью **прямого** квалификатора.

    **Прямой** квалификатор не позволяет поставщику представления сопоставлять ссылку на представление со ссылкой с тегами.

В следующих примерах кода показано, как создавать классы представлений ассоциаций.

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 



