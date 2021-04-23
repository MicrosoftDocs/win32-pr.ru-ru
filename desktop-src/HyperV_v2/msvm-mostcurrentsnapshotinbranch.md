---
description: Связывает экземпляр \_ класса мсвм ComputerSystem или мсвм \_ планнедкомпутерсистем, представляющий виртуальную систему, с экземпляром \_ класса мсвм виртуалсистемсеттингдата, представляющего моментальный снимок виртуальной системы, который является самым актуальным моментальным снимком в ветви зависимых моментальных снимков.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Класс Msvm_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664508"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="6d12f-103">\_Класс мсвм мосткуррентснапшотинбранч</span><span class="sxs-lookup"><span data-stu-id="6d12f-103">Msvm\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="6d12f-104">Связывает экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) или [**мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md) , представляющий виртуальную систему, с экземпляром класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющего моментальный снимок виртуальной системы, который является самым актуальным моментальным снимком в ветви зависимых моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="6d12f-104">Associates an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing a virtual system, with an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class representing the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span>

<span data-ttu-id="6d12f-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6d12f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d12f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d12f-106">Syntax</span></span>

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6d12f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6d12f-107">Members</span></span>

<span data-ttu-id="6d12f-108">Класс **мсвм \_ мосткуррентснапшотинбранч** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6d12f-108">The **Msvm\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="6d12f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d12f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d12f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d12f-110">Properties</span></span>

<span data-ttu-id="6d12f-111">Класс **мсвм \_ мосткуррентснапшотинбранч** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6d12f-111">The **Msvm\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d12f-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="6d12f-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d12f-113">Тип данных: **[ **CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="6d12f-113">Data type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>
</dt> <dt>

<span data-ttu-id="6d12f-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d12f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d12f-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6d12f-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6d12f-116">Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) или [**мсвм \_ планнедкомпутерсистем**](msvm-plannedcomputersystem.md) , представляющий виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="6d12f-116">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing the virtual system.</span></span> <span data-ttu-id="6d12f-117">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="6d12f-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="6d12f-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="6d12f-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d12f-119">Тип данных: **[ **мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="6d12f-119">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6d12f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d12f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d12f-121">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6d12f-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6d12f-122">Ссылка на экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий моментальный снимок виртуальной системы, который является самым актуальным моментальным снимком в ветви зависимых моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="6d12f-122">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span> <span data-ttu-id="6d12f-123">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="6d12f-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d12f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6d12f-124">Requirements</span></span>



| <span data-ttu-id="6d12f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6d12f-125">Requirement</span></span> | <span data-ttu-id="6d12f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6d12f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d12f-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d12f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6d12f-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6d12f-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6d12f-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d12f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6d12f-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6d12f-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d12f-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d12f-131">Namespace</span></span><br/>                | <span data-ttu-id="6d12f-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6d12f-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6d12f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6d12f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d12f-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d12f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d12f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6d12f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d12f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d12f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

