---
description: Представляет связь между виртуальной системой и самым актуальным моментальным снимком системы. Эта ассоциация может существовать только в том случае, если виртуальная система была создана с помощью моментального снимка или если моментальный снимок был создан из виртуальной системы.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: Класс CIM_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683260"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="60a41-104">\_Класс CIM мосткуррентснапшотинбранч</span><span class="sxs-lookup"><span data-stu-id="60a41-104">CIM\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="60a41-105">Представляет связь между виртуальной системой и самым актуальным моментальным снимком системы.</span><span class="sxs-lookup"><span data-stu-id="60a41-105">Represents an association between a virtual system and the most current snapshot of the system.</span></span> <span data-ttu-id="60a41-106">Эта ассоциация может существовать только в том случае, если виртуальная система была создана с помощью моментального снимка или если моментальный снимок был создан из виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="60a41-106">This association can only exist if the virtual system was create using a snapshot or if a snapshot was created from the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a41-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60a41-107">Syntax</span></span>

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="60a41-108">Члены</span><span class="sxs-lookup"><span data-stu-id="60a41-108">Members</span></span>

<span data-ttu-id="60a41-109">Класс **CIM \_ мосткуррентснапшотинбранч** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="60a41-109">The **CIM\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="60a41-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="60a41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60a41-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="60a41-111">Properties</span></span>

<span data-ttu-id="60a41-112">Класс **CIM \_ мосткуррентснапшотинбранч** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="60a41-112">The **CIM\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60a41-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="60a41-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60a41-114">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="60a41-114">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="60a41-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="60a41-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60a41-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="60a41-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="60a41-117">Ссылка на экземпляр [**CIM \_ ComputerSystem**](cim-computersystem.md) , представляющий виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="60a41-117">A reference to the instance of [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="60a41-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="60a41-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60a41-119">Тип данных: **CIM \_ виртуалсистемсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="60a41-119">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="60a41-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="60a41-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60a41-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="60a41-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="60a41-122">Ссылка на экземпляр [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющий моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="60a41-122">A reference to the instance of [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that represents the virtual system snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60a41-123">Требования</span><span class="sxs-lookup"><span data-stu-id="60a41-123">Requirements</span></span>



| <span data-ttu-id="60a41-124">Требование</span><span class="sxs-lookup"><span data-stu-id="60a41-124">Requirement</span></span> | <span data-ttu-id="60a41-125">Значение</span><span class="sxs-lookup"><span data-stu-id="60a41-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60a41-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60a41-126">Minimum supported client</span></span><br/> | <span data-ttu-id="60a41-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="60a41-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="60a41-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60a41-128">Minimum supported server</span></span><br/> | <span data-ttu-id="60a41-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60a41-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="60a41-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60a41-130">Namespace</span></span><br/>                | <span data-ttu-id="60a41-131">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="60a41-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60a41-132">MOF</span><span class="sxs-lookup"><span data-stu-id="60a41-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60a41-133"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60a41-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60a41-134">DLL</span><span class="sxs-lookup"><span data-stu-id="60a41-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60a41-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60a41-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60a41-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60a41-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a41-137">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="60a41-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

