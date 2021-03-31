---
description: Предоставляет дополнительные сведения для использования с методом CreateSnapshot \_ класса Виртуалсистемснапшотсервице мсвм.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Класс Msvm_VirtualSystemSnapshotSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423686"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a><span data-ttu-id="bb208-103">\_Класс мсвм виртуалсистемснапшотсеттингдата</span><span class="sxs-lookup"><span data-stu-id="bb208-103">Msvm\_VirtualSystemSnapshotSettingData class</span></span>

<span data-ttu-id="bb208-104">Предоставляет дополнительные сведения для использования с методом [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) класса [**\_ виртуалсистемснапшотсервице мсвм**](msvm-virtualsystemsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="bb208-104">Provides additional information to be used with the [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) method of the [**Msvm\_VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) class.</span></span>

<span data-ttu-id="bb208-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="bb208-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb208-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb208-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a><span data-ttu-id="bb208-107">Члены</span><span class="sxs-lookup"><span data-stu-id="bb208-107">Members</span></span>

<span data-ttu-id="bb208-108">Класс **мсвм \_ виртуалсистемснапшотсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bb208-108">The **Msvm\_VirtualSystemSnapshotSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="bb208-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb208-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb208-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb208-110">Properties</span></span>

<span data-ttu-id="bb208-111">Класс **мсвм \_ виртуалсистемснапшотсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bb208-111">The **Msvm\_VirtualSystemSnapshotSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb208-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="bb208-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb208-113">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bb208-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bb208-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb208-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb208-115">Уровень согласованности моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="bb208-115">The consistency level of the snapshot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb208-116">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bb208-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="bb208-117">С **совместимостью приложений** (1)</span><span class="sxs-lookup"><span data-stu-id="bb208-117">**Application Consistent** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="bb208-118">**Отказоустойчивость (2** )</span><span class="sxs-lookup"><span data-stu-id="bb208-118">**Crash Consistent** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb208-119">**гуестбаккуптипе**</span><span class="sxs-lookup"><span data-stu-id="bb208-119">**GuestBackupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb208-120">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bb208-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bb208-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb208-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb208-122">Тип резервной копии, который будет использоваться в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="bb208-122">Backup type to be used inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="bb208-123">Свойство добавлено в Windows 10, версия 1703</span><span class="sxs-lookup"><span data-stu-id="bb208-123">Property added in Windows 10, version 1703</span></span>

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="bb208-124">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="bb208-124">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="bb208-125">**Full** (1)</span><span class="sxs-lookup"><span data-stu-id="bb208-125">**Full** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="bb208-126">**Копирование** (2)</span><span class="sxs-lookup"><span data-stu-id="bb208-126">**Copy** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb208-127">**игноренонснапшоттабледискс**</span><span class="sxs-lookup"><span data-stu-id="bb208-127">**IgnoreNonSnapshottableDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb208-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bb208-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb208-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb208-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb208-130">Указывает, пропускаются ли не снапшоттабле диски, такие как транзитные диски и диски Fibre Channel, во время создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="bb208-130">Specifies if non-snapshottable disks like passthrough disks and Fibre Channel Disks are to be ignored while creating the snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb208-131">Требования</span><span class="sxs-lookup"><span data-stu-id="bb208-131">Requirements</span></span>



| <span data-ttu-id="bb208-132">Требование</span><span class="sxs-lookup"><span data-stu-id="bb208-132">Requirement</span></span> | <span data-ttu-id="bb208-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bb208-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb208-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb208-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bb208-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bb208-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bb208-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb208-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bb208-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bb208-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bb208-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb208-138">Namespace</span></span><br/>                | <span data-ttu-id="bb208-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bb208-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bb208-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bb208-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb208-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb208-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb208-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bb208-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb208-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb208-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb208-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb208-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb208-145">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="bb208-145">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




