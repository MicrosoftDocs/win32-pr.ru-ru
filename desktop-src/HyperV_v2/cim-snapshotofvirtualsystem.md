---
description: Связывает виртуальную систему с моментальным снимком виртуальной системы.
ms.assetid: f85f6914-dbb8-42c9-a732-11d48613c15c
title: Класс CIM_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SnapshotOfVirtualSystem
- CIM_SnapshotOfVirtualSystem.Antecedent
- CIM_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e8e0929f1198ececea5ea5ec144e2f7313ec35c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998927"
---
# <a name="cim_snapshotofvirtualsystem-class"></a><span data-ttu-id="43815-103">\_Класс CIM снапшотофвиртуалсистем</span><span class="sxs-lookup"><span data-stu-id="43815-103">CIM\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="43815-104">Связывает виртуальную систему с моментальным снимком виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="43815-104">Associates a virtual system a snapshot of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="43815-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43815-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_SnapshotOfVirtualSystem : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="43815-106">Члены</span><span class="sxs-lookup"><span data-stu-id="43815-106">Members</span></span>

<span data-ttu-id="43815-107">Класс **CIM \_ снапшотофвиртуалсистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="43815-107">The **CIM\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="43815-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="43815-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43815-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="43815-109">Properties</span></span>

<span data-ttu-id="43815-110">Класс **CIM \_ снапшотофвиртуалсистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="43815-110">The **CIM\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43815-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="43815-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43815-112">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="43815-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="43815-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43815-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43815-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="43815-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="43815-115">Ссылка на компьютерную систему, представляющую виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="43815-115">A reference to the computer system that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="43815-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="43815-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43815-117">Тип данных: **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="43815-117">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="43815-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="43815-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43815-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="43815-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="43815-120">Ссылка на объект данных параметров, представляющий моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="43815-120">A reference to the settings data object that represents the snapshot of the virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43815-121">Требования</span><span class="sxs-lookup"><span data-stu-id="43815-121">Requirements</span></span>



| <span data-ttu-id="43815-122">Требование</span><span class="sxs-lookup"><span data-stu-id="43815-122">Requirement</span></span> | <span data-ttu-id="43815-123">Значение</span><span class="sxs-lookup"><span data-stu-id="43815-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43815-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43815-124">Minimum supported client</span></span><br/> | <span data-ttu-id="43815-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="43815-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="43815-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43815-126">Minimum supported server</span></span><br/> | <span data-ttu-id="43815-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="43815-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="43815-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43815-128">Namespace</span></span><br/>                | <span data-ttu-id="43815-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="43815-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="43815-130">MOF</span><span class="sxs-lookup"><span data-stu-id="43815-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43815-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43815-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43815-132">DLL</span><span class="sxs-lookup"><span data-stu-id="43815-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43815-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43815-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="43815-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43815-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43815-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="43815-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

