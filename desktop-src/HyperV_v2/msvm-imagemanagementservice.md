---
description: Управляет виртуальным носителем (VHD-файлы,. VHDX,. ISO или. VFD) для виртуальной машины.
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Класс Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36a45041ec41b8fbd87801a65fa2b28ac99da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810427"
---
# <a name="msvm_imagemanagementservice-class"></a><span data-ttu-id="5b351-103">\_Класс мсвм)</span><span class="sxs-lookup"><span data-stu-id="5b351-103">Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="5b351-104">Управляет виртуальным носителем (VHD-файлы,. VHDX,. ISO или. VFD) для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b351-104">Manages the virtual media (.vhd, .vhdx, .iso, or .vfd files) for a virtual machine.</span></span>

<span data-ttu-id="5b351-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5b351-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b351-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b351-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="5b351-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5b351-107">Members</span></span>

<span data-ttu-id="5b351-108">Класс **мсвм \_ )** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5b351-108">The **Msvm\_ImageManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="5b351-109">Методы</span><span class="sxs-lookup"><span data-stu-id="5b351-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5b351-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b351-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5b351-111">Методы</span><span class="sxs-lookup"><span data-stu-id="5b351-111">Methods</span></span>

<span data-ttu-id="5b351-112">Класс **мсвм \_ )** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5b351-112">The **Msvm\_ImageManagementService** class has these methods.</span></span>



| <span data-ttu-id="5b351-113">Метод</span><span class="sxs-lookup"><span data-stu-id="5b351-113">Method</span></span>                                                                                                           | <span data-ttu-id="5b351-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5b351-114">Description</span></span>                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b351-115">**аттачвиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-115">**AttachVirtualHardDisk**</span></span>](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="5b351-116">Подключает файл образа виртуального диска в режиме замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="5b351-116">Attaches a virtual disk image file in loopback mode.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="5b351-117">**компактвиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-117">**CompactVirtualHardDisk**</span></span>](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="5b351-118">Сжимает файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-118">Compacts a virtual hard disk file.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="5b351-119">**конвертвиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-119">**ConvertVirtualHardDisk**</span></span>](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="5b351-120">Преобразует существующий виртуальный жесткий диск в другой тип или формат.</span><span class="sxs-lookup"><span data-stu-id="5b351-120">Converts an existing virtual hard disk to a different type or format.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="5b351-121">**конвертвиртуалхарддисктовхдсет**</span><span class="sxs-lookup"><span data-stu-id="5b351-121">**ConvertVirtualHardDiskToVHDSet**</span></span>](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | <span data-ttu-id="5b351-122">Преобразование файла виртуального жесткого диска путем создания нового файла набора ВИРТУАЛЬНЫХ жестких дисков вместе с существующим виртуальным жестким диском.</span><span class="sxs-lookup"><span data-stu-id="5b351-122">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="5b351-123">**креатевиртуалфлоппидиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-123">**CreateVirtualFloppyDisk**</span></span>](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="5b351-124">Создает файл виртуального гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-124">Creates a virtual floppy disk file.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="5b351-125">**креатевиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-125">**CreateVirtualHardDisk**</span></span>](createvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="5b351-126">Создает файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-126">Creates a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="5b351-127">**делетевхдснапшот**</span><span class="sxs-lookup"><span data-stu-id="5b351-127">**DeleteVHDSnapshot**</span></span>](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | <span data-ttu-id="5b351-128">Удаляет запись моментального снимка виртуального жесткого диска в файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="5b351-128">Deletes a VHD Snapshot entry within a VHD Set file.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="5b351-129">**финдмаунтедсторажеимажеинстанце**</span><span class="sxs-lookup"><span data-stu-id="5b351-129">**FindMountedStorageImageInstance**</span></span>](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | <span data-ttu-id="5b351-130">Находит \_ объект Маунтедсторажеимаже мсвм для указанного пути к образу диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-130">Finds a Msvm\_MountedStorageImage object for a given disk image path.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="5b351-131">**жетвхдсетинформатион**</span><span class="sxs-lookup"><span data-stu-id="5b351-131">**GetVHDSetInformation**</span></span>](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | <span data-ttu-id="5b351-132">Извлекает сведения о файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="5b351-132">Retrieves information about a VHD Set file.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="5b351-133">**жетвхдснапшотинформатион**</span><span class="sxs-lookup"><span data-stu-id="5b351-133">**GetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | <span data-ttu-id="5b351-134">Извлекает сведения о моментальном снимке виртуального жесткого диска в файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="5b351-134">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="5b351-135">**жетвиртуалдискчанжес**</span><span class="sxs-lookup"><span data-stu-id="5b351-135">**GetVirtualDiskChanges**</span></span>](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | <span data-ttu-id="5b351-136">Извлекает список изменений в заданной области виртуального диска, начиная с предоставленного ИД отказоустойчивого Отслеживание изменений или идентификатора моментального снимка Вхдсет.</span><span class="sxs-lookup"><span data-stu-id="5b351-136">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span><br/>                                                                                     |
| [<span data-ttu-id="5b351-137">**жетвиртуалхарддисксеттингдата**</span><span class="sxs-lookup"><span data-stu-id="5b351-137">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="5b351-138">Извлекает данные настройки, связанные с файлами виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-138">Retrieves setting data associated with virtual hard disk files.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="5b351-139">**жетвиртуалхарддискстате**</span><span class="sxs-lookup"><span data-stu-id="5b351-139">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | <span data-ttu-id="5b351-140">Извлекает состояние файлов виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-140">Retrieves state of virtual hard disk files.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="5b351-141">**мержевиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-141">**MergeVirtualHardDisk**</span></span>](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | <span data-ttu-id="5b351-142">Слияние дочернего виртуального жесткого диска в цепочке разностного с одним или несколькими родительскими виртуальными жесткими дисками в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5b351-142">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="5b351-143">**оптимизевхдсет**</span><span class="sxs-lookup"><span data-stu-id="5b351-143">**OptimizeVHDSet**</span></span>](msvm-imagemanagementservice-optimizevhdset.md)                                             | <span data-ttu-id="5b351-144">Оптимизирует файл набора виртуальных жестких дисков для использования меньшего места на диске.</span><span class="sxs-lookup"><span data-stu-id="5b351-144">Optimizes a VHD Set file to use less disk space.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="5b351-145">**Равен**</span><span class="sxs-lookup"><span data-stu-id="5b351-145">**RequestStateChange**</span></span>](msvm-imagemanagementservice-requeststatechange.md)                                     | <span data-ttu-id="5b351-146">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="5b351-146">Requests a state change.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="5b351-147">**ресизевиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-147">**ResizeVirtualHardDisk**</span></span>](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="5b351-148">Изменяет размер существующего виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-148">Resizes an existing virtual hard disk.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="5b351-149">**сетпарентвиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-149">**SetParentVirtualHardDisk**</span></span>](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | <span data-ttu-id="5b351-150">Обновляет родительский объект для указанных конечных и дочерних файлов виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-150">Updates the parent for the specified leaf and child virtual hard disk files.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="5b351-151">**сетвхдснапшотинформатион**</span><span class="sxs-lookup"><span data-stu-id="5b351-151">**SetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | <span data-ttu-id="5b351-152">Изменяет запись моментального снимка виртуального жесткого диска в файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="5b351-152">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="5b351-153">Если идентификатор моментального снимка в вопросе уже существует, существующая запись моментального снимка будет перезаписана новой записью.</span><span class="sxs-lookup"><span data-stu-id="5b351-153">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="5b351-154">В противном случае новая запись будет добавлена в файл набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="5b351-154">Otherwise, the new entry will be added to the VHD Set file.</span></span><br/> |
| [<span data-ttu-id="5b351-155">**сетвиртуалхарддисксеттингдата**</span><span class="sxs-lookup"><span data-stu-id="5b351-155">**SetVirtualHardDiskSettingData**</span></span>](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="5b351-156">Задает файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="5b351-156">Sets a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="5b351-157">**StartService**</span><span class="sxs-lookup"><span data-stu-id="5b351-157">**StartService**</span></span>](msvm-imagemanagementservice-startservice.md)                                                 | <span data-ttu-id="5b351-158">запускает службу.</span><span class="sxs-lookup"><span data-stu-id="5b351-158">Starts the service.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="5b351-159">**StopService**</span><span class="sxs-lookup"><span data-stu-id="5b351-159">**StopService**</span></span>](msvm-imagemanagementservice-stopservice.md)                                                   | <span data-ttu-id="5b351-160">останавливает службу.</span><span class="sxs-lookup"><span data-stu-id="5b351-160">Stops the service.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="5b351-161">**валидатеперсистентресерватионсуппорт**</span><span class="sxs-lookup"><span data-stu-id="5b351-161">**ValidatePersistentReservationSupport**</span></span>](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | <span data-ttu-id="5b351-162">Проверяет, может ли файловая система поддерживать виртуальный жесткий диск с включенным постоянным резервированием.</span><span class="sxs-lookup"><span data-stu-id="5b351-162">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="5b351-163">**валидатевиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="5b351-163">**ValidateVirtualHardDisk**</span></span>](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="5b351-164">Проверяет, можно ли открыть образ виртуального диска в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5b351-164">Validates whether a virtual disk image can be opened in read-only mode.</span></span><br/>                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="5b351-165">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b351-165">Properties</span></span>

<span data-ttu-id="5b351-166">Класс **мсвм \_ )** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5b351-166">The **Msvm\_ImageManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b351-167">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="5b351-167">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-168">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="5b351-168">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5b351-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-170">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="5b351-170">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="5b351-171">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5b351-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5b351-172">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="5b351-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-175">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5b351-175">A short description of the object.</span></span> <span data-ttu-id="5b351-176">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления образами Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="5b351-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="5b351-177">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="5b351-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-178">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-180">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="5b351-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5b351-181">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="5b351-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5b351-182">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5b351-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5b351-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5b351-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="5b351-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="5b351-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="5b351-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="5b351-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5b351-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5b351-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5b351-190">)</span><span class="sxs-lookup"><span data-stu-id="5b351-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b351-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5b351-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-194">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5b351-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5b351-195">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ )".</span><span class="sxs-lookup"><span data-stu-id="5b351-195">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ImageManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="5b351-196">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5b351-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-199">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5b351-199">A description of the object.</span></span> <span data-ttu-id="5b351-200">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "обеспечивает обслуживание управления образами для Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="5b351-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Image Management servicing for Hyper-V".</span></span>

</dd> <dt>

<span data-ttu-id="5b351-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5b351-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-202">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-204">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5b351-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5b351-205">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="5b351-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5b351-206">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5b351-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5b351-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="5b351-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="5b351-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="5b351-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="5b351-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="5b351-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="5b351-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5b351-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5b351-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5b351-215">)</span><span class="sxs-lookup"><span data-stu-id="5b351-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b351-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5b351-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-219">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="5b351-219">A display name for the object.</span></span> <span data-ttu-id="5b351-220">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления образами Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="5b351-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="5b351-221">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="5b351-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-222">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-224">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="5b351-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5b351-225">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="5b351-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-226">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5b351-226">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-227">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-229">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="5b351-229">The enabled and disabled states of an element.</span></span> <span data-ttu-id="5b351-230">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="5b351-230">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="5b351-231">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="5b351-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-232">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5b351-232">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-233">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-235">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="5b351-235">The current health of the element.</span></span> <span data-ttu-id="5b351-236">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="5b351-236">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="5b351-237">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="5b351-237">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="5b351-238">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="5b351-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="5b351-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5b351-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-240">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b351-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-242">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b351-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="5b351-243">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5b351-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5b351-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-245">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b351-247">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="5b351-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5b351-248">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="5b351-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5b351-249">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5b351-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-250">**Name**</span><span class="sxs-lookup"><span data-stu-id="5b351-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b351-253">Квалификаторы: **ключ**, **Переопределение** ("имя"), **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5b351-253">Qualifiers: **Key**, **Override** ("Name"), **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b351-254">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="5b351-254">The label by which the object is known.</span></span> <span data-ttu-id="5b351-255">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "vhdsvc".</span><span class="sxs-lookup"><span data-stu-id="5b351-255">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "vhdsvc".</span></span>

</dd> <dt>

<span data-ttu-id="5b351-256">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="5b351-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-257">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-259">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5b351-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5b351-260">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="5b351-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5b351-261">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5b351-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5b351-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5b351-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="5b351-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="5b351-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="5b351-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="5b351-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="5b351-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="5b351-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="5b351-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="5b351-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="5b351-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="5b351-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="5b351-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="5b351-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="5b351-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="5b351-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="5b351-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="5b351-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5b351-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5b351-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5b351-281">)</span><span class="sxs-lookup"><span data-stu-id="5b351-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b351-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5b351-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-283">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="5b351-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5b351-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-285">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="5b351-285">The current status of the object.</span></span> <span data-ttu-id="5b351-286">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="5b351-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-287">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="5b351-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-290">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="5b351-290">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="5b351-291">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="5b351-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5b351-292">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5b351-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5b351-293">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="5b351-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-296">Строка, которая предоставляет сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="5b351-296">A string that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="5b351-297">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5b351-297">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5b351-298">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="5b351-298">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-301">Имя основного владельца службы, если она определена.</span><span class="sxs-lookup"><span data-stu-id="5b351-301">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="5b351-302">Первичный владелец — это первоначальный контактный контакт для службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="5b351-302">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="5b351-303">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5b351-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5b351-304">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="5b351-304">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-305">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-307">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5b351-307">Provides high level status information.</span></span> <span data-ttu-id="5b351-308">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="5b351-308">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5b351-309">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="5b351-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5b351-310">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5b351-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5b351-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5b351-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-312"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="5b351-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="5b351-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="5b351-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5b351-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5b351-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5b351-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5b351-317">)</span><span class="sxs-lookup"><span data-stu-id="5b351-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b351-318">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5b351-318">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-319">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-321">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="5b351-321">The last requested or desired state for the element.</span></span> <span data-ttu-id="5b351-322">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="5b351-322">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="5b351-323">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="5b351-323">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="5b351-324">Конкретный экземпляр **енабледлогикалелемент** может не поддерживать **рекуестедстатечанже**.</span><span class="sxs-lookup"><span data-stu-id="5b351-324">A particular instance of **EnabledLogicalElement** might not support **RequestedStateChange**.</span></span> <span data-ttu-id="5b351-325">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="5b351-325">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="5b351-326">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="5b351-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-327">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="5b351-327">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-328">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5b351-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-330">Указывает, запущена ли служба.</span><span class="sxs-lookup"><span data-stu-id="5b351-330">Indicates whether the service has been started.</span></span> <span data-ttu-id="5b351-331">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="5b351-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="5b351-332">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="5b351-332">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-335">Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу.</span><span class="sxs-lookup"><span data-stu-id="5b351-335">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="5b351-336">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5b351-336">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5b351-337">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="5b351-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="5b351-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5b351-341">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="5b351-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-342">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5b351-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5b351-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-344">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5b351-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5b351-345">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5b351-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-346">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="5b351-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-349">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="5b351-349">The scoping system's creation class name.</span></span> <span data-ttu-id="5b351-350">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="5b351-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="5b351-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5b351-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b351-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-354">Имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="5b351-354">The name of the hosting computer system.</span></span> <span data-ttu-id="5b351-355">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="5b351-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-356">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="5b351-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-357">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b351-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-359">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="5b351-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="5b351-360">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5b351-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5b351-361">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="5b351-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b351-362">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b351-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b351-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b351-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b351-364">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="5b351-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5b351-365">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5b351-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b351-366">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b351-366">Remarks</span></span>

<span data-ttu-id="5b351-367">Доступ к классу **\_ ) мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="5b351-367">Access to the **Msvm\_ImageManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5b351-368">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5b351-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b351-369">Требования</span><span class="sxs-lookup"><span data-stu-id="5b351-369">Requirements</span></span>



| <span data-ttu-id="5b351-370">Требование</span><span class="sxs-lookup"><span data-stu-id="5b351-370">Requirement</span></span> | <span data-ttu-id="5b351-371">Значение</span><span class="sxs-lookup"><span data-stu-id="5b351-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b351-372">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b351-372">Minimum supported client</span></span><br/> | <span data-ttu-id="5b351-373">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5b351-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5b351-374">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b351-374">Minimum supported server</span></span><br/> | <span data-ttu-id="5b351-375">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5b351-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5b351-376">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5b351-376">Namespace</span></span><br/>                | <span data-ttu-id="5b351-377">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5b351-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5b351-378">MOF</span><span class="sxs-lookup"><span data-stu-id="5b351-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b351-379"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b351-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b351-380">DLL</span><span class="sxs-lookup"><span data-stu-id="5b351-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b351-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b351-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b351-382">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b351-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b351-383">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="5b351-383">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="5b351-384">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="5b351-384">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[<span data-ttu-id="5b351-385">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="5b351-385">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

