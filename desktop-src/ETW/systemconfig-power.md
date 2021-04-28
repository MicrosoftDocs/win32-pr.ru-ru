---
description: SystemConfig_Power класс. Этот класс является классом типа событий для событий конфигурации питания. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: Класс SystemConfig_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7338faad8c313847ad7db7aaac5d4000abba5be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106072"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="c782a-104">\_Класс питания системконфиг</span><span class="sxs-lookup"><span data-stu-id="c782a-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="c782a-105">Этот класс является классом типа событий для событий конфигурации питания.</span><span class="sxs-lookup"><span data-stu-id="c782a-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="c782a-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="c782a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c782a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c782a-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="c782a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c782a-108">Members</span></span>

<span data-ttu-id="c782a-109">Класс **\_ питания системконфиг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c782a-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="c782a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c782a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c782a-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="c782a-111">Properties</span></span>

<span data-ttu-id="c782a-112">Класс **\_ питания системконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c782a-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c782a-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="c782a-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c782a-114">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c782a-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c782a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c782a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c782a-116">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="c782a-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="c782a-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c782a-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c782a-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="c782a-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c782a-119">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c782a-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c782a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c782a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c782a-121">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="c782a-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="c782a-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c782a-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c782a-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="c782a-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c782a-124">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c782a-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c782a-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c782a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c782a-126">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="c782a-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="c782a-127">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c782a-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c782a-128">s1</span><span class="sxs-lookup"><span data-stu-id="c782a-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c782a-129">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c782a-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c782a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c782a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c782a-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="c782a-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c782a-132">Значение true указывает, что система поддерживает состояние сна S1.</span><span class="sxs-lookup"><span data-stu-id="c782a-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="c782a-133">s2</span><span class="sxs-lookup"><span data-stu-id="c782a-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c782a-134">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c782a-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c782a-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c782a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c782a-136">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="c782a-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c782a-137">Значение true указывает, что система поддерживает состояние сна S2.</span><span class="sxs-lookup"><span data-stu-id="c782a-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="c782a-138">s3</span><span class="sxs-lookup"><span data-stu-id="c782a-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c782a-139">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c782a-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c782a-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c782a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c782a-141">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="c782a-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="c782a-142">Значение true указывает, что система поддерживает состояние сна S3.</span><span class="sxs-lookup"><span data-stu-id="c782a-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="c782a-143">S4</span><span class="sxs-lookup"><span data-stu-id="c782a-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c782a-144">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c782a-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c782a-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c782a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c782a-146">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="c782a-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c782a-147">Значение true указывает, что система поддерживает состояние сна S4.</span><span class="sxs-lookup"><span data-stu-id="c782a-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="c782a-148">остановки</span><span class="sxs-lookup"><span data-stu-id="c782a-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c782a-149">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c782a-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c782a-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c782a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c782a-151">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="c782a-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="c782a-152">Значение true указывает, что система поддерживает состояние сна S5.</span><span class="sxs-lookup"><span data-stu-id="c782a-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c782a-153">Требования</span><span class="sxs-lookup"><span data-stu-id="c782a-153">Requirements</span></span>



| <span data-ttu-id="c782a-154">Требование</span><span class="sxs-lookup"><span data-stu-id="c782a-154">Requirement</span></span> | <span data-ttu-id="c782a-155">Значение</span><span class="sxs-lookup"><span data-stu-id="c782a-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c782a-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c782a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="c782a-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c782a-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c782a-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c782a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="c782a-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c782a-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c782a-160">См. также</span><span class="sxs-lookup"><span data-stu-id="c782a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c782a-161">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="c782a-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




