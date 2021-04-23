---
description: Этот класс является классом типа событий для событий конфигурации питания. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: d27586451f944ac9c94e9ec2d204035c21f37679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984397"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="cf136-104">\_Класс питания системконфиг</span><span class="sxs-lookup"><span data-stu-id="cf136-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="cf136-105">Этот класс является классом типа событий для событий конфигурации питания.</span><span class="sxs-lookup"><span data-stu-id="cf136-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="cf136-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="cf136-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf136-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf136-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="cf136-108">Участники</span><span class="sxs-lookup"><span data-stu-id="cf136-108">Members</span></span>

<span data-ttu-id="cf136-109">Класс **\_ питания системконфиг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cf136-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="cf136-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="cf136-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf136-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cf136-111">Properties</span></span>

<span data-ttu-id="cf136-112">Класс **\_ питания системконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf136-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf136-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="cf136-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf136-114">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cf136-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf136-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf136-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf136-116">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="cf136-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="cf136-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="cf136-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cf136-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="cf136-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf136-119">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cf136-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf136-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf136-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf136-121">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="cf136-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="cf136-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="cf136-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cf136-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="cf136-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf136-124">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cf136-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf136-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf136-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf136-126">Квалификаторы: Вмидатаид (8)</span><span class="sxs-lookup"><span data-stu-id="cf136-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="cf136-127">Не используется.</span><span class="sxs-lookup"><span data-stu-id="cf136-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cf136-128">s1</span><span class="sxs-lookup"><span data-stu-id="cf136-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf136-129">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cf136-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf136-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf136-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf136-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="cf136-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="cf136-132">Значение true указывает, что система поддерживает состояние сна S1.</span><span class="sxs-lookup"><span data-stu-id="cf136-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="cf136-133">s2</span><span class="sxs-lookup"><span data-stu-id="cf136-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf136-134">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cf136-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf136-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf136-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf136-136">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="cf136-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="cf136-137">Значение true указывает, что система поддерживает состояние сна S2.</span><span class="sxs-lookup"><span data-stu-id="cf136-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="cf136-138">s3</span><span class="sxs-lookup"><span data-stu-id="cf136-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf136-139">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cf136-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf136-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf136-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf136-141">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="cf136-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="cf136-142">Значение true указывает, что система поддерживает состояние сна S3.</span><span class="sxs-lookup"><span data-stu-id="cf136-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="cf136-143">S4</span><span class="sxs-lookup"><span data-stu-id="cf136-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf136-144">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cf136-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf136-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf136-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf136-146">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="cf136-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="cf136-147">Значение true указывает, что система поддерживает состояние сна S4.</span><span class="sxs-lookup"><span data-stu-id="cf136-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="cf136-148">остановки</span><span class="sxs-lookup"><span data-stu-id="cf136-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf136-149">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="cf136-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf136-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf136-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf136-151">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="cf136-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="cf136-152">Значение true указывает, что система поддерживает состояние сна S5.</span><span class="sxs-lookup"><span data-stu-id="cf136-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf136-153">Требования</span><span class="sxs-lookup"><span data-stu-id="cf136-153">Requirements</span></span>



| <span data-ttu-id="cf136-154">Требование</span><span class="sxs-lookup"><span data-stu-id="cf136-154">Requirement</span></span> | <span data-ttu-id="cf136-155">Значение</span><span class="sxs-lookup"><span data-stu-id="cf136-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf136-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf136-156">Minimum supported client</span></span><br/> | <span data-ttu-id="cf136-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf136-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf136-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf136-158">Minimum supported server</span></span><br/> | <span data-ttu-id="cf136-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf136-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf136-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf136-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf136-161">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="cf136-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




