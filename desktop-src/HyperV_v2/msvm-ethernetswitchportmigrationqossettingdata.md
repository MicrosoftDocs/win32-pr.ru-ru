---
description: Представляет параметры качества обслуживания VFP.
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Класс Msvm_EthernetSwitchPortMigrationQosSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e279b24178c33c760477995ff744a0699cea1aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683687"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a><span data-ttu-id="fcb3a-103">\_Класс мсвм есернетсвитчпортмигратионкоссеттингдата</span><span class="sxs-lookup"><span data-stu-id="fcb3a-103">Msvm\_EthernetSwitchPortMigrationQosSettingData class</span></span>

<span data-ttu-id="fcb3a-104">Представляет параметры качества обслуживания VFP.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-104">Represents the VFP QOS settings.</span></span>

<span data-ttu-id="fcb3a-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb3a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcb3a-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a><span data-ttu-id="fcb3a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fcb3a-107">Members</span></span>

<span data-ttu-id="fcb3a-108">Класс **мсвм \_ есернетсвитчпортмигратионкоссеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fcb3a-108">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fcb3a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="fcb3a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcb3a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fcb3a-110">Properties</span></span>

<span data-ttu-id="fcb3a-111">Класс **мсвм \_ есернетсвитчпортмигратионкоссеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-111">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcb3a-112">**инбаундмаксимуммбпс**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-112">**InboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-113">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-115">Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-115">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-116">Значение ограничения пропускной способности для входящего трафика.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-116">The bandwidth cap value for inbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-117">**аутбаундмаксимуммбпс**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-117">**OutboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-118">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-120">Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-120">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-121">Значение ограничения пропускной способности для исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-121">The bandwidth cap value for outbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-122">**аутбаундресерведвалуе**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-122">**OutboundReservedValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-123">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-125">Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-125">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-126">Значение резервирования пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-126">The bandwidth reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-127">**куеуеид**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-127">**QueueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-130">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **вмидатаид** (1), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-131">Идентификатор очереди QOS.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-131">The ID of the QOS queue.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-132">**Переключить \_ дефаултресерватион**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-132">**Switch\_DefaultReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-133">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-135">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-135">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-136">Значение резервирования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-136">The default reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-137">**Переключить \_ енаблехардварелимитс**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-137">**Switch\_EnableHardwareLimits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-140">Квалификаторы: **вмидатаид** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-140">Qualifiers: **WmiDataId** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-141">Указывает, предпринимались ли попытки аппаратной разгрузки для ограничений, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-141">Indicates whether hardware offloads for limits are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-142">**Переключить \_ енаблехардварересерватионс**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-142">**Switch\_EnableHardwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-145">Квалификаторы: **вмидатаид** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-145">Qualifiers: **WmiDataId** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-146">Указывает, предпринимается ли повторная разгрузка оборудования для резервирования, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-146">Indicates whether hardware offloads for reservations are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-147">**Переключить \_ енаблесофтварересерватионс**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-147">**Switch\_EnableSoftwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-150">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-150">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-151">Указывает, доступно ли резервирование на основе программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-151">Indicates whether software based reservation is available.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-152">**Переключить \_ линкспидперцентаже**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-152">**Switch\_LinkSpeedPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-153">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-155">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-155">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-156">Скорость связи в процентах, используемая для резервирования.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-156">The link speed percentage to be used for reservation.</span></span>

</dd> <dt>

<span data-ttu-id="fcb3a-157">**Переключить \_ ресерватионмоде**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-157">**Switch\_ReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb3a-158">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-158">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcb3a-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcb3a-160">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fcb3a-161">Режим резервирования QOS на коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="fcb3a-161">The QOS reservation mode on the switch.</span></span>

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="fcb3a-162">**Absolute** (0)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-162">**Absolute** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="fcb3a-163">**Вес** (1)</span><span class="sxs-lookup"><span data-stu-id="fcb3a-163">**Weight** (1)</span></span>


<span data-ttu-id="fcb3a-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fcb3a-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fcb3a-165">Требования</span><span class="sxs-lookup"><span data-stu-id="fcb3a-165">Requirements</span></span>



| <span data-ttu-id="fcb3a-166">Требование</span><span class="sxs-lookup"><span data-stu-id="fcb3a-166">Requirement</span></span> | <span data-ttu-id="fcb3a-167">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb3a-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb3a-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcb3a-168">Minimum supported client</span></span><br/> | <span data-ttu-id="fcb3a-169">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="fcb3a-169">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fcb3a-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcb3a-170">Minimum supported server</span></span><br/> | <span data-ttu-id="fcb3a-171">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fcb3a-171">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fcb3a-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fcb3a-172">Namespace</span></span><br/>                | <span data-ttu-id="fcb3a-173">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fcb3a-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fcb3a-174">MOF</span><span class="sxs-lookup"><span data-stu-id="fcb3a-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcb3a-175"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcb3a-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcb3a-176">DLL</span><span class="sxs-lookup"><span data-stu-id="fcb3a-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcb3a-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fcb3a-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fcb3a-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcb3a-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb3a-179">**Мсвм \_ есернетсвитчпортфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="fcb3a-179">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

