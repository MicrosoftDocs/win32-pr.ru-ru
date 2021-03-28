---
description: Класс Хвконфиг \_ логдиск является классом типа событий для событий конфигурации логического диска. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: Класс HWConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546538"
---
# <a name="hwconfig_logdisk-class"></a><span data-ttu-id="2b5f1-104">\_Класс хвконфиг логдиск</span><span class="sxs-lookup"><span data-stu-id="2b5f1-104">HWConfig\_LogDisk class</span></span>

<span data-ttu-id="2b5f1-105">Класс **хвконфиг \_ логдиск** является классом типа событий для событий конфигурации логического диска.</span><span class="sxs-lookup"><span data-stu-id="2b5f1-105">The **HWConfig\_LogDisk** class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="2b5f1-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="2b5f1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b5f1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b5f1-107">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a><span data-ttu-id="2b5f1-108">Участники</span><span class="sxs-lookup"><span data-stu-id="2b5f1-108">Members</span></span>

<span data-ttu-id="2b5f1-109">Класс **хвконфиг \_ логдиск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b5f1-109">The **HWConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="2b5f1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b5f1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b5f1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b5f1-111">Properties</span></span>

<span data-ttu-id="2b5f1-112">Класс **хвконфиг \_ логдиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2b5f1-112">The **HWConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b5f1-113">дискнумбер</span><span class="sxs-lookup"><span data-stu-id="2b5f1-113">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b5f1-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b5f1-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b5f1-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b5f1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b5f1-116">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="2b5f1-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="2b5f1-117">Номер индекса диска, содержащего этот раздел.</span><span class="sxs-lookup"><span data-stu-id="2b5f1-117">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="2b5f1-118">Pad</span><span class="sxs-lookup"><span data-stu-id="2b5f1-118">Pad</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b5f1-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b5f1-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b5f1-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b5f1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b5f1-121">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="2b5f1-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2b5f1-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2b5f1-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2b5f1-123">PartitionSize</span><span class="sxs-lookup"><span data-stu-id="2b5f1-123">PartitionSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b5f1-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b5f1-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b5f1-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b5f1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b5f1-126">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="2b5f1-126">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="2b5f1-127">Общий размер секции в байтах.</span><span class="sxs-lookup"><span data-stu-id="2b5f1-127">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2b5f1-128">стартоффсет</span><span class="sxs-lookup"><span data-stu-id="2b5f1-128">StartOffset</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b5f1-129">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b5f1-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b5f1-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b5f1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b5f1-131">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="2b5f1-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="2b5f1-132">Начальное смещение (в байтах) секции от начала диска.</span><span class="sxs-lookup"><span data-stu-id="2b5f1-132">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b5f1-133">Требования</span><span class="sxs-lookup"><span data-stu-id="2b5f1-133">Requirements</span></span>



| <span data-ttu-id="2b5f1-134">Требование</span><span class="sxs-lookup"><span data-stu-id="2b5f1-134">Requirement</span></span> | <span data-ttu-id="2b5f1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="2b5f1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="2b5f1-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b5f1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2b5f1-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2b5f1-137">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2b5f1-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b5f1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2b5f1-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2b5f1-139">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="2b5f1-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b5f1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b5f1-141">**хвконфиг**</span><span class="sxs-lookup"><span data-stu-id="2b5f1-141">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




