---
description: Представляет параметры, относящиеся к выделению виртуального хранилища.
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Класс Msvm_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d889c262eee9d827a02547ddbfdff2cb121cb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265240"
---
# <a name="msvm_storageallocationsettingdata-class"></a><span data-ttu-id="46726-103">\_Класс мсвм сторажеаллокатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="46726-103">Msvm\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="46726-104">Представляет параметры, относящиеся к выделению виртуального хранилища.</span><span class="sxs-lookup"><span data-stu-id="46726-104">Represents settings specifically related to the allocation of virtual storage.</span></span>

<span data-ttu-id="46726-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="46726-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46726-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46726-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a><span data-ttu-id="46726-107">Члены</span><span class="sxs-lookup"><span data-stu-id="46726-107">Members</span></span>

<span data-ttu-id="46726-108">Класс **мсвм \_ сторажеаллокатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="46726-108">The **Msvm\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="46726-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="46726-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46726-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="46726-110">Properties</span></span>

<span data-ttu-id="46726-111">Класс **мсвм \_ сторажеаллокатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="46726-111">The **Msvm\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46726-112">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="46726-112">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46726-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46726-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-115">Указывает доступ к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="46726-115">Specifies the storage access.</span></span> <span data-ttu-id="46726-116">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-116">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="46726-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="46726-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46726-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="46726-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>
</dt> <dt>

<span data-ttu-id="46726-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="46726-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="46726-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="46726-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46726-121">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="46726-121">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-124">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="46726-124">The address of the resource.</span></span> <span data-ttu-id="46726-125">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-125">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-126">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="46726-126">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-129">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="46726-129">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="46726-130">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="46726-130">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="46726-131">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-131">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-132">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="46726-132">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-135">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="46726-135">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="46726-136">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-136">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-137">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="46726-137">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46726-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46726-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-140">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="46726-140">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="46726-141">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-141">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-142">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="46726-142">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46726-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46726-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-145">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="46726-145">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="46726-146">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-147">**качингмоде**</span><span class="sxs-lookup"><span data-stu-id="46726-147">**CachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-148">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46726-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46726-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-150">Указывает, следует ли использовать кэширование файлов в памяти для этого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="46726-150">Indicates whether and how in-memory file caching should be used for this VHD.</span></span> <span data-ttu-id="46726-151">Политика по умолчанию задается в поле **дефаултвиртуалхарддисккачингмоде** класса [**\_ виртуалсистемманажементсервицесеттингдата мсвм**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="46726-151">The default policy is set in the **DefaultVirtualHardDiskCachingMode** field of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="46726-152">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="46726-152">Added in Windows 10.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46726-153">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="46726-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="46726-154">**По умолчанию** (2)</span><span class="sxs-lookup"><span data-stu-id="46726-154">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="46726-155">**Без кэширования** (3)</span><span class="sxs-lookup"><span data-stu-id="46726-155">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="46726-156">**Кэшировать родители-предки** (4)</span><span class="sxs-lookup"><span data-stu-id="46726-156">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46726-157">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="46726-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46726-160">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="46726-160">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="46726-161">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="46726-161">A short description of the object.</span></span> <span data-ttu-id="46726-162">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "параметры по умолчанию для образа жесткого диска".</span><span class="sxs-lookup"><span data-stu-id="46726-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hard Disk Image Default Settings".</span></span>

</dd> <dt>

<span data-ttu-id="46726-163">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="46726-163">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-164">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="46726-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46726-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-166">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="46726-166">The device to which this resource is connected.</span></span> <span data-ttu-id="46726-167">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-167">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-168">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="46726-168">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-169">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46726-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46726-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-171">Видимость потребителя для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="46726-171">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="46726-172">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-172">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="46726-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="46726-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46726-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Пройдено** (2)</span><span class="sxs-lookup"><span data-stu-id="46726-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passed-Through** (2)</span></span>
</dt> <dt>

<span data-ttu-id="46726-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Виртуализированный** (3)</span><span class="sxs-lookup"><span data-stu-id="46726-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualized** (3)</span></span>
</dt> <dt>

<span data-ttu-id="46726-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Не представлено** (4)</span><span class="sxs-lookup"><span data-stu-id="46726-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Not represented** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46726-177">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46726-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-180">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="46726-180">A description of the object.</span></span> <span data-ttu-id="46726-181">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "описывает параметры по умолчанию для ресурсов образа жесткого диска".</span><span class="sxs-lookup"><span data-stu-id="46726-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the default settings for the hard disk image resources".</span></span>

</dd> <dt>

<span data-ttu-id="46726-182">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="46726-182">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-185">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="46726-185">A display name for the object.</span></span> <span data-ttu-id="46726-186">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="46726-186">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="46726-187">**хостекстентнаме**</span><span class="sxs-lookup"><span data-stu-id="46726-187">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-190">Уникальный идентификатор для экстента узла.</span><span class="sxs-lookup"><span data-stu-id="46726-190">A unique identifier for the host extent.</span></span> <span data-ttu-id="46726-191">Определенная область узла используется для выделения ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="46726-191">The identified host extent is used for the storage resource allocation.</span></span> <span data-ttu-id="46726-192">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-192">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="46726-193">**хостекстентнамеформат**</span><span class="sxs-lookup"><span data-stu-id="46726-193">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-194">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46726-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46726-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-196">Определяет формат, используемый для свойства **хостекстентнаме** .</span><span class="sxs-lookup"><span data-stu-id="46726-196">Identifies the format that is used for the **HostExtentName** property.</span></span> <span data-ttu-id="46726-197">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-197">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="46726-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="46726-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46726-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="46726-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="46726-200"><span id="SNVM"></span><span id="snvm"></span>**Снвм** (7)</span><span class="sxs-lookup"><span data-stu-id="46726-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="46726-201"><span id="NAA"></span><span id="naa"></span>**Удаляем** (9)</span><span class="sxs-lookup"><span data-stu-id="46726-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="46726-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="46726-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>
</dt> <dt>

<span data-ttu-id="46726-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="46726-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>
</dt> <dt>

<span data-ttu-id="46726-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Имя устройства ОС** (12)</span><span class="sxs-lookup"><span data-stu-id="46726-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>
</dt> <dt>

<span data-ttu-id="46726-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="46726-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="46726-206">)</span><span class="sxs-lookup"><span data-stu-id="46726-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46726-207">**хостекстентнаменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="46726-207">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46726-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46726-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-210">Если областью узла является том SCSI, предпочтительным источником для имен томов SCSI является SCSI VPD Page 83 Responses.</span><span class="sxs-lookup"><span data-stu-id="46726-210">If the host extent is a SCSI volume, then the preferred source for SCSI volume names is SCSI VPD Page 83 responses.</span></span> <span data-ttu-id="46726-211">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-211">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="46726-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="46726-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46726-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="46726-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="46726-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="46726-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span></span>
</dt> <dt>

<span data-ttu-id="46726-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="46726-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span></span>
</dt> <dt>

<span data-ttu-id="46726-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="46726-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span></span>
</dt> <dt>

<span data-ttu-id="46726-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="46726-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span></span>
</dt> <dt>

<span data-ttu-id="46726-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**Нодеввн** (6)</span><span class="sxs-lookup"><span data-stu-id="46726-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span></span>
</dt> <dt>

<span data-ttu-id="46726-219"><span id="SNVM"></span><span id="snvm"></span>**Снвм** (7)</span><span class="sxs-lookup"><span data-stu-id="46726-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="46726-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Пространство имен устройств ОС** (8)</span><span class="sxs-lookup"><span data-stu-id="46726-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**OS Device Namespace** (8)</span></span>
</dt> <dt>

<span data-ttu-id="46726-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="46726-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="46726-222">)</span><span class="sxs-lookup"><span data-stu-id="46726-222">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46726-223">**хостекстентстартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="46726-223">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-224">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46726-224">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46726-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-226">Определяет начальный адрес в области хранения узла, определяемый свойством **хостекстентнаме** , который используется для размещения виртуального экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="46726-226">Identifies the starting address on the host storage extent, identified by the **HostExtentName** property, that is used for the allocation of the virtual storage extent.</span></span> <span data-ttu-id="46726-227">Значение **null** указывает на отсутствие прямого сопоставления экстента виртуальной памяти с пространством хранения на упоминаемом узле.</span><span class="sxs-lookup"><span data-stu-id="46726-227">A **Null** value indicates that there is no direct mapping of the virtual storage extent to the referenced host storage extent.</span></span> <span data-ttu-id="46726-228">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-228">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="46726-229">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="46726-229">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-230">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="46726-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46726-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-232">Каждому устройству на виртуальной машине можно назначить только один ресурс узла, поэтому можно установить только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="46726-232">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="46726-233">Для устройств, поддерживающих эту функцию, установите первый элемент массива **хостресаурце** , чтобы он содержал ссылку на базовый ресурс узла, который нужно назначить.</span><span class="sxs-lookup"><span data-stu-id="46726-233">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="46726-234">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-234">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="46726-235">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="46726-235">This is a read-only property.</span></span> <span data-ttu-id="46726-236">Но если свойство **ResourceType** имеет значение 31 (логический диск) и свойство **ресаурцесубтипе** имеет значение "Microsoft: Hyper-v: Virtual жесткий диск", "Microsoft: Hyper-v: виртуальный компакт-или DVD-диск" или "Microsoft: Hyper-v: виртуальная дискета", свойство **хостресаурце** можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="46726-236">But if the **ResourceType** property is 31 (Logical Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Virtual Hard Disk", "Microsoft:Hyper-V:Virtual CD/DVD Disk", or "Microsoft:Hyper-V:Virtual Floppy Disk", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="46726-237">**хостресаурцеблокксизе**</span><span class="sxs-lookup"><span data-stu-id="46726-237">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-238">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46726-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46726-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-240">Размер (в байтах) блоков, выделенных на узле в результате этого выделения ресурсов хранилища или запроса на выделение ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="46726-240">The size, in bytes, of the blocks that are allocated at the host as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="46726-241">Если размер блока является переменным, то будет указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="46726-241">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="46726-242">Если размер блока неизвестен или если не применяется концепция блока, будет использовано значение 1.</span><span class="sxs-lookup"><span data-stu-id="46726-242">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="46726-243">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-243">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="46726-244">**игнорефлушес**</span><span class="sxs-lookup"><span data-stu-id="46726-244">**IgnoreFlushes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-245">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46726-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46726-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-247">Если задано значение true, Hyper-V будет игнорировать обратную запись на диск для этой конкретной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="46726-247">If set to true, Hyper-V will ignore write back flushing for that particular virtual machine.</span></span> <span data-ttu-id="46726-248">Если задано значение false, то Hyper-V продолжает выполнять обратную запись на диск при каждом сбросе.</span><span class="sxs-lookup"><span data-stu-id="46726-248">If set to false, Hyper-V will continue to write back to the disk on every flush.</span></span> <span data-ttu-id="46726-249">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="46726-249">The default setting is false.</span></span>

<span data-ttu-id="46726-250">**Windows 10:** Это значение не поддерживается до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="46726-250">**Windows 10:** This value is not supported until Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="46726-251">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="46726-251">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46726-254">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="46726-254">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="46726-255">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="46726-255">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="46726-256">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="46726-256">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="46726-257">**иопсаллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="46726-257">**IOPSAllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-260">Указывает единицы распределения, используемые свойствами **иопслимит** и **иопсресерватион** .</span><span class="sxs-lookup"><span data-stu-id="46726-260">Specifies the allocation units used by the **IOPSLimit** and **IOPSReservation** properties.</span></span> <span data-ttu-id="46726-261">Это свойство всегда имеет значение:</span><span class="sxs-lookup"><span data-stu-id="46726-261">This property always has the value:</span></span>

<span data-ttu-id="46726-262">"Count (нормализованные операции ввода-вывода) в секунду"</span><span class="sxs-lookup"><span data-stu-id="46726-262">"count(normalized I/O) / second"</span></span>

<span data-ttu-id="46726-263">Пропускная способность измеряется в нормализованных операциях ввода-вывода в секунду, а не в необработанных ЧИСЛАх.</span><span class="sxs-lookup"><span data-stu-id="46726-263">Throughput is measured in normalized I/O operations per second (IOPS) instead of raw IOPS.</span></span> <span data-ttu-id="46726-264">При использовании нормализованных операций ввода-вывода каждый запрос на ввод/вывод учитывается как 1 нормализованный ввод-вывод, если размер запроса меньше или равен предопределенному базовому размеру (8 КБ).</span><span class="sxs-lookup"><span data-stu-id="46726-264">When using normalized IOPS, each I/O request is accounted for as 1 normalized I/O if the size of the request is less than or equal to a predefined base size (8 KB).</span></span> <span data-ttu-id="46726-265">Запросы, размер которых превышает базовый размер, задаются как N операций ввода-вывода, где N — округленное значение размера запроса, деленное на базовый размер.</span><span class="sxs-lookup"><span data-stu-id="46726-265">Requests that are larger than the base size are accounted for as N I/O operations, where N is the rounded-up value of the request size divided by the base size.</span></span> <span data-ttu-id="46726-266">Например, если базовый размер равен 8 КБ, то запрос размером 16 КБ считается 2 нормализованными операциями ввода-вывода, запросом 32 КБ как 4 нормализованными операциями ввода-вывода и т. д.</span><span class="sxs-lookup"><span data-stu-id="46726-266">For example, if the base size is 8 KB, a 16-KB request is counted as 2 normalized I/O operations, a 32-KB request as 4 normalized I/O operations, and so on.</span></span>

<span data-ttu-id="46726-267">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="46726-267">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="46726-268">**иопслимит**</span><span class="sxs-lookup"><span data-stu-id="46726-268">**IOPSLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-269">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46726-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46726-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46726-271">Квалификаторы: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span><span class="sxs-lookup"><span data-stu-id="46726-271">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="46726-272">Максимальное количество операций ввода-вывода в секунду, которые будут обслуживаться для этого экстента виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="46726-272">The maximum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span> <span data-ttu-id="46726-273">Если значение не определено или равно нулю, количество операций ввода-вывода, которое может выдавать устройство, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="46726-273">If the value isn't defined or is zero, there is no limit to the number of IOPS that the device can issue.</span></span>

> [!Note]  
> <span data-ttu-id="46726-274">Для изменения значения этого свойства можно использовать метод [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="46726-274">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="46726-275">Это свойство имеет смысл только для экземпляров **мсвм \_ сторажеаллокатионсеттингдата** , которые запрашивают выделение ресурсов для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="46726-275">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="46726-276">При выделении ресурсов для дочернего пула он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="46726-276">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="46726-277">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="46726-277">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="46726-278">**иопсресерватион**</span><span class="sxs-lookup"><span data-stu-id="46726-278">**IOPSReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-279">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46726-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46726-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46726-281">Квалификаторы: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span><span class="sxs-lookup"><span data-stu-id="46726-281">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="46726-282">Минимальное количество операций ввода-вывода в секунду, которые будут обслуживаться для этого экстента виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="46726-282">The minimum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span>

<span data-ttu-id="46726-283">Если определены оба **иопслимит** и **Иопсресерватион** , значение **иопслимит** должно быть больше или равно значению **иопсресерватион**.</span><span class="sxs-lookup"><span data-stu-id="46726-283">If both **IOPSLimit** and **IOPSReservation** are defined, the value of **IOPSLimit** must be greater than or equal to the value of **IOPSReservation**.</span></span>

> [!Note]  
> <span data-ttu-id="46726-284">Для изменения значения этого свойства можно использовать метод [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="46726-284">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="46726-285">Это свойство имеет смысл только для экземпляров **мсвм \_ сторажеаллокатионсеттингдата** , которые запрашивают выделение ресурсов для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="46726-285">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="46726-286">При выделении ресурсов для дочернего пула он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="46726-286">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="46726-287">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="46726-287">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="46726-288">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="46726-288">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-289">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46726-289">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46726-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-291">Максимальное число блоков, которые будут предоставлены для этого выделения ресурсов хранилища на узле.</span><span class="sxs-lookup"><span data-stu-id="46726-291">The maximum number of blocks that will be granted for this storage resource allocation at the host.</span></span> <span data-ttu-id="46726-292">Размер блока задается свойством **хостресаурцеблокксизе** .</span><span class="sxs-lookup"><span data-stu-id="46726-292">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="46726-293">Обычно значение этого свойства будет отражать максимальный размер выделенного экстента, который соответствует размеру виртуальной памяти, предоставленной потребителю.</span><span class="sxs-lookup"><span data-stu-id="46726-293">Usually the value of this property would reflect a maximum size for the allocated host extent that matches the size of the virtual storage extent presented to the consumer.</span></span> <span data-ttu-id="46726-294">Значение меньше, чем это указывает на ситуацию, когда ожидается разреженный экстент виртуального хранилища, где скорость заполнения ограничена значением свойства Limit.</span><span class="sxs-lookup"><span data-stu-id="46726-294">A value less than that would indicate a situation where a sparsely populated virtual storage extent is expected, where the fill rate is limited by the value of the Limit property.</span></span> <span data-ttu-id="46726-295">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-295">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-296">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="46726-296">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-297">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46726-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46726-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-299">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="46726-299">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="46726-300">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-300">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-301">**осерхостекстентнамеформат**</span><span class="sxs-lookup"><span data-stu-id="46726-301">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-304">Строка, описывающая формат свойства **хостекстентнаме** , если свойство **хостекстентнамеформат** равно 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="46726-304">A string that describes the format of the **HostExtentName** property if the **HostExtentNameFormat** property is 1 (Other).</span></span> <span data-ttu-id="46726-305">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-305">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="46726-306">**осерхостекстентнаменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="46726-306">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-309">Строка, описывающая пространство имен свойства **хостекстентнаме** , если свойство **хостекстентнаменамеспаце** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="46726-309">A string that describes the namespace of the **HostExtentName** property if the **HostExtentNameNamespace** property contains 1 (Other).</span></span> <span data-ttu-id="46726-310">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-310">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="46726-311">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="46726-311">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-314">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorsettingdata.md) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="46726-314">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="46726-315">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-315">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-316">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="46726-316">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-319">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="46726-319">The parent of the resource.</span></span> <span data-ttu-id="46726-320">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-320">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-321">**персистентресерватионссуппортед**</span><span class="sxs-lookup"><span data-stu-id="46726-321">**PersistentReservationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-322">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46726-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46726-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-324">Указывает, поддерживает ли виртуальный жесткий диск постоянные резервирования SCSI-3.</span><span class="sxs-lookup"><span data-stu-id="46726-324">Indicates whether the virtual hard disk supports SCSI-3 persistent reservations.</span></span>

<span data-ttu-id="46726-325">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="46726-325">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="46726-326">**пулид**</span><span class="sxs-lookup"><span data-stu-id="46726-326">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-327">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-329">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="46726-329">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="46726-330">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-330">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-331">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="46726-331">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-332">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46726-332">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46726-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46726-334">Квалификаторы: **override** ("резервирование"), **Моделкорреспонденце** ("CIM \_ сторажеаллокатионсеттингдата. хостресаурцеблокксизе")</span><span class="sxs-lookup"><span data-stu-id="46726-334">Qualifiers: **Override** ("Reservation"), **ModelCorrespondence** ("CIM\_StorageAllocationSettingData.HostResourceBlockSize")</span></span>
</dt> </dl>

<span data-ttu-id="46726-335">Число блоков, которые гарантированно будут доступны для этого выделения ресурсов хранилища на узле.</span><span class="sxs-lookup"><span data-stu-id="46726-335">The number of blocks that are guaranteed to be available for this storage resource allocation at the host.</span></span> <span data-ttu-id="46726-336">Размер блока задается свойством **хостресаурцеблокксизе** .</span><span class="sxs-lookup"><span data-stu-id="46726-336">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="46726-337">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-337">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="46726-338">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="46726-338">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-339">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-341">Строка, описывающая подтип для этого ресурса, зависящий от реализации.</span><span class="sxs-lookup"><span data-stu-id="46726-341">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="46726-342">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46726-342">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="46726-343">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-343">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-344">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="46726-344">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-345">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46726-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46726-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-347">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="46726-347">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="46726-348">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-348">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="46726-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="46726-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="46726-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="46726-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="46726-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="46726-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="46726-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="46726-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="46726-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="46726-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="46726-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="46726-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="46726-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="46726-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="46726-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="46726-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="46726-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="46726-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="46726-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="46726-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="46726-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="46726-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="46726-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="46726-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="46726-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="46726-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="46726-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Флоппи-дисковод** (14)</span><span class="sxs-lookup"><span data-stu-id="46726-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="46726-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="46726-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="46726-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="46726-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="46726-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Диск** (17)</span><span class="sxs-lookup"><span data-stu-id="46726-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="46726-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Ленточный накопитель** (18)</span><span class="sxs-lookup"><span data-stu-id="46726-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="46726-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Область хранения** (19)</span><span class="sxs-lookup"><span data-stu-id="46726-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="46726-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Другое запоминающее устройство** (20)</span><span class="sxs-lookup"><span data-stu-id="46726-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="46726-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (21)</span><span class="sxs-lookup"><span data-stu-id="46726-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="46726-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (22)</span><span class="sxs-lookup"><span data-stu-id="46726-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="46726-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Контроллер USB** (23)</span><span class="sxs-lookup"><span data-stu-id="46726-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="46726-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (24)</span><span class="sxs-lookup"><span data-stu-id="46726-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="46726-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Контроллер IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="46726-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="46726-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="46726-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="46726-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="46726-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="46726-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Источник питания** (28)</span><span class="sxs-lookup"><span data-stu-id="46726-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="46726-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Охлаждающее устройство** (29)</span><span class="sxs-lookup"><span data-stu-id="46726-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="46726-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Порт коммутатора Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="46726-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="46726-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Логический диск** (31)</span><span class="sxs-lookup"><span data-stu-id="46726-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="46726-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Том хранилища** (32)</span><span class="sxs-lookup"><span data-stu-id="46726-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="46726-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-подключение** (33)</span><span class="sxs-lookup"><span data-stu-id="46726-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="46726-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="46726-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="46726-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="46726-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46726-384">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="46726-384">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-385">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-386">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-387">Идентификатор GUID, представляющий моментальный снимок в файле набора виртуальных жестких дисков, который должен быть присоединен.</span><span class="sxs-lookup"><span data-stu-id="46726-387">A GUID representing which snapshot within the VHD Set file is to be attached.</span></span>

> [!Note]  
> <span data-ttu-id="46726-388">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="46726-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="46726-389">**сторажекосполициид**</span><span class="sxs-lookup"><span data-stu-id="46726-389">**StorageQoSPolicyID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-390">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-390">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-392">Указывает уникальный идентификатор политики качества обслуживания хранилища, применяемой к этому экстенту виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="46726-392">Specifies the unique identifier of the Storage QoS Policy to be applied to this virtual storage extent.</span></span>

> [!Note]  
> <span data-ttu-id="46726-393">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="46726-393">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="46726-394">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="46726-394">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-395">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46726-395">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46726-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-397">Число блоков, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="46726-397">The number of blocks that are presented to the consumer.</span></span> <span data-ttu-id="46726-398">Размер блока задается свойством **виртуалресаурцеблокксизе** .</span><span class="sxs-lookup"><span data-stu-id="46726-398">The block size is specified by the **VirtualResourceBlockSize** property.</span></span> <span data-ttu-id="46726-399">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-399">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="46726-400">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="46726-400">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46726-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46726-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-403">Указывает единицы, используемые свойством **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="46726-403">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="46726-404">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-404">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>



| <span data-ttu-id="46726-405">Значение</span><span class="sxs-lookup"><span data-stu-id="46726-405">Value</span></span>                                                                                                | <span data-ttu-id="46726-406">Значение</span><span class="sxs-lookup"><span data-stu-id="46726-406">Meaning</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46726-407"><dt>"Count (блок фиксированного размера)"</dt></span><span class="sxs-lookup"><span data-stu-id="46726-407"><dt>"count(fixed size block)"</dt></span></span> </dl> | <span data-ttu-id="46726-408">Фиксированный размер блока содержится в свойстве **виртуалресаурцеблокксизе** .</span><span class="sxs-lookup"><span data-stu-id="46726-408">The fixed block size is contained in the **VirtualResourceBlockSize** property.</span></span><br/> |
| <dl> <span data-ttu-id="46726-409"><dt>двухбайтовых</dt></span><span class="sxs-lookup"><span data-stu-id="46726-409"><dt>"byte"</dt></span></span> </dl>                    | <span data-ttu-id="46726-410">Свойство **виртуалкуантити** измеряется в байтах.</span><span class="sxs-lookup"><span data-stu-id="46726-410">The **VirtualQuantity** property is measured in bytes.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="46726-411">**виртуалресаурцеблокксизе**</span><span class="sxs-lookup"><span data-stu-id="46726-411">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-412">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="46726-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="46726-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-414">Размер (в байтах) блоков, представленных потребителю в результате этого выделения ресурсов хранилища или запроса на выделение ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="46726-414">The size, in bytes, of the blocks that are presented to the consumer as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="46726-415">Если размер блока является переменным, то будет указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="46726-415">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="46726-416">Если размер блока неизвестен или если не применяется концепция блока, будет использовано значение 1.</span><span class="sxs-lookup"><span data-stu-id="46726-416">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="46726-417">Это свойство наследуется от **CIM \_ сторажеаллокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="46726-417">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="46726-418">**Weight**</span><span class="sxs-lookup"><span data-stu-id="46726-418">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-419">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46726-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46726-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46726-421">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("вес"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span><span class="sxs-lookup"><span data-stu-id="46726-421">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span></span>
</dt> </dl>

<span data-ttu-id="46726-422">Задает относительный приоритет для этого выделения относительно других выделений из того же пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46726-422">Specifies a relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="46726-423">Это свойство не имеет единицы измерения и является релевантным только в том случае, если по сравнению с другими распределениями Винг для тех же ресурсов узла.</span><span class="sxs-lookup"><span data-stu-id="46726-423">This property has no unit of measure and is only relevant when compared to other allocations vying for the same host resources.</span></span> <span data-ttu-id="46726-424">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="46726-424">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="46726-425">Диапазон: 1 10000</span><span class="sxs-lookup"><span data-stu-id="46726-425">Range: 1 10000</span></span>

</dd> <dt>

<span data-ttu-id="46726-426">**вритехарденингмесод**</span><span class="sxs-lookup"><span data-stu-id="46726-426">**WriteHardeningMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46726-427">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46726-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46726-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46726-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46726-429">Указывает, какой метод усиления записи поддерживается диском.</span><span class="sxs-lookup"><span data-stu-id="46726-429">Indicates what write hardening method is supported by the disk.</span></span>

> [!Note]  
> <span data-ttu-id="46726-430">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="46726-430">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="46726-431">**По умолчанию** (0)</span><span class="sxs-lookup"><span data-stu-id="46726-431">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

<span data-ttu-id="46726-432">**Вритекачинаблед** (1)</span><span class="sxs-lookup"><span data-stu-id="46726-432">**WriteCacheEnabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

<span data-ttu-id="46726-433">**Вритекачеандфуаенаблед** (2)</span><span class="sxs-lookup"><span data-stu-id="46726-433">**WriteCacheandFUAEnabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

<span data-ttu-id="46726-434">**Вритекачедисаблед** (3)</span><span class="sxs-lookup"><span data-stu-id="46726-434">**WriteCacheDisabled** (3)</span></span>


<span data-ttu-id="46726-435"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="46726-435"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="46726-436">Требования</span><span class="sxs-lookup"><span data-stu-id="46726-436">Requirements</span></span>



| <span data-ttu-id="46726-437">Требование</span><span class="sxs-lookup"><span data-stu-id="46726-437">Requirement</span></span> | <span data-ttu-id="46726-438">Значение</span><span class="sxs-lookup"><span data-stu-id="46726-438">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46726-439">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46726-439">Minimum supported client</span></span><br/> | <span data-ttu-id="46726-440">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="46726-440">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="46726-441">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46726-441">Minimum supported server</span></span><br/> | <span data-ttu-id="46726-442">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="46726-442">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46726-443">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="46726-443">Namespace</span></span><br/>                | <span data-ttu-id="46726-444">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="46726-444">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46726-445">MOF</span><span class="sxs-lookup"><span data-stu-id="46726-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46726-446"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46726-446"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46726-447">DLL</span><span class="sxs-lookup"><span data-stu-id="46726-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46726-448"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46726-448"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

