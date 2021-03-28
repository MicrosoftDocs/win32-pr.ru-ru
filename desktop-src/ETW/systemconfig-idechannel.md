---
description: Этот класс является классом типа событий для событий канала IDE. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: Класс SystemConfig_IDEChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541866"
---
# <a name="systemconfig_idechannel-class"></a><span data-ttu-id="5b363-104">\_Класс системконфиг идечаннел</span><span class="sxs-lookup"><span data-stu-id="5b363-104">SystemConfig\_IDEChannel class</span></span>

<span data-ttu-id="5b363-105">Этот класс является классом типа событий для событий канала IDE.</span><span class="sxs-lookup"><span data-stu-id="5b363-105">This class is the event type class for IDE channel events.</span></span>

<span data-ttu-id="5b363-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="5b363-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b363-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b363-107">Syntax</span></span>

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a><span data-ttu-id="5b363-108">Участники</span><span class="sxs-lookup"><span data-stu-id="5b363-108">Members</span></span>

<span data-ttu-id="5b363-109">Класс **системконфиг \_ идечаннел** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5b363-109">The **SystemConfig\_IDEChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="5b363-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b363-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b363-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b363-111">Properties</span></span>

<span data-ttu-id="5b363-112">Класс **системконфиг \_ идечаннел** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5b363-112">The **SystemConfig\_IDEChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b363-113">**девицетимингмоде**</span><span class="sxs-lookup"><span data-stu-id="5b363-113">**DeviceTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b363-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b363-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b363-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b363-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b363-116">Квалификаторы: Вмидатаид (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="5b363-116">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="5b363-117">Режим, в котором может работать интегрированная среда разработки.</span><span class="sxs-lookup"><span data-stu-id="5b363-117">The mode in which the IDE could function.</span></span> <span data-ttu-id="5b363-118">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5b363-118">The following are the possible values:</span></span>

-   <span data-ttu-id="5b363-119">PIO \_ MODE0 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5b363-119">PIO\_MODE0 (0x1)</span></span>
-   <span data-ttu-id="5b363-120">PIO \_ MODE1 (0x2)</span><span class="sxs-lookup"><span data-stu-id="5b363-120">PIO\_MODE1 (0x2)</span></span>
-   <span data-ttu-id="5b363-121">\_MODE2 Pio (0x4)</span><span class="sxs-lookup"><span data-stu-id="5b363-121">PIO\_MODE2 (0x4)</span></span>
-   <span data-ttu-id="5b363-122">PIO \_ MODE3 (0x8)</span><span class="sxs-lookup"><span data-stu-id="5b363-122">PIO\_MODE3 (0x8)</span></span>
-   <span data-ttu-id="5b363-123">PIO \_ MODE4 (0x10)</span><span class="sxs-lookup"><span data-stu-id="5b363-123">PIO\_MODE4 (0x10)</span></span>
-   <span data-ttu-id="5b363-124">СВДМА \_ MODE0 (0x20)</span><span class="sxs-lookup"><span data-stu-id="5b363-124">SWDMA\_MODE0 (0x20)</span></span>
-   <span data-ttu-id="5b363-125">СВДМА \_ MODE1 (0x40)</span><span class="sxs-lookup"><span data-stu-id="5b363-125">SWDMA\_MODE1 (0x40)</span></span>
-   <span data-ttu-id="5b363-126">СВДМА \_ MODE2 (0x80)</span><span class="sxs-lookup"><span data-stu-id="5b363-126">SWDMA\_MODE2 (0x80)</span></span>
-   <span data-ttu-id="5b363-127">МВДМА \_ MODE0 (0x100)</span><span class="sxs-lookup"><span data-stu-id="5b363-127">MWDMA\_MODE0 (0x100)</span></span>
-   <span data-ttu-id="5b363-128">МВДМА \_ MODE2 (0x200)</span><span class="sxs-lookup"><span data-stu-id="5b363-128">MWDMA\_MODE2 (0x200)</span></span>
-   <span data-ttu-id="5b363-129">МВДМА \_ MODE3 (0x400)</span><span class="sxs-lookup"><span data-stu-id="5b363-129">MWDMA\_MODE3 (0x400)</span></span>
-   <span data-ttu-id="5b363-130">UDMA \_ MODE0 (0x800)</span><span class="sxs-lookup"><span data-stu-id="5b363-130">UDMA\_MODE0 (0x800)</span></span>
-   <span data-ttu-id="5b363-131">UDMA \_ MODE1 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="5b363-131">UDMA\_MODE1 (0x1000)</span></span>
-   <span data-ttu-id="5b363-132">UDMA \_ MODE2 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="5b363-132">UDMA\_MODE2 (0x2000)</span></span>
-   <span data-ttu-id="5b363-133">UDMA \_ MODE3 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="5b363-133">UDMA\_MODE3 (0x4000)</span></span>
-   <span data-ttu-id="5b363-134">UDMA \_ MODE4 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="5b363-134">UDMA\_MODE4 (0x8000)</span></span>
-   <span data-ttu-id="5b363-135">UDMA \_ MODE5 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="5b363-135">UDMA\_MODE5 (0x10000)</span></span>

</dd> <dt>

<span data-ttu-id="5b363-136">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="5b363-136">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b363-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b363-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b363-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b363-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b363-139">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="5b363-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="5b363-140">Тип устройства.</span><span class="sxs-lookup"><span data-stu-id="5b363-140">The device type.</span></span> <span data-ttu-id="5b363-141">Допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5b363-141">The following are the possible values:</span></span>

-   <span data-ttu-id="5b363-142">ATA (1)</span><span class="sxs-lookup"><span data-stu-id="5b363-142">ATA (1)</span></span>
-   <span data-ttu-id="5b363-143">ATAPI (2)</span><span class="sxs-lookup"><span data-stu-id="5b363-143">ATAPI (2)</span></span>

</dd> <dt>

<span data-ttu-id="5b363-144">**локатионинформатион**</span><span class="sxs-lookup"><span data-stu-id="5b363-144">**LocationInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b363-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b363-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b363-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b363-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b363-147">Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="5b363-147">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5b363-148">Канал IDE (например, основной канал, дополнительный канал и т. д.).</span><span class="sxs-lookup"><span data-stu-id="5b363-148">The IDE channel (for example, Primary Channel, Secondary Channel, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="5b363-149">**локатионинформатионлен**</span><span class="sxs-lookup"><span data-stu-id="5b363-149">**LocationInformationLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b363-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b363-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b363-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b363-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b363-152">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="5b363-152">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="5b363-153">Длина строки **локатионинформатион** .</span><span class="sxs-lookup"><span data-stu-id="5b363-153">Length of the **LocationInformation** string.</span></span>

</dd> <dt>

<span data-ttu-id="5b363-154">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="5b363-154">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b363-155">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b363-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b363-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b363-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b363-157">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="5b363-157">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="5b363-158">Идентификатор диска.</span><span class="sxs-lookup"><span data-stu-id="5b363-158">The identifier of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b363-159">Требования</span><span class="sxs-lookup"><span data-stu-id="5b363-159">Requirements</span></span>



| <span data-ttu-id="5b363-160">Требование</span><span class="sxs-lookup"><span data-stu-id="5b363-160">Requirement</span></span> | <span data-ttu-id="5b363-161">Значение</span><span class="sxs-lookup"><span data-stu-id="5b363-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5b363-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b363-162">Minimum supported client</span></span><br/> | <span data-ttu-id="5b363-163">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b363-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5b363-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b363-164">Minimum supported server</span></span><br/> | <span data-ttu-id="5b363-165">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b363-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b363-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b363-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b363-167">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="5b363-167">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




