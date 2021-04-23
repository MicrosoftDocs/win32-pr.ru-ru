---
description: Связывает виртуальную систему с моментальным снимком, захваченным из виртуальной системы.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Класс Msvm_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991464"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a><span data-ttu-id="6c0da-103">\_Класс мсвм снапшотофвиртуалсистем</span><span class="sxs-lookup"><span data-stu-id="6c0da-103">Msvm\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="6c0da-104">Связывает виртуальную систему с моментальным снимком, захваченным из виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="6c0da-104">Associates a virtual system with a snapshot that was captured from the virtual system.</span></span>

<span data-ttu-id="6c0da-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6c0da-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0da-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c0da-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6c0da-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6c0da-107">Members</span></span>

<span data-ttu-id="6c0da-108">Класс **мсвм \_ снапшотофвиртуалсистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6c0da-108">The **Msvm\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="6c0da-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6c0da-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c0da-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6c0da-110">Properties</span></span>

<span data-ttu-id="6c0da-111">Класс **мсвм \_ снапшотофвиртуалсистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6c0da-111">The **Msvm\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c0da-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="6c0da-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0da-113">Тип данных: **[ **мсвм \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="6c0da-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6c0da-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6c0da-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0da-115">Ссылка на экземпляр класса [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющий виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="6c0da-115">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system.</span></span> <span data-ttu-id="6c0da-116">Это свойство является производным [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="6c0da-116">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="6c0da-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="6c0da-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0da-118">Тип данных: **[ **мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="6c0da-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6c0da-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6c0da-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0da-120">Ссылка на экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , представляющий моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="6c0da-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the snapshot.</span></span> <span data-ttu-id="6c0da-121">Это свойство является производным [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="6c0da-121">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c0da-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6c0da-122">Requirements</span></span>



| <span data-ttu-id="6c0da-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6c0da-123">Requirement</span></span> | <span data-ttu-id="6c0da-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6c0da-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c0da-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c0da-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6c0da-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6c0da-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6c0da-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c0da-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6c0da-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6c0da-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c0da-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6c0da-129">Namespace</span></span><br/>                | <span data-ttu-id="6c0da-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6c0da-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6c0da-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6c0da-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c0da-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c0da-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c0da-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6c0da-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c0da-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c0da-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c0da-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c0da-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0da-136">**\_СНАПШОТОФВИРТУАЛСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="6c0da-136">**CIM\_SnapshotOfVirtualSystem**</span></span>](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[<span data-ttu-id="6c0da-137">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="6c0da-137">**CreateSnapshot**</span></span>](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

