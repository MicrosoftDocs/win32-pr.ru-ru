---
description: Предоставляет дополнительные сведения для использования с методом Експортсистемдефинитион \_ класса Виртуалсистемманажементсервице мсвм.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Класс Msvm_VirtualSystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682504"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a><span data-ttu-id="80076-103">\_Класс мсвм виртуалсистемекспортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="80076-103">Msvm\_VirtualSystemExportSettingData class</span></span>

<span data-ttu-id="80076-104">Предоставляет дополнительные сведения для использования с методом [**експортсистемдефинитион**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="80076-104">Provides additional information to be used with the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="80076-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="80076-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80076-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80076-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a><span data-ttu-id="80076-107">Члены</span><span class="sxs-lookup"><span data-stu-id="80076-107">Members</span></span>

<span data-ttu-id="80076-108">Класс **мсвм \_ виртуалсистемекспортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="80076-108">The **Msvm\_VirtualSystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="80076-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="80076-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80076-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="80076-110">Properties</span></span>

<span data-ttu-id="80076-111">Класс **мсвм \_ виртуалсистемекспортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="80076-111">The **Msvm\_VirtualSystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80076-112">**баккупинтент**</span><span class="sxs-lookup"><span data-stu-id="80076-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-113">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80076-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80076-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-115">Указывает цель использования экспортированных резервных наборов данных.</span><span class="sxs-lookup"><span data-stu-id="80076-115">Indicates the intent on how the exported backup sets would be used.</span></span>

> [!Note]  
> <span data-ttu-id="80076-116">Это свойство было добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="80076-116">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="80076-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**Баккупинтентпресервечаин** (0)</span><span class="sxs-lookup"><span data-stu-id="80076-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span></span>


</dt> <dd>

<span data-ttu-id="80076-118">Все экспортированные полные и разностные резервные наборы данных будут сохраняться по мере их возникновения.</span><span class="sxs-lookup"><span data-stu-id="80076-118">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="80076-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**Баккупинтентмерже** (1)</span><span class="sxs-lookup"><span data-stu-id="80076-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span></span>


</dt> <dd>

<span data-ttu-id="80076-120">Экспортированные полные и разностные резервные наборы данных будут объединены для создания полных резервных наборов данных.</span><span class="sxs-lookup"><span data-stu-id="80076-120">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80076-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="80076-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80076-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80076-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80076-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80076-124">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="80076-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="80076-125">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="80076-125">A short description of the object.</span></span> <span data-ttu-id="80076-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="80076-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="80076-127">**каптуреливестате**</span><span class="sxs-lookup"><span data-stu-id="80076-127">**CaptureLiveState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-128">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80076-128">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80076-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-130">Указывает, какое состояние следует записать, если целевой объект экспорта является работающей виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="80076-130">Indicates what state to capture if the target of the export is a running VM.</span></span>

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span data-ttu-id="80076-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**Каптурекрашконсистентстате** (0)</span><span class="sxs-lookup"><span data-stu-id="80076-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span></span>


</dt> <dd>

<span data-ttu-id="80076-132">Файлы сохраненного состояния не будут экспортированы для работающей виртуальной машины, поместив ее в состояние сбоя.</span><span class="sxs-lookup"><span data-stu-id="80076-132">No saved state files will be exported for the running VM, placing it in a crash consistent state.</span></span>

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span data-ttu-id="80076-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**Каптуресаведстате** (1)</span><span class="sxs-lookup"><span data-stu-id="80076-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span></span>


</dt> <dd>

<span data-ttu-id="80076-134">Файлы сохраненного состояния для работающей виртуальной машины будут экспортированы вместе с конфигурацией виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-134">Saved state files for the running VM will be exported along with the VM configuration.</span></span>

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span data-ttu-id="80076-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**Каптуреаппконсистентстате** (2)</span><span class="sxs-lookup"><span data-stu-id="80076-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span></span>


</dt> <dd>

<span data-ttu-id="80076-136">Будет экспортировано состояние работающей виртуальной машины в режиме совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="80076-136">Application-consistent state of the running VM will be exported.</span></span>

> [!Note]  
> <span data-ttu-id="80076-137">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="80076-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80076-138">**кописнапшотконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="80076-138">**CopySnapshotConfiguration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-139">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80076-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80076-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-141">Указывает, какие моментальные снимки должны быть экспортированы с помощью виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-141">Indicates what snapshots are to be exported with the virtual machine.</span></span>

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span data-ttu-id="80076-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**Експорталлснапшотс** (0)</span><span class="sxs-lookup"><span data-stu-id="80076-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span></span>


</dt> <dd>

<span data-ttu-id="80076-143">Все моментальные снимки будут экспортированы с помощью виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-143">All snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span data-ttu-id="80076-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**Експортноснапшотс** (1)</span><span class="sxs-lookup"><span data-stu-id="80076-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span></span>


</dt> <dd>

<span data-ttu-id="80076-145">Моментальные снимки не будут экспортированы с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="80076-145">No snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span data-ttu-id="80076-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**Експортонеснапшот** (2)</span><span class="sxs-lookup"><span data-stu-id="80076-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="80076-147">Моментальные снимки, определяемые свойством **снапшотвиртуалсистем** , будут экспортированы вместе с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="80076-147">The snapshots identified by the **SnapshotVirtualSystem** property will be exported with the virtual machine.</span></span> <span data-ttu-id="80076-148">Свойства **копивмстораже** и **копивмрунтимеинформатион** не учитываются, сведения о хранилище и времени выполнения экспортируются вместе с виртуальной машиной, а все разностные диски VHD будут ОБЪЕДИНЕНЫ в новый виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="80076-148">The **CopyVmStorage** and **CopyVmRuntimeInformation** properties are ignored, storage and run-time information is exported with the virtual machine, and any VHD differencing disks will be merged into a new VHD.</span></span>

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span data-ttu-id="80076-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**Експортонеснапшотфорбаккуп** (3)</span><span class="sxs-lookup"><span data-stu-id="80076-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span></span>


</dt> <dd>

<span data-ttu-id="80076-150">Моментальный снимок, определяемый свойством **снапшотвиртуалсистем** , будет экспортирован в целях резервного копирования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-150">The snapshot identified by the **SnapshotVirtualSystem** property will be exported for the purpose of backing up the VM.</span></span> <span data-ttu-id="80076-151">Экспортированная конфигурация будет использовать идентификатор виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-151">The exported configuration will use ID of the VM.</span></span>

> [!Note]  
> <span data-ttu-id="80076-152">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="80076-152">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80076-153">**копивмрунтимеинформатион**</span><span class="sxs-lookup"><span data-stu-id="80076-153">**CopyVmRuntimeInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-154">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80076-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80076-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-156">Указывает, будут ли копироваться сведения о времени выполнения виртуальной машины при экспорте виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-156">Indicates whether the virtual machine run-time information will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="80076-157">Значение</span><span class="sxs-lookup"><span data-stu-id="80076-157">Value</span></span>                                                                                | <span data-ttu-id="80076-158">Значение</span><span class="sxs-lookup"><span data-stu-id="80076-158">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80076-159"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="80076-159"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="80076-160">Сведения о времени выполнения виртуальной машины будут скопированы.</span><span class="sxs-lookup"><span data-stu-id="80076-160">The virtual machine run-time information will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="80076-161"><dt>**Неверно**</dt></span><span class="sxs-lookup"><span data-stu-id="80076-161"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="80076-162">Сведения о времени выполнения виртуальной машины не будут скопированы.</span><span class="sxs-lookup"><span data-stu-id="80076-162">The virtual machine run-time information will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80076-163">**копивмстораже**</span><span class="sxs-lookup"><span data-stu-id="80076-163">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-164">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80076-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80076-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-166">Указывает, будет ли копироваться хранилище виртуальной машины при экспорте виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-166">Indicates whether the virtual machine storage will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="80076-167">Значение</span><span class="sxs-lookup"><span data-stu-id="80076-167">Value</span></span>                                                                                | <span data-ttu-id="80076-168">Значение</span><span class="sxs-lookup"><span data-stu-id="80076-168">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="80076-169"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="80076-169"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="80076-170">Будет скопировано хранилище виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-170">The virtual machine storage will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="80076-171"><dt>**Неверно**</dt></span><span class="sxs-lookup"><span data-stu-id="80076-171"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="80076-172">Хранилище виртуальной машины не будет скопировано.</span><span class="sxs-lookup"><span data-stu-id="80076-172">The virtual machine storage will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80076-173">**креатевмекспортсубдиректори**</span><span class="sxs-lookup"><span data-stu-id="80076-173">**CreateVmExportSubdirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-174">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80076-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80076-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-176">Указывает, будет ли создаваться подкаталог с именем виртуальной машины при экспорте виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="80076-176">Indicates whether a subdirectory with the name of the virtual machine will be created when the virtual machine is exported.</span></span>



| <span data-ttu-id="80076-177">Значение</span><span class="sxs-lookup"><span data-stu-id="80076-177">Value</span></span>                                                                                | <span data-ttu-id="80076-178">Значение</span><span class="sxs-lookup"><span data-stu-id="80076-178">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="80076-179"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="80076-179"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="80076-180">Будет создан подкаталог.</span><span class="sxs-lookup"><span data-stu-id="80076-180">A subdirectory will be created.</span></span><br/>     |
| <dl> <span data-ttu-id="80076-181"><dt>**Неверно**</dt></span><span class="sxs-lookup"><span data-stu-id="80076-181"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="80076-182">Подкаталог не будет создан.</span><span class="sxs-lookup"><span data-stu-id="80076-182">A subdirectory will not be created.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80076-183">**Описание**</span><span class="sxs-lookup"><span data-stu-id="80076-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80076-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80076-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80076-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80076-186">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="80076-186">A description of the object.</span></span> <span data-ttu-id="80076-187">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="80076-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="80076-188">**дифферентиалбаккупбасе**</span><span class="sxs-lookup"><span data-stu-id="80076-188">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80076-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80076-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-191">База для разностного экспорта.</span><span class="sxs-lookup"><span data-stu-id="80076-191">Base for differential export.</span></span> <span data-ttu-id="80076-192">Это путь к экземпляру [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , который представляет точку ссылки или путь к экземпляру [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , который представляет моментальный снимок, используемый в качестве основы для разностного экспорта.</span><span class="sxs-lookup"><span data-stu-id="80076-192">This is either path to a [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance that represents the reference point or path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be used as a base for differential export.</span></span> <span data-ttu-id="80076-193">Если свойство **кописнапшотконфигуратион** не имеет значение 3 (**експортонеснапшотфорбаккуп**), это свойство игнорируется.</span><span class="sxs-lookup"><span data-stu-id="80076-193">If the **CopySnapshotConfiguration** property is not set to 3(**ExportOneSnapshotForBackup**), this property is ignored.</span></span>

> [!Note]  
> <span data-ttu-id="80076-194">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="80076-194">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="80076-195">**дисабледифферентиалофигноредстораже**</span><span class="sxs-lookup"><span data-stu-id="80076-195">**DisableDifferentialOfIgnoredStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80076-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80076-197">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-198">Указывает, будут ли создаваться разностные диски или нет для хранилища, пропущенного во время экспорта.</span><span class="sxs-lookup"><span data-stu-id="80076-198">Indicates whether differencing disks will be created or not for storage ignored during export.</span></span> <span data-ttu-id="80076-199">По умолчанию установлено значение false, что означает, что разностные диски создаются для хранилища, которое не будет скопировано в назначение экспорта.</span><span class="sxs-lookup"><span data-stu-id="80076-199">By default this is set to false, which means that differencing disks are created for the storage that is not going to be copied over to the export destination.</span></span>

> [!Note]  
> <span data-ttu-id="80076-200">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="80076-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="80076-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="80076-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80076-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80076-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80076-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80076-204">Отображаемое имя для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="80076-204">The display name for this instance.</span></span> <span data-ttu-id="80076-205">Кроме того, отображаемое имя можно использовать в качестве свойства индекса для поиска или запроса.</span><span class="sxs-lookup"><span data-stu-id="80076-205">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="80076-206">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80076-206">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="80076-207">**ексклудедвиртуалхарддискс**</span><span class="sxs-lookup"><span data-stu-id="80076-207">**ExcludedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-208">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="80076-208">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="80076-209">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-209">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-210">Массив идентификаторов экземпляров [**мсвм \_ сторажеаллокатионсеттингдата**](msvm-storageallocationsettingdata.md) (расд), которые представляют виртуальные жесткие диски, запрашиваемые для исключения из операции экспорта.</span><span class="sxs-lookup"><span data-stu-id="80076-210">Array of [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) instance IDs that represent the virtual hard disks that are requested to be excluded from the export operation.</span></span> <span data-ttu-id="80076-211">Если хотя бы один из предоставленных идентификаторов не является допустимым подключенным виртуальным жестким диском, операция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="80076-211">If at least one of the supplied IDs is not a valid attached virtual hard disk, the operation will fail.</span></span>

<span data-ttu-id="80076-212">Виртуальные жесткие диски, на которые ссылается это свойство, могут быть из виртуальной машины и (или) из моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="80076-212">The virtual hard disks referenced by this property may be from the VM and/or from any of its snapshots.</span></span> <span data-ttu-id="80076-213">Исключение виртуальных жестких дисков не поддерживается, если свойство **кописнапшотконфигуратион** имеет значение 0 (експорталлснапшотс).</span><span class="sxs-lookup"><span data-stu-id="80076-213">Exclusion of virtual hard disks is not supported when property **CopySnapshotConfiguration** is set to 0(ExportAllSnapshots).</span></span>

<span data-ttu-id="80076-214">Обратите внимание, что идентификатор экземпляра РАСД для виртуальных жестких дисков представляет расположение, к которому они присоединены, и исключение через этот идентификатор исключает все виртуальные жесткие диски, подключенные в этом расположении в дереве моментальных снимков виртуальной машины, независимо от того, действительно ли они являются действительной цепочкой виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="80076-214">Note that the RASD instance ID for virtual hard disks represents the location they are attached to, and excluding through this ID excludes all virtual hard disks attached in that location throughout the virtual machine's snapshot tree, regardless of them really being a valid virtual hard disk chain.</span></span>

> [!Note]  
> <span data-ttu-id="80076-215">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="80076-215">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="80076-216">**експортфорливемигратион**</span><span class="sxs-lookup"><span data-stu-id="80076-216">**ExportForLiveMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-217">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80076-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80076-218">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-219">Указывает, должна ли экспортированная виртуальная машина использоваться в динамической миграции.</span><span class="sxs-lookup"><span data-stu-id="80076-219">Indicates whether the exported VM is intended to be used in live migration.</span></span>

> [!Note]  
> <span data-ttu-id="80076-220">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="80076-220">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="80076-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="80076-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80076-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80076-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80076-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80076-224">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="80076-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="80076-225">В области создания экземпляра пространства имен непрозрачно и уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="80076-225">Within the scope of the instantiating Namespace, opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="80076-226">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80076-226">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="80076-227">**снапшотвиртуалсистем**</span><span class="sxs-lookup"><span data-stu-id="80076-227">**SnapshotVirtualSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80076-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80076-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80076-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80076-229">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80076-230">Путь к экземпляру [**\_ виртуалсистемсеттингдата мсвм**](msvm-virtualsystemsettingdata.md) , который представляет моментальный снимок, экспортируемый с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="80076-230">Path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be exported with the virtual machine.</span></span> <span data-ttu-id="80076-231">Если свойство **кописнапшотконфигуратион** не имеет значение 2 (експортонеснапшот), это свойство игнорируется.</span><span class="sxs-lookup"><span data-stu-id="80076-231">If the **CopySnapshotConfiguration** property is not set to 2 (ExportOneSnapshot), this property is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80076-232">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80076-232">Remarks</span></span>

<span data-ttu-id="80076-233">Доступ к классу **\_ виртуалсистемекспортсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="80076-233">Access to the **Msvm\_VirtualSystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="80076-234">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="80076-234">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="80076-235">Требования</span><span class="sxs-lookup"><span data-stu-id="80076-235">Requirements</span></span>



| <span data-ttu-id="80076-236">Требование</span><span class="sxs-lookup"><span data-stu-id="80076-236">Requirement</span></span> | <span data-ttu-id="80076-237">Значение</span><span class="sxs-lookup"><span data-stu-id="80076-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80076-238">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80076-238">Minimum supported client</span></span><br/> | <span data-ttu-id="80076-239">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="80076-239">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="80076-240">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80076-240">Minimum supported server</span></span><br/> | <span data-ttu-id="80076-241">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="80076-241">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80076-242">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="80076-242">Namespace</span></span><br/>                | <span data-ttu-id="80076-243">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="80076-243">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="80076-244">MOF</span><span class="sxs-lookup"><span data-stu-id="80076-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80076-245"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80076-245"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80076-246">DLL</span><span class="sxs-lookup"><span data-stu-id="80076-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80076-247"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80076-247"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80076-248">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80076-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80076-249">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="80076-249">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="80076-250">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="80076-250">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> <dt>

[<span data-ttu-id="80076-251">**експортсистемдефинитион**</span><span class="sxs-lookup"><span data-stu-id="80076-251">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

