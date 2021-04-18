---
description: Этот класс является классом типа событий для событий подпрограммы обработки прерываний (ISR). Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: Класс ISR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985597"
---
# <a name="isr-class"></a><span data-ttu-id="68c91-104">Класс ISR</span><span class="sxs-lookup"><span data-stu-id="68c91-104">ISR class</span></span>

<span data-ttu-id="68c91-105">Этот класс является классом типа событий для событий подпрограммы обработки прерываний (ISR).</span><span class="sxs-lookup"><span data-stu-id="68c91-105">This class is the event type class for interrupt service routine (ISR) events.</span></span>

<span data-ttu-id="68c91-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="68c91-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c91-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68c91-107">Syntax</span></span>

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="68c91-108">Участники</span><span class="sxs-lookup"><span data-stu-id="68c91-108">Members</span></span>

<span data-ttu-id="68c91-109">Класс **ISR** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="68c91-109">The **ISR** class has these types of members:</span></span>

-   [<span data-ttu-id="68c91-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="68c91-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68c91-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="68c91-111">Properties</span></span>

<span data-ttu-id="68c91-112">Класс **ISR** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="68c91-112">The **ISR** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68c91-113">**инитиалтиме**</span><span class="sxs-lookup"><span data-stu-id="68c91-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68c91-114">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="68c91-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="68c91-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68c91-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68c91-116">Квалификаторы: Вмидатаид (1), Extension ("Вмитиме")</span><span class="sxs-lookup"><span data-stu-id="68c91-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="68c91-117">Время записи ISR.</span><span class="sxs-lookup"><span data-stu-id="68c91-117">ISR entry time.</span></span>

</dd> <dt>

<span data-ttu-id="68c91-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="68c91-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68c91-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68c91-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68c91-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68c91-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68c91-121">Квалификаторы: Вмидатаид (5), Pointer</span><span class="sxs-lookup"><span data-stu-id="68c91-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="68c91-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="68c91-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="68c91-123">**ReturnValue**</span><span class="sxs-lookup"><span data-stu-id="68c91-123">**ReturnValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68c91-124">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68c91-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68c91-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68c91-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68c91-126">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="68c91-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="68c91-127">Логическое значение, указывающее, было ли прерывание запрошено (имеет значение true, если прерывание было затребовано).</span><span class="sxs-lookup"><span data-stu-id="68c91-127">Boolean indicating if the interrupt was claimed (is True if the interrupt was claimed).</span></span>

</dd> <dt>

<span data-ttu-id="68c91-128">**Подпрограмма**</span><span class="sxs-lookup"><span data-stu-id="68c91-128">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68c91-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68c91-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68c91-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68c91-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68c91-131">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="68c91-131">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="68c91-132">Адрес подпрограммы ISR.</span><span class="sxs-lookup"><span data-stu-id="68c91-132">Address of ISR routine.</span></span> <span data-ttu-id="68c91-133">Используйте адрес с событиями Image, чтобы определить, какое изображение запущено.</span><span class="sxs-lookup"><span data-stu-id="68c91-133">Use the address with the Image events to find which image started.</span></span>

</dd> <dt>

<span data-ttu-id="68c91-134">**Вектор**</span><span class="sxs-lookup"><span data-stu-id="68c91-134">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68c91-135">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="68c91-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="68c91-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68c91-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68c91-137">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="68c91-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="68c91-138">Вектор из таблицы дескрипторов прерываний, которому назначается процедура ISR.</span><span class="sxs-lookup"><span data-stu-id="68c91-138">Vector from interrupt descriptor table to which ISR routine is assigned.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68c91-139">Требования</span><span class="sxs-lookup"><span data-stu-id="68c91-139">Requirements</span></span>



| <span data-ttu-id="68c91-140">Требование</span><span class="sxs-lookup"><span data-stu-id="68c91-140">Requirement</span></span> | <span data-ttu-id="68c91-141">Значение</span><span class="sxs-lookup"><span data-stu-id="68c91-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68c91-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68c91-142">Minimum supported client</span></span><br/> | <span data-ttu-id="68c91-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68c91-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68c91-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68c91-144">Minimum supported server</span></span><br/> | <span data-ttu-id="68c91-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68c91-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




