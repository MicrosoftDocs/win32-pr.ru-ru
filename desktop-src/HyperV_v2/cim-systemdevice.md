---
description: Связывает систему с логическим устройством, которое является компонентом системы.
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: Класс CIM_SystemDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b02921e4be0f8aa0cddc194a2ed430e10e115eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683257"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a><span data-ttu-id="40a5a-103">Класс CIM_SystemDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="40a5a-103">CIM_SystemDevice class (Hyper-V management)</span></span>

<span data-ttu-id="40a5a-104">Связывает систему с логическим устройством, которое является компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="40a5a-104">Associates a system with a logical device that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a5a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40a5a-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="40a5a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="40a5a-106">Members</span></span>

<span data-ttu-id="40a5a-107">Класс **CIM \_ системдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="40a5a-107">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="40a5a-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="40a5a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40a5a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="40a5a-109">Properties</span></span>

<span data-ttu-id="40a5a-110">Класс **CIM \_ системдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="40a5a-110">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40a5a-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="40a5a-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40a5a-112">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="40a5a-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="40a5a-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40a5a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40a5a-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="40a5a-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="40a5a-115">[**\_ Системная ссылка CIM**](cim-system.md) на родительскую систему в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="40a5a-115">A [**CIM\_System**](cim-system.md) reference to the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="40a5a-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="40a5a-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40a5a-117">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="40a5a-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="40a5a-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40a5a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40a5a-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40a5a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40a5a-120">Ссылка логического устройства [**CIM \_**](cim-logicaldevice.md) на логическое устройство, которое является компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="40a5a-120">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) reference to the logical device that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40a5a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="40a5a-121">Requirements</span></span>



| <span data-ttu-id="40a5a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="40a5a-122">Requirement</span></span> | <span data-ttu-id="40a5a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="40a5a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40a5a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40a5a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40a5a-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="40a5a-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="40a5a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40a5a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40a5a-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40a5a-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="40a5a-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40a5a-128">Namespace</span></span><br/>                | <span data-ttu-id="40a5a-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="40a5a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="40a5a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="40a5a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40a5a-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40a5a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="40a5a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="40a5a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40a5a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="40a5a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="40a5a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40a5a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a5a-135">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="40a5a-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

