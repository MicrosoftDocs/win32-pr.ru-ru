---
description: Этот класс является классом типа событий для событий запросов на прерывание (IRQ). Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: Класс SystemConfig_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984456"
---
# <a name="systemconfig_irq-class"></a><span data-ttu-id="ba767-104">\_Класс системконфиг IRQ</span><span class="sxs-lookup"><span data-stu-id="ba767-104">SystemConfig\_IRQ class</span></span>

<span data-ttu-id="ba767-105">Этот класс является классом типа событий для событий запросов на прерывание (IRQ).</span><span class="sxs-lookup"><span data-stu-id="ba767-105">This class is the event type class for interrupt request (IRQ) events.</span></span>

<span data-ttu-id="ba767-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="ba767-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba767-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba767-107">Syntax</span></span>

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a><span data-ttu-id="ba767-108">Участники</span><span class="sxs-lookup"><span data-stu-id="ba767-108">Members</span></span>

<span data-ttu-id="ba767-109">Класс **системконфиг \_ IRQ** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ba767-109">The **SystemConfig\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="ba767-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba767-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba767-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba767-111">Properties</span></span>

<span data-ttu-id="ba767-112">Класс **системконфиг \_ IRQ** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="ba767-112">The **SystemConfig\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba767-113">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="ba767-113">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba767-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ba767-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba767-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba767-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba767-116">Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="ba767-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="ba767-117">Описание устройства или программного обеспечения, выполняющего запрос.</span><span class="sxs-lookup"><span data-stu-id="ba767-117">Description of the device or software making the request.</span></span>

</dd> <dt>

<span data-ttu-id="ba767-118">**девицедескриптионлен**</span><span class="sxs-lookup"><span data-stu-id="ba767-118">**DeviceDescriptionLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba767-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba767-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba767-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba767-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba767-121">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="ba767-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ba767-122">Длина строки в **DeviceDescription** в символах.</span><span class="sxs-lookup"><span data-stu-id="ba767-122">Length, in characters, of the string in **DeviceDescription**.</span></span>

</dd> <dt>

<span data-ttu-id="ba767-123">**иркаффинити**</span><span class="sxs-lookup"><span data-stu-id="ba767-123">**IRQAffinity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba767-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ba767-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ba767-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba767-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba767-126">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="ba767-126">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="ba767-127">Маска сходства IRQ.</span><span class="sxs-lookup"><span data-stu-id="ba767-127">IRQ affinity mask.</span></span> <span data-ttu-id="ba767-128">Маска сходства определяет конкретные процессоры (или группы процессоров), которые могут получить IRQ.</span><span class="sxs-lookup"><span data-stu-id="ba767-128">The affinity mask identifies the specific processors (or groups of processors) that can receive the IRQ.</span></span>

</dd> <dt>

<span data-ttu-id="ba767-129">**иркнум**</span><span class="sxs-lookup"><span data-stu-id="ba767-129">**IRQNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba767-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba767-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba767-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba767-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba767-132">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="ba767-132">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="ba767-133">Номер строки запроса на прерывание.</span><span class="sxs-lookup"><span data-stu-id="ba767-133">Interrupt request line number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba767-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ba767-134">Requirements</span></span>



| <span data-ttu-id="ba767-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ba767-135">Requirement</span></span> | <span data-ttu-id="ba767-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ba767-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba767-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba767-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ba767-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba767-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba767-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba767-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ba767-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba767-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba767-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba767-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba767-142">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="ba767-142">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




