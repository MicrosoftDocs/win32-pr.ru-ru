---
description: Класс представления взаимосвязей позволяет использовать СОЕДИНИТЕЛи запросов к классам, которые находятся в разных пространствах имен.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Связывание экземпляров между пространствами имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346225"
---
# <a name="associating-instances-between-namespaces"></a><span data-ttu-id="ce52a-103">Связывание экземпляров между пространствами имен</span><span class="sxs-lookup"><span data-stu-id="ce52a-103">Associating Instances Between Namespaces</span></span>

<span data-ttu-id="ce52a-104">Класс представления взаимосвязей позволяет использовать [соединители](associators-of-statement.md) запросов к классам, которые находятся в разных пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="ce52a-104">An association view class allows you to use [ASSOCIATORS OF](associators-of-statement.md) queries on classes that reside in different namespaces.</span></span>

<span data-ttu-id="ce52a-105">Следующая процедура описывает, как связать экземпляры между пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="ce52a-105">The following procedure describes how to associate instances between namespaces.</span></span>

<span data-ttu-id="ce52a-106">**Связывание экземпляров между пространствами имен**</span><span class="sxs-lookup"><span data-stu-id="ce52a-106">**To associate instances between namespaces**</span></span>

1.  <span data-ttu-id="ce52a-107">Начните определение класса с квалификатором строки [**связи**](meta-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="ce52a-107">Begin your class definition with the [**Association**](meta-qualifiers.md) string qualifier.</span></span>

    <span data-ttu-id="ce52a-108">Квалификаторы **жоинон**, [**Association**](meta-qualifiers.md)и **Union** являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="ce52a-108">The **JoinOn**, [**Association**](meta-qualifiers.md), and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="ce52a-109">Создайте запросы, определяющие экземпляры источника, используемые в классе представления, с квалификатором [**виевсаурцес**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="ce52a-109">Create the queries that define source instances used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="ce52a-110">Определите имена и расположение пространств имен, в которых экземпляры источника находятся с квалификатором [**виевспацес**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="ce52a-110">Define the names and location of the namespaces in which the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="ce52a-111">Определите необходимые свойства в классе представления ассоциаций с помощью квалификатора [**пропертисаурцес**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="ce52a-111">Define the properties you want in your association view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="ce52a-112">При необходимости можно пометить любые свойства как принадлежащие исходному классу с помощью квалификатора [**хиддендефаулт**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="ce52a-112">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="ce52a-113">Пометьте все соответствующие свойства с помощью **прямого** квалификатора.</span><span class="sxs-lookup"><span data-stu-id="ce52a-113">Tag any relevant properties with the **Direct** qualifier.</span></span>

    <span data-ttu-id="ce52a-114">**Прямой** квалификатор не позволяет поставщику представления сопоставлять ссылку на представление со ссылкой с тегами.</span><span class="sxs-lookup"><span data-stu-id="ce52a-114">The **Direct** qualifier prevents the View Provider from mapping the tagged association reference to a view reference.</span></span>

<span data-ttu-id="ce52a-115">В следующих примерах кода показано, как создавать классы представлений ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="ce52a-115">The following code examples show how to create association view classes.</span></span>

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

 

 



