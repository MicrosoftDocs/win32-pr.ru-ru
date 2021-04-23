---
description: Этот класс является классом типа событий для событий конфигурации питания. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: 2e42af68ad12857d65d776b7a73794d2d13b2b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984393"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="0166b-104">\_ \_ Класс питания системконфиг v0</span><span class="sxs-lookup"><span data-stu-id="0166b-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="0166b-105">Этот класс является классом типа событий для событий конфигурации питания.</span><span class="sxs-lookup"><span data-stu-id="0166b-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="0166b-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="0166b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0166b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0166b-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="0166b-108">Участники</span><span class="sxs-lookup"><span data-stu-id="0166b-108">Members</span></span>

<span data-ttu-id="0166b-109">Класс **\_ \_ питания системконфиг v0** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0166b-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="0166b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0166b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0166b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0166b-111">Properties</span></span>

<span data-ttu-id="0166b-112">Класс **\_ \_ питания системконфиг v0** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0166b-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0166b-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="0166b-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0166b-114">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0166b-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0166b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0166b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0166b-116">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="0166b-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="0166b-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="0166b-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0166b-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="0166b-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0166b-119">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0166b-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0166b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0166b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0166b-121">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="0166b-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="0166b-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="0166b-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0166b-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="0166b-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0166b-124">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0166b-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0166b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0166b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0166b-126">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="0166b-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="0166b-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="0166b-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0166b-128">s1</span><span class="sxs-lookup"><span data-stu-id="0166b-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0166b-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0166b-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0166b-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0166b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0166b-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="0166b-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="0166b-132">Значение true указывает, что система поддерживает состояние сна S1.</span><span class="sxs-lookup"><span data-stu-id="0166b-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="0166b-133">s2</span><span class="sxs-lookup"><span data-stu-id="0166b-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0166b-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0166b-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0166b-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0166b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0166b-136">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="0166b-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="0166b-137">Значение true указывает, что система поддерживает состояние сна S2.</span><span class="sxs-lookup"><span data-stu-id="0166b-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="0166b-138">s3</span><span class="sxs-lookup"><span data-stu-id="0166b-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0166b-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0166b-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0166b-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0166b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0166b-141">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="0166b-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0166b-142">Значение true указывает, что система поддерживает состояние сна S3.</span><span class="sxs-lookup"><span data-stu-id="0166b-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="0166b-143">S4</span><span class="sxs-lookup"><span data-stu-id="0166b-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0166b-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0166b-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0166b-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0166b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0166b-146">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="0166b-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="0166b-147">Значение true указывает, что система поддерживает состояние сна S4.</span><span class="sxs-lookup"><span data-stu-id="0166b-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="0166b-148">остановки</span><span class="sxs-lookup"><span data-stu-id="0166b-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0166b-149">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0166b-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0166b-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0166b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0166b-151">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="0166b-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="0166b-152">Значение true указывает, что система поддерживает состояние сна S5.</span><span class="sxs-lookup"><span data-stu-id="0166b-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0166b-153">Требования</span><span class="sxs-lookup"><span data-stu-id="0166b-153">Requirements</span></span>



| <span data-ttu-id="0166b-154">Требование</span><span class="sxs-lookup"><span data-stu-id="0166b-154">Requirement</span></span> | <span data-ttu-id="0166b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="0166b-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0166b-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0166b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="0166b-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0166b-157">None supported</span></span><br/>                            |
| <span data-ttu-id="0166b-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0166b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="0166b-159">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0166b-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0166b-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0166b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0166b-161">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="0166b-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




