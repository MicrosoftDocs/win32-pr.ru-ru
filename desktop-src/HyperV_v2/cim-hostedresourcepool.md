---
description: Представляет связь между системой и пулом ресурсов, который является компонентом системы.
ms.assetid: 0ac60dbd-0498-4978-b2d6-f4c9926a83a8
title: Класс CIM_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedResourcePool
- CIM_HostedResourcePool.GroupComponent
- CIM_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dbb6d523b533d6e8b2f5bc1e21de93962cfd860f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662145"
---
# <a name="cim_hostedresourcepool-class"></a><span data-ttu-id="64cc5-103">\_Класс CIM хостедресаурцепул</span><span class="sxs-lookup"><span data-stu-id="64cc5-103">CIM\_HostedResourcePool class</span></span>

<span data-ttu-id="64cc5-104">Представляет связь между системой и пулом ресурсов, который является компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="64cc5-104">Represents an association between a system and a resource pool that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="64cc5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64cc5-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_HostedResourcePool : CIM_SystemComponent
{
  CIM_System       REF GroupComponent;
  CIM_ResourcePool REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="64cc5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="64cc5-106">Members</span></span>

<span data-ttu-id="64cc5-107">Класс **CIM \_ хостедресаурцепул** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="64cc5-107">The **CIM\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="64cc5-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="64cc5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64cc5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="64cc5-109">Properties</span></span>

<span data-ttu-id="64cc5-110">Класс **CIM \_ хостедресаурцепул** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="64cc5-110">The **CIM\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64cc5-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="64cc5-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64cc5-112">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="64cc5-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="64cc5-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64cc5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64cc5-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="64cc5-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="64cc5-115">Родительская система в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="64cc5-115">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="64cc5-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="64cc5-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64cc5-117">Тип данных: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="64cc5-117">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="64cc5-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64cc5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64cc5-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="64cc5-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="64cc5-120">Пул ресурсов, который является компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="64cc5-120">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64cc5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="64cc5-121">Requirements</span></span>



| <span data-ttu-id="64cc5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="64cc5-122">Requirement</span></span> | <span data-ttu-id="64cc5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="64cc5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64cc5-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64cc5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="64cc5-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="64cc5-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="64cc5-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64cc5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="64cc5-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="64cc5-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="64cc5-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="64cc5-128">Namespace</span></span><br/>                | <span data-ttu-id="64cc5-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="64cc5-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="64cc5-130">MOF</span><span class="sxs-lookup"><span data-stu-id="64cc5-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64cc5-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64cc5-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64cc5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="64cc5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64cc5-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64cc5-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64cc5-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64cc5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64cc5-135">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="64cc5-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

