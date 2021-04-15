---
description: Экспорт данных параметров, передаваемых в метод Експортснапшот \_ класса мсвм коллектионснапшотсервице.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Класс Msvm_CollectionSnapshotExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662379"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a><span data-ttu-id="f21ab-103">\_Класс мсвм коллектионснапшотекспортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="f21ab-103">Msvm\_CollectionSnapshotExportSettingData class</span></span>

<span data-ttu-id="f21ab-104">Экспорт данных параметров, передаваемых в метод Експортснапшот класса [**мсвм \_ коллектионснапшотсервице**](msvm-collectionsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f21ab-104">Export setting data to be passed in to the ExportSnapshot method of [**Msvm\_CollectionSnapshotService**](msvm-collectionsnapshotservice.md) class.</span></span>

<span data-ttu-id="f21ab-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f21ab-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f21ab-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a><span data-ttu-id="f21ab-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f21ab-107">Members</span></span>

<span data-ttu-id="f21ab-108">Класс **мсвм \_ коллектионснапшотекспортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f21ab-108">The **Msvm\_CollectionSnapshotExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f21ab-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f21ab-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f21ab-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f21ab-110">Properties</span></span>

<span data-ttu-id="f21ab-111">Класс **мсвм \_ коллектионснапшотекспортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f21ab-111">The **Msvm\_CollectionSnapshotExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f21ab-112">**баккупинтент**</span><span class="sxs-lookup"><span data-stu-id="f21ab-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f21ab-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f21ab-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f21ab-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f21ab-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f21ab-115">Указывает цель использования экспортированных резервных наборов данных:</span><span class="sxs-lookup"><span data-stu-id="f21ab-115">Indicates the intent how the exported backup sets would be used:</span></span>

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="f21ab-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**Баккупинтентпресервечаин** (1)</span><span class="sxs-lookup"><span data-stu-id="f21ab-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f21ab-117">Все экспортированные полные и разностные резервные наборы данных будут сохраняться по мере их возникновения.</span><span class="sxs-lookup"><span data-stu-id="f21ab-117">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="f21ab-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**Баккупинтентмерже** (2)</span><span class="sxs-lookup"><span data-stu-id="f21ab-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f21ab-119">Экспортированные полные и разностные резервные наборы данных будут объединены для создания полных резервных наборов данных.</span><span class="sxs-lookup"><span data-stu-id="f21ab-119">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f21ab-120">**копивмстораже**</span><span class="sxs-lookup"><span data-stu-id="f21ab-120">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f21ab-121">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f21ab-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f21ab-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f21ab-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f21ab-123">Если **значение — true**, при экспорте виртуальной машины хранилище виртуальной машины будет скопировано.</span><span class="sxs-lookup"><span data-stu-id="f21ab-123">if **true**, the VM storage will be copied when the VM is exported.</span></span> <span data-ttu-id="f21ab-124">В противном случае — **значение false.**</span><span class="sxs-lookup"><span data-stu-id="f21ab-124">Otherwise, **false.**</span></span>

</dd> <dt>

<span data-ttu-id="f21ab-125">**дифферентиалбаккупбасе**</span><span class="sxs-lookup"><span data-stu-id="f21ab-125">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f21ab-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f21ab-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f21ab-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f21ab-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f21ab-128">База для разностного экспорта.</span><span class="sxs-lookup"><span data-stu-id="f21ab-128">Base for differential export.</span></span> <span data-ttu-id="f21ab-129">Это путь к экземпляру [**\_ референцепоинтколлектион мсвм**](msvm-referencepointcollection.md) , который представляет точку ссылки, или путь к экземпляру [**мсвм \_ снапшотколлектион**](msvm-snapshotcollection.md) , который представляет моментальный снимок, который будет использоваться в качестве основы для разностного экспорта.</span><span class="sxs-lookup"><span data-stu-id="f21ab-129">This is either path to an [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the reference point, or path to an [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) instance that represents the snapshot to be used as a base for differential export.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f21ab-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f21ab-130">Requirements</span></span>



| <span data-ttu-id="f21ab-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f21ab-131">Requirement</span></span> | <span data-ttu-id="f21ab-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f21ab-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21ab-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f21ab-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f21ab-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f21ab-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f21ab-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f21ab-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f21ab-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f21ab-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f21ab-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f21ab-137">Namespace</span></span><br/>                | <span data-ttu-id="f21ab-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f21ab-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f21ab-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f21ab-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f21ab-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f21ab-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f21ab-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f21ab-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f21ab-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f21ab-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f21ab-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f21ab-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21ab-144">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="f21ab-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




