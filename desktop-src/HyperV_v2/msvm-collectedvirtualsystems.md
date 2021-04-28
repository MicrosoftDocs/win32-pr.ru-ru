---
description: Msvm_CollectedVirtualSystems класс — связывает виртуалсистемколлектион Мсвм \_ с содержащимися в \_ них объектами мсвм ComputerSystem.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Класс Msvm_CollectedVirtualSystems
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6775f41a6e2ae7e45bac642fcd32b8deaec3fda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119282"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="43a60-103">\_Класс мсвм коллектедвиртуалсистемс</span><span class="sxs-lookup"><span data-stu-id="43a60-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="43a60-104">Связывает [**\_ виртуалсистемколлектион мсвм**](msvm-virtualsystemcollection.md) с содержащимися в них объектами [**мсвм \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="43a60-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="43a60-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="43a60-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a60-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43a60-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="43a60-107">Члены</span><span class="sxs-lookup"><span data-stu-id="43a60-107">Members</span></span>

<span data-ttu-id="43a60-108">Класс **мсвм \_ коллектедвиртуалсистемс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="43a60-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="43a60-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="43a60-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43a60-110">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="43a60-110">Properties</span></span>

<span data-ttu-id="43a60-111">Класс **мсвм \_ коллектедвиртуалсистемс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="43a60-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43a60-112">**Коллекция**</span><span class="sxs-lookup"><span data-stu-id="43a60-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43a60-113">Тип данных: **мсвм \_ виртуалсистемколлектион**</span><span class="sxs-lookup"><span data-stu-id="43a60-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="43a60-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43a60-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43a60-115">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="43a60-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="43a60-116">Объект [**мсвм \_ виртуалсистемколлектион**](msvm-virtualsystemcollection.md) GROUPING или "сумка", представляющий коллекцию.</span><span class="sxs-lookup"><span data-stu-id="43a60-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="43a60-117">**Член**</span><span class="sxs-lookup"><span data-stu-id="43a60-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43a60-118">Тип данных: **мсвм \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="43a60-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="43a60-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43a60-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43a60-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("член")</span><span class="sxs-lookup"><span data-stu-id="43a60-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="43a60-121">Объект [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , содержащий элементы коллекции.</span><span class="sxs-lookup"><span data-stu-id="43a60-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43a60-122">Требования</span><span class="sxs-lookup"><span data-stu-id="43a60-122">Requirements</span></span>



| <span data-ttu-id="43a60-123">Требование</span><span class="sxs-lookup"><span data-stu-id="43a60-123">Requirement</span></span> | <span data-ttu-id="43a60-124">Значение</span><span class="sxs-lookup"><span data-stu-id="43a60-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a60-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43a60-125">Minimum supported client</span></span><br/> | <span data-ttu-id="43a60-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="43a60-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="43a60-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43a60-127">Minimum supported server</span></span><br/> | <span data-ttu-id="43a60-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="43a60-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="43a60-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43a60-129">Namespace</span></span><br/>                | <span data-ttu-id="43a60-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="43a60-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="43a60-131">MOF</span><span class="sxs-lookup"><span data-stu-id="43a60-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43a60-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43a60-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43a60-133">DLL</span><span class="sxs-lookup"><span data-stu-id="43a60-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43a60-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43a60-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="43a60-135">См. также</span><span class="sxs-lookup"><span data-stu-id="43a60-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a60-136">**\_КОЛЛЕКТЕДМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="43a60-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

