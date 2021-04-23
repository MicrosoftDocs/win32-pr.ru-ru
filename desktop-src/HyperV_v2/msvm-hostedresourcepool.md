---
description: Представляет специализацию связи системных компонентов, которая устанавливает, что пул ресурсов определяется в контексте системы.
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Класс Msvm_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d64488a845e8d51bfe27829b01ebcf0ac7d944c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896838"
---
# <a name="msvm_hostedresourcepool-class"></a><span data-ttu-id="c5ffe-103">\_Класс мсвм хостедресаурцепул</span><span class="sxs-lookup"><span data-stu-id="c5ffe-103">Msvm\_HostedResourcePool class</span></span>

<span data-ttu-id="c5ffe-104">Представляет специализацию связи системных компонентов, которая устанавливает, что пул ресурсов определяется в контексте системы.</span><span class="sxs-lookup"><span data-stu-id="c5ffe-104">Represents a specialization of the system component association that establishes that the resource pool is defined in the context of the system.</span></span>

<span data-ttu-id="c5ffe-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c5ffe-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ffe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5ffe-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="c5ffe-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c5ffe-107">Members</span></span>

<span data-ttu-id="c5ffe-108">Класс **мсвм \_ хостедресаурцепул** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c5ffe-108">The **Msvm\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="c5ffe-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5ffe-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5ffe-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5ffe-110">Properties</span></span>

<span data-ttu-id="c5ffe-111">Класс **мсвм \_ хостедресаурцепул** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c5ffe-111">The **Msvm\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5ffe-112">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="c5ffe-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5ffe-113">Тип данных: **[ **мсвм \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="c5ffe-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c5ffe-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5ffe-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5ffe-115">Квалификаторы: [**переопределения**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="c5ffe-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c5ffe-116">Родительская система в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="c5ffe-116">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="c5ffe-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c5ffe-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5ffe-118">Тип данных: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c5ffe-118">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="c5ffe-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5ffe-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5ffe-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="c5ffe-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c5ffe-121">Пул ресурсов, который является компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="c5ffe-121">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5ffe-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c5ffe-122">Requirements</span></span>



| <span data-ttu-id="c5ffe-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c5ffe-123">Requirement</span></span> | <span data-ttu-id="c5ffe-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ffe-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ffe-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5ffe-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ffe-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c5ffe-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c5ffe-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5ffe-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ffe-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c5ffe-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5ffe-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c5ffe-129">Namespace</span></span><br/>                | <span data-ttu-id="c5ffe-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c5ffe-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c5ffe-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c5ffe-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5ffe-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5ffe-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5ffe-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ffe-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5ffe-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5ffe-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

