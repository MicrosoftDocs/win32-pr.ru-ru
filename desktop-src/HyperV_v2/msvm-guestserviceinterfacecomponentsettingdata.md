---
description: Представляет настроенное состояние компонента интерфейса гостевой службы.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Класс Msvm_GuestServiceInterfaceComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662241"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a><span data-ttu-id="66886-103">\_Класс мсвм гуестсервицеинтерфацекомпонентсеттингдата</span><span class="sxs-lookup"><span data-stu-id="66886-103">Msvm\_GuestServiceInterfaceComponentSettingData class</span></span>

<span data-ttu-id="66886-104">Представляет настроенное состояние компонента интерфейса гостевой службы.</span><span class="sxs-lookup"><span data-stu-id="66886-104">Represents the configured state of the guest service interface component.</span></span> <span data-ttu-id="66886-105">Этот класс является производным от класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) .</span><span class="sxs-lookup"><span data-stu-id="66886-105">This class derives from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class.</span></span>

<span data-ttu-id="66886-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="66886-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66886-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66886-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a><span data-ttu-id="66886-108">Члены</span><span class="sxs-lookup"><span data-stu-id="66886-108">Members</span></span>

<span data-ttu-id="66886-109">Класс **мсвм \_ гуестсервицеинтерфацекомпонентсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="66886-109">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="66886-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="66886-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66886-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="66886-111">Properties</span></span>

<span data-ttu-id="66886-112">Класс **мсвм \_ гуестсервицеинтерфацекомпонентсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="66886-112">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66886-113">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="66886-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66886-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66886-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-116">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="66886-116">The address of the resource.</span></span> <span data-ttu-id="66886-117">Например, MAC-адрес порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="66886-117">For example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="66886-118">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="66886-118">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66886-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66886-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-121">Это свойство задает единицы распределения, используемые свойствами резервирования и ограничения.</span><span class="sxs-lookup"><span data-stu-id="66886-121">This property specifies the units of allocation used by the Reservation and Limit properties.</span></span> <span data-ttu-id="66886-122">Например, если ResourceType = Processor, Аллокатионунитс может иметь значение МГц.</span><span class="sxs-lookup"><span data-stu-id="66886-122">For example, when ResourceType=Processor, AllocationUnits may be set to MHz.</span></span> <span data-ttu-id="66886-123">Если ResourceType = Memory, Аллокатионунитс может иметь значение МБ</span><span class="sxs-lookup"><span data-stu-id="66886-123">When ResourceType=Memory, AllocationUnits may be set to MB</span></span>

</dd> <dt>

<span data-ttu-id="66886-124">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="66886-124">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-125">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="66886-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66886-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-127">Это свойство указывает, будет ли ресурс автоматически выделяться.</span><span class="sxs-lookup"><span data-stu-id="66886-127">This property specifies if the resource will be automatically allocated.</span></span> <span data-ttu-id="66886-128">Например, если задано значение true, то при включении виртуальной вычислительной системы этот ресурс будет выделен.</span><span class="sxs-lookup"><span data-stu-id="66886-128">For example when set to true, when the consuming virtual computer system is powered on, this resource would be allocated.</span></span> <span data-ttu-id="66886-129">Значение false указывает, что ресурс должен быть явно выделен.</span><span class="sxs-lookup"><span data-stu-id="66886-129">A value of false indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="66886-130">Например, параметр может представлять съемные носители (т. е. устройство CDROM или дискеты), где во время электропитания отсутствует носитель.</span><span class="sxs-lookup"><span data-stu-id="66886-130">For example, the setting may represent removable media (that is, cdrom or floppy) where at power on time, the media is not present.</span></span> <span data-ttu-id="66886-131">Для выделения ресурса требуется явная операция.</span><span class="sxs-lookup"><span data-stu-id="66886-131">An explicit operation is required to allocate the resource.</span></span>

</dd> <dt>

<span data-ttu-id="66886-132">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="66886-132">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="66886-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66886-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-135">Это свойство указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="66886-135">This property specifies if the resource will be automatically deallocated.</span></span> <span data-ttu-id="66886-136">Например, если задано значение true, то при отключении использования виртуальной системы компьютера этот ресурс будет освобожден.</span><span class="sxs-lookup"><span data-stu-id="66886-136">For example, when set to true, when the consuming virtual computer system is powered off, this resource would be deallocated.</span></span> <span data-ttu-id="66886-137">Если задано значение false, ресурс останется выделенным и должен быть освобожден явным образом.</span><span class="sxs-lookup"><span data-stu-id="66886-137">When set to false, the resource will remain allocated and must be explicitly deallocated.</span></span>

</dd> <dt>

<span data-ttu-id="66886-138">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="66886-138">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-139">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="66886-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="66886-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-141">Объект, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="66886-141">The thing to which this resource is connected.</span></span> <span data-ttu-id="66886-142">Например, именованная сеть или порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="66886-142">For example, a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="66886-143">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="66886-143">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66886-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66886-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-146">Описывает видимость пользователей для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="66886-146">Describes the consumers visibility to the allocated resource.</span></span>



| <span data-ttu-id="66886-147">Значение</span><span class="sxs-lookup"><span data-stu-id="66886-147">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="66886-148">Значение</span><span class="sxs-lookup"><span data-stu-id="66886-148">Meaning</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="66886-149"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66886-149"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                            | <span data-ttu-id="66886-150">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="66886-150">Unknown.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <span data-ttu-id="66886-151"><dt>**Передано**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="66886-151"><dt>**Passed-Through**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="66886-152">Базовый ресурс или ресурсы узла используются и передаются потребителю, возможно, с помощью секционирования.</span><span class="sxs-lookup"><span data-stu-id="66886-152">The underlying or host resource is utilized and passed through to the consumer, possibly using partitioning.</span></span> <span data-ttu-id="66886-153">В свойстве DeviceID должен присутствовать хотя бы один элемент.</span><span class="sxs-lookup"><span data-stu-id="66886-153">At least one item shall be present in the DeviceID property.</span></span><br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <span data-ttu-id="66886-154"><dt>**Виртуализированный**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="66886-154"><dt>**Virtualized**</dt> <dt>3</dt></span></span> </dl>                            | <span data-ttu-id="66886-155">Ресурс является виртуализированным и может не сопоставляться напрямую с базовым ресурсом или узлом узла.</span><span class="sxs-lookup"><span data-stu-id="66886-155">The resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="66886-156">Некоторые реализации могут поддерживать определенное назначение виртуализованных ресурсов. в этом случае ресурсы узла предоставляются с помощью свойства DeviceID.</span><span class="sxs-lookup"><span data-stu-id="66886-156">Some implementations may support specific assignment for virtualized resources, in which case the host resource(s) are exposed using the DeviceID property.</span></span><br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <span data-ttu-id="66886-157"><dt>**Не представлено**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="66886-157"><dt>**Not represented**</dt> <dt>4</dt></span></span> </dl>            | <span data-ttu-id="66886-158">Представление ресурса не существует в контексте потребителя ресурса.</span><span class="sxs-lookup"><span data-stu-id="66886-158">A representation of the resource does not exist within the context of the resource consumer.</span></span><br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="66886-159"><dt>**Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="66886-159"><dt>**DMTF reserved**</dt> <dt>..</dt></span></span> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="66886-160"><dt>**Зарезервировано поставщиком**</dt> <dt>32767.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="66886-160"><dt>**Vendor Reserved**</dt> <dt>32767..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="66886-161">**дефаултенабледстатеполици**</span><span class="sxs-lookup"><span data-stu-id="66886-161">**DefaultEnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-162">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66886-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66886-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-164">Включенные и отключенные состояния служб гостевой связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66886-164">The enabled and disabled states of guest communication services by default.</span></span>

<span data-ttu-id="66886-165">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="66886-165">This is a read-only property, but it can be changed using the [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="66886-166">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="66886-166">Added in Windows 10.</span></span>

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="66886-167">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="66886-167">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="66886-168">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="66886-168">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66886-169">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="66886-169">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66886-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66886-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-172">Отображаемое имя для этого экземпляра SettingData.</span><span class="sxs-lookup"><span data-stu-id="66886-172">The display name for this instance of SettingData.</span></span> <span data-ttu-id="66886-173">Кроме того, отображаемое имя можно использовать в качестве свойства индекса для поиска или запроса.</span><span class="sxs-lookup"><span data-stu-id="66886-173">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="66886-174">(Примечание. имя не обязательно должно быть уникальным в пределах пространства имен.)</span><span class="sxs-lookup"><span data-stu-id="66886-174">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="66886-175">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="66886-175">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-176">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66886-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66886-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-178">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="66886-178">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="66886-179">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифивиртуалсистемресаурцес**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (или [**модифиресаурцесеттингс**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) в Windows 10 или более поздней версии) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="66886-179">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method (or [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 or later) of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="66886-180">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="66886-180">Valid values are:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="66886-181">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="66886-181">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="66886-182">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="66886-182">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66886-183">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="66886-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-184">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="66886-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="66886-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-186">Это свойство предоставляет определенное назначение для размещения или базовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66886-186">This property exposes specific assignment to host or underlying resources.</span></span> <span data-ttu-id="66886-187">Внедренные экземпляры должны содержать только ключевые свойства и рассматриваться как пути к объектам.</span><span class="sxs-lookup"><span data-stu-id="66886-187">The embedded instances shall contain only key properties and be treated as Object Paths.</span></span> <span data-ttu-id="66886-188">Если виртуальный ресурс может быть запланирован на несколько базовых ресурсов, это свойство должно оставаться **равным NULL**.</span><span class="sxs-lookup"><span data-stu-id="66886-188">If the virtual resource may be scheduled on a number of underlying resources, this property should remain **NULL**.</span></span> <span data-ttu-id="66886-189">В этом случае можно использовать ассоциации Девицеаллокатедфромпул или Ресаурцеаллокатионфромпул, чтобы определить пул ресурсов узла, на котором может быть запланирован этот виртуальный ресурс.</span><span class="sxs-lookup"><span data-stu-id="66886-189">In that case, the DeviceAllocatedFromPool or ResourceAllocationFromPool associations may be used to determine the pool of host resources on which this virtual resource may be scheduled.</span></span> <span data-ttu-id="66886-190">Если используется конкретное назначение, все базовые ресурсы, используемые этим виртуальным ресурсом, должны быть перечислены в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="66886-190">If specific assignment is utilized, all underlying resources used by this virtual resource shall be listed in this array.</span></span> <span data-ttu-id="66886-191">Как правило, массив будет содержать один элемент, однако для агрегатных распределений, таких как несколько процессоров, можно указать несколько ресурсов узла.</span><span class="sxs-lookup"><span data-stu-id="66886-191">Typically, the array will contain one item, however for aggregate allocations, such as multiple processors, multiple host resources may be specified.</span></span>

</dd> <dt>

<span data-ttu-id="66886-192">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="66886-192">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66886-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66886-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66886-195">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="66886-195">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="66886-196">В пределах области создания экземпляра пространства имен InstanceID непрозрачно и уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="66886-196">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="66886-197">Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма: *OrgID*:*LocalId* , где *OrgID* и *LocalID* разделяются двоеточием (:), и там, где *OrgID* необходимо включать уникальное имя, которое принадлежит бизнес-сущности, которая создает или определяет InstanceId или является зарегистрированным идентификатором, назначенным бизнес-сущности в известном Глобальном центре сертификации.</span><span class="sxs-lookup"><span data-stu-id="66886-197">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="66886-198">(Это требование похоже на объект *SchemaName* \_ . Структура *className* имен классов схемы.) Кроме того, чтобы обеспечить уникальность, *OrgID* не должен содержать двоеточия (:).</span><span class="sxs-lookup"><span data-stu-id="66886-198">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="66886-199">При использовании этого алгоритма первое двоеточие должно появиться в идентификаторе InstanceID между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="66886-199">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="66886-200">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов.</span><span class="sxs-lookup"><span data-stu-id="66886-200">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="66886-201">Если приведенный выше "предпочтительный" алгоритм не используется, определяющая сущность должна гарантировать, что полученный идентификатор InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="66886-201">If the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="66886-202">Для экземпляров, определяемых DMTF, необходимо использовать "предпочтительный" алгоритм с *OrgID* , для которого задано значение CIM.</span><span class="sxs-lookup"><span data-stu-id="66886-202">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="66886-203">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="66886-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-204">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66886-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66886-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-206">Это свойство задает верхнюю границу или максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="66886-206">This property specifies the upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="66886-207">Например, система, поддерживающая подкачку памяти, может поддерживать установку ограничения выделения памяти ниже, чем Виртуалкуантити, таким образом принудительное разбиение на страницы для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="66886-207">For example, a system which supports memory paging may support setting the Limit of a Memory allocation below that of the VirtualQuantity, thus forcing paging to occur for this allocation.</span></span>

</dd> <dt>

<span data-ttu-id="66886-208">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="66886-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-209">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66886-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66886-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-211">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="66886-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="66886-212">Если массив Хостресаурце содержит какие бы то ни было записи, это свойство отражает, как ресурс сопоставляется с этими конкретными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="66886-212">If the HostResource array contains any entries, this property reflects how the resource maps to those specific resources.</span></span>

<dl> <dt>

<span data-ttu-id="66886-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="66886-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="66886-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="66886-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="66886-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (2)</span><span class="sxs-lookup"><span data-stu-id="66886-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66886-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Мягкое сходство** (3)</span><span class="sxs-lookup"><span data-stu-id="66886-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (3)</span></span>
</dt> <dt>

<span data-ttu-id="66886-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Жесткое сходство** (4)</span><span class="sxs-lookup"><span data-stu-id="66886-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="66886-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="66886-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="66886-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="66886-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="66886-220">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="66886-220">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66886-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66886-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-223">Строка, описывающая тип ресурса, когда хорошо определенное значение недоступно, а ResourceType имеет значение other.</span><span class="sxs-lookup"><span data-stu-id="66886-223">A string that describes the resource type when a well defined value is not available and ResourceType has the value "Other".</span></span>

</dd> <dt>

<span data-ttu-id="66886-224">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="66886-224">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66886-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66886-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-227">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="66886-227">The Parent of the resource.</span></span> <span data-ttu-id="66886-228">Например, контроллер для текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="66886-228">For example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="66886-229">**пулид**</span><span class="sxs-lookup"><span data-stu-id="66886-229">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66886-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66886-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-232">Это свойство указывает, какой ResourcePool ресурс в данный момент выделяется из, или что ResourcePool ресурс будет выделен при выделении.</span><span class="sxs-lookup"><span data-stu-id="66886-232">This property specifies which ResourcePool the resource is currently allocated from, or which ResourcePool the resource will be allocated from when the allocation occurs.</span></span>

</dd> <dt>

<span data-ttu-id="66886-233">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="66886-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-234">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66886-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66886-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-236">Это свойство определяет объем ресурса, который должен быть доступен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="66886-236">This property specifies the amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="66886-237">В системе, которая поддерживает чрезмерное использование ресурсов, это значение обычно используется для управления допуском, чтобы предотвратить принятие выделения, что препятствует исчерпанию ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66886-237">On system which support over-commitment of resources, this value is typically used for admission control to prevent an an allocation from being accepted thus preventing resource depletion.</span></span>

</dd> <dt>

<span data-ttu-id="66886-238">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="66886-238">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-239">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66886-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66886-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-241">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="66886-241">A string describing an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="66886-242">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66886-242">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="66886-243">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="66886-243">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-244">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66886-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66886-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-246">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="66886-246">The type of resource this allocation setting represents.</span></span>

<dl> <dt>

<span data-ttu-id="66886-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66886-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="66886-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="66886-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66886-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="66886-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="66886-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="66886-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="66886-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="66886-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="66886-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="66886-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="66886-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="66886-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="66886-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="66886-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="66886-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="66886-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="66886-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="66886-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="66886-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="66886-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="66886-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="66886-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="66886-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="66886-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="66886-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="66886-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="66886-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="66886-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="66886-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="66886-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="66886-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (17)</span><span class="sxs-lookup"><span data-stu-id="66886-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="66886-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (18)</span><span class="sxs-lookup"><span data-stu-id="66886-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="66886-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-контроллер** (19)</span><span class="sxs-lookup"><span data-stu-id="66886-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="66886-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (20)</span><span class="sxs-lookup"><span data-stu-id="66886-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="66886-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Область хранения** (21)</span><span class="sxs-lookup"><span data-stu-id="66886-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="66886-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Диск** (22)</span><span class="sxs-lookup"><span data-stu-id="66886-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="66886-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Лента** (23)</span><span class="sxs-lookup"><span data-stu-id="66886-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="66886-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Другое запоминающее устройство** (24)</span><span class="sxs-lookup"><span data-stu-id="66886-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="66886-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Контроллер FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="66886-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="66886-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="66886-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="66886-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="66886-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="66886-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Источник питания** (28)</span><span class="sxs-lookup"><span data-stu-id="66886-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="66886-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Охлаждающее устройство** (29)</span><span class="sxs-lookup"><span data-stu-id="66886-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="66886-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="66886-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="66886-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="66886-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="66886-278">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="66886-278">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-279">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66886-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66886-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-281">Это свойство указывает количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="66886-281">This property specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="66886-282">Например, если ResourceType = Processor, это свойство будет отражать количество дискретных процессоров, представленных в системе виртуального компьютера.</span><span class="sxs-lookup"><span data-stu-id="66886-282">For example, when ResourceType=Processor, this property would reflect the number of discrete Processors presented to the virtual computer system.</span></span> <span data-ttu-id="66886-283">Если ResourceType = Memory, это свойство может отражать число МБ, переданных в систему виртуального компьютера.</span><span class="sxs-lookup"><span data-stu-id="66886-283">When ResourceType=Memory, this property could reflect the number of MB reported to the virtual computer system.</span></span>

</dd> <dt>

<span data-ttu-id="66886-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="66886-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66886-285">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66886-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66886-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66886-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66886-287">Это свойство задает относительный приоритет для этого выделения относительно других выделений из того же ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="66886-287">This property specifies a relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="66886-288">Это свойство не имеет единицы измерения и имеет смысл только в сравнении с другими выделениями, конкурирующими за те же ресурсы узла.</span><span class="sxs-lookup"><span data-stu-id="66886-288">This property has no unit of measure, and is only relevant when compared to other allocations competing for the same host resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66886-289">Требования</span><span class="sxs-lookup"><span data-stu-id="66886-289">Requirements</span></span>



| <span data-ttu-id="66886-290">Требование</span><span class="sxs-lookup"><span data-stu-id="66886-290">Requirement</span></span> | <span data-ttu-id="66886-291">Значение</span><span class="sxs-lookup"><span data-stu-id="66886-291">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66886-292">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66886-292">Minimum supported client</span></span><br/> | <span data-ttu-id="66886-293">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66886-293">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="66886-294">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66886-294">Minimum supported server</span></span><br/> | <span data-ttu-id="66886-295">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="66886-295">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="66886-296">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="66886-296">Namespace</span></span><br/>                | <span data-ttu-id="66886-297">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="66886-297">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="66886-298">MOF</span><span class="sxs-lookup"><span data-stu-id="66886-298">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66886-299"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66886-299"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66886-300">DLL</span><span class="sxs-lookup"><span data-stu-id="66886-300">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66886-301"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66886-301"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="66886-302">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66886-302">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66886-303">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="66886-303">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="66886-304">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="66886-304">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

