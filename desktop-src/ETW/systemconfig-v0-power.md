---
description: SystemConfig_V0_Power класс. Этот класс является классом типа событий для событий конфигурации питания. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: Класс SystemConfig_V0_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab268e719374906e149dc9c1b733487f986e8308
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105942"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="db072-104">\_ \_ Класс питания системконфиг v0</span><span class="sxs-lookup"><span data-stu-id="db072-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="db072-105">Этот класс является классом типа событий для событий конфигурации питания.</span><span class="sxs-lookup"><span data-stu-id="db072-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="db072-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="db072-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="db072-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db072-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a><span data-ttu-id="db072-108">Члены</span><span class="sxs-lookup"><span data-stu-id="db072-108">Members</span></span>

<span data-ttu-id="db072-109">Класс **\_ \_ питания системконфиг v0** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="db072-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="db072-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="db072-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db072-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="db072-111">Properties</span></span>

<span data-ttu-id="db072-112">Класс **\_ \_ питания системконфиг v0** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="db072-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db072-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="db072-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db072-114">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="db072-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="db072-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db072-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db072-116">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="db072-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="db072-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="db072-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="db072-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="db072-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db072-119">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="db072-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="db072-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db072-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db072-121">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="db072-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="db072-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="db072-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="db072-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="db072-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db072-124">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="db072-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="db072-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db072-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db072-126">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="db072-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="db072-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="db072-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="db072-128">s1</span><span class="sxs-lookup"><span data-stu-id="db072-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db072-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="db072-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db072-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db072-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db072-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="db072-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="db072-132">Значение true указывает, что система поддерживает состояние сна S1.</span><span class="sxs-lookup"><span data-stu-id="db072-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="db072-133">s2</span><span class="sxs-lookup"><span data-stu-id="db072-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db072-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="db072-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db072-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db072-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db072-136">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="db072-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="db072-137">Значение true указывает, что система поддерживает состояние сна S2.</span><span class="sxs-lookup"><span data-stu-id="db072-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="db072-138">s3</span><span class="sxs-lookup"><span data-stu-id="db072-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db072-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="db072-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db072-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db072-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db072-141">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="db072-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="db072-142">Значение true указывает, что система поддерживает состояние сна S3.</span><span class="sxs-lookup"><span data-stu-id="db072-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="db072-143">S4</span><span class="sxs-lookup"><span data-stu-id="db072-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db072-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="db072-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db072-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db072-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db072-146">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="db072-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="db072-147">Значение true указывает, что система поддерживает состояние сна S4.</span><span class="sxs-lookup"><span data-stu-id="db072-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="db072-148">остановки</span><span class="sxs-lookup"><span data-stu-id="db072-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db072-149">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="db072-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db072-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db072-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db072-151">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="db072-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="db072-152">Значение true указывает, что система поддерживает состояние сна S5.</span><span class="sxs-lookup"><span data-stu-id="db072-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db072-153">Требования</span><span class="sxs-lookup"><span data-stu-id="db072-153">Requirements</span></span>



| <span data-ttu-id="db072-154">Требование</span><span class="sxs-lookup"><span data-stu-id="db072-154">Requirement</span></span> | <span data-ttu-id="db072-155">Значение</span><span class="sxs-lookup"><span data-stu-id="db072-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db072-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db072-156">Minimum supported client</span></span><br/> | <span data-ttu-id="db072-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="db072-157">None supported</span></span><br/>                            |
| <span data-ttu-id="db072-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db072-158">Minimum supported server</span></span><br/> | <span data-ttu-id="db072-159">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db072-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db072-160">См. также</span><span class="sxs-lookup"><span data-stu-id="db072-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db072-161">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="db072-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




