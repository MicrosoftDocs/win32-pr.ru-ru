---
description: Представляет пространство имен WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: Класс __Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912755"
---
# <a name="__namespace-class"></a><span data-ttu-id="578ed-103">\_\_Класс Namespace</span><span class="sxs-lookup"><span data-stu-id="578ed-103">\_\_Namespace class</span></span>

<span data-ttu-id="578ed-104">Класс системы **\_ \_ пространства имен** представляет пространство имен WMI.</span><span class="sxs-lookup"><span data-stu-id="578ed-104">The **\_\_Namespace** system class represents a WMI namespace.</span></span>

<span data-ttu-id="578ed-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="578ed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="578ed-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="578ed-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="578ed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="578ed-107">Syntax</span></span>

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="578ed-108">Члены</span><span class="sxs-lookup"><span data-stu-id="578ed-108">Members</span></span>

<span data-ttu-id="578ed-109">Класс **\_ \_ Namespace** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="578ed-109">The **\_\_Namespace** class has these types of members:</span></span>

-   [<span data-ttu-id="578ed-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="578ed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="578ed-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="578ed-111">Properties</span></span>

<span data-ttu-id="578ed-112">Класс **\_ \_ Namespace** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="578ed-112">The **\_\_Namespace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="578ed-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="578ed-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="578ed-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="578ed-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="578ed-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="578ed-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="578ed-116">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="578ed-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="578ed-117">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="578ed-117">Namespace name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="578ed-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="578ed-118">Remarks</span></span>

<span data-ttu-id="578ed-119">Класс **\_ \_ Namespace** является производным от [**\_ \_ системкласс**](--systemclass.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="578ed-119">The **\_\_Namespace** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="578ed-120">**\_ \_ Пространство имен** можно использовать для поиска, создания и удаления дочерних пространств имен в текущем рабочем пространстве, для которого имеется объект [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="578ed-120">You can use **\_\_Namespace** to identify, create, and delete child namespaces within the current working namespace for which you have an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) object.</span></span> <span data-ttu-id="578ed-121">Создание нового экземпляра **\_ \_ пространства имен** в любом рабочем пространстве имен создает Дочернее пространство имен в рабочем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="578ed-121">Creating a new instance of **\_\_Namespace** within any working namespace creates a child namespace within the working namespace.</span></span> <span data-ttu-id="578ed-122">И наоборот, удаление экземпляра **\_ \_ пространства имен** удаляет Дочернее пространство имен из рабочего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="578ed-122">Conversely, deleting an instance of **\_\_Namespace** removes the child namespace from the working namespace.</span></span> <span data-ttu-id="578ed-123">Обратите внимание, что при удалении дочернего пространства имен также удаляются все его классы и экземпляры.</span><span class="sxs-lookup"><span data-stu-id="578ed-123">Note that deleting a child namespace also deletes all of its classes and instances.</span></span>

<span data-ttu-id="578ed-124">Перечисление экземпляров этого класса в любом рабочем пространстве имен предоставляет доступные дочерние пространства имен.</span><span class="sxs-lookup"><span data-stu-id="578ed-124">Enumerating instances of this class within any working namespace gives the available child namespaces.</span></span>

<span data-ttu-id="578ed-125">Например, в \\ корневом пространстве имен два экземпляра **\_ \_ пространства имен**.</span><span class="sxs-lookup"><span data-stu-id="578ed-125">For example, within the \\root namespace are two instances of **\_\_Namespace**.</span></span> <span data-ttu-id="578ed-126">Свойство **Name** имеет значение Default, а другое имеет **имя** "CIMV2".</span><span class="sxs-lookup"><span data-stu-id="578ed-126">One has its **Name** property set to "Default," the other has **Name** set to "Cimv2."</span></span> <span data-ttu-id="578ed-127">Эти экземпляры представляют \\ корневые \\ пространства имен по умолчанию и \\ корневые \\ CIMV2, соответственно.</span><span class="sxs-lookup"><span data-stu-id="578ed-127">These instances represent the \\root\\default, and \\root\\cimv2 namespaces, respectively.</span></span>

## <a name="examples"></a><span data-ttu-id="578ed-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="578ed-128">Examples</span></span>

<span data-ttu-id="578ed-129">В примере из [списка всех пространств имен WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) в коллекции TechNet используется рекурсивный вызов для перечисления всех экземпляров \_ \_ класса пространства имен в системе.</span><span class="sxs-lookup"><span data-stu-id="578ed-129">The [List All WMI Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript example on the TechNet Gallery uses a recursive call to list all instances of the \_\_Namespace class on a system.</span></span>

<span data-ttu-id="578ed-130">Следующий пример кода извлекает все пространства имен в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="578ed-130">The following code sample retrieves all namespaces in PowerShell.</span></span>


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



<span data-ttu-id="578ed-131">Следующий пример кода улучшает предыдущий пример и добавляет дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="578ed-131">The following code sample improves on the previous sample, and adds in additional information.</span></span>


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a><span data-ttu-id="578ed-132">Требования</span><span class="sxs-lookup"><span data-stu-id="578ed-132">Requirements</span></span>



| <span data-ttu-id="578ed-133">Требование</span><span class="sxs-lookup"><span data-stu-id="578ed-133">Requirement</span></span> | <span data-ttu-id="578ed-134">Значение</span><span class="sxs-lookup"><span data-stu-id="578ed-134">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="578ed-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="578ed-135">Minimum supported client</span></span><br/> | <span data-ttu-id="578ed-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="578ed-136">Windows Vista</span></span><br/>       |
| <span data-ttu-id="578ed-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="578ed-137">Minimum supported server</span></span><br/> | <span data-ttu-id="578ed-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="578ed-138">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="578ed-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="578ed-139">Namespace</span></span><br/>                | <span data-ttu-id="578ed-140">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="578ed-140">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="578ed-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="578ed-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578ed-142">**\_\_системкласс**</span><span class="sxs-lookup"><span data-stu-id="578ed-142">**\_\_SystemClass**</span></span>](--systemclass.md)
</dt> <dt>

[<span data-ttu-id="578ed-143">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="578ed-143">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




