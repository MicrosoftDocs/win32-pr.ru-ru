---
description: '\_Класс ЦП хвконфиг является классом типа событий для событий конфигурации ЦП. Следующий синтаксис упрощен из MOF-кода.'
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: Класс HWConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 493952e25080d4a64e018477ca1b45033c8747af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984797"
---
# <a name="hwconfig_cpu-class"></a><span data-ttu-id="7b195-104">\_Класс ЦП хвконфиг</span><span class="sxs-lookup"><span data-stu-id="7b195-104">HWConfig\_CPU class</span></span>

<span data-ttu-id="7b195-105">Класс **\_ ЦП хвконфиг** является классом типа событий для событий конфигурации ЦП.</span><span class="sxs-lookup"><span data-stu-id="7b195-105">The **HWConfig\_CPU** class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="7b195-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="7b195-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b195-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b195-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a><span data-ttu-id="7b195-108">Участники</span><span class="sxs-lookup"><span data-stu-id="7b195-108">Members</span></span>

<span data-ttu-id="7b195-109">Класс **\_ ЦП хвконфиг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7b195-109">The **HWConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="7b195-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b195-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b195-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b195-111">Properties</span></span>

<span data-ttu-id="7b195-112">Класс **\_ ЦП хвконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7b195-112">The **HWConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b195-113">аллокатионгрануларити</span><span class="sxs-lookup"><span data-stu-id="7b195-113">AllocationGranularity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b195-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b195-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b195-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b195-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b195-116">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="7b195-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="7b195-117">Степень гранулярности, с которой выделяется виртуальная память.</span><span class="sxs-lookup"><span data-stu-id="7b195-117">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="7b195-118">ИмяКомпьютера</span><span class="sxs-lookup"><span data-stu-id="7b195-118">ComputerName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b195-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b195-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b195-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b195-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b195-121">Квалификаторы: Вмидатаид (6), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="7b195-121">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="7b195-122">Имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="7b195-122">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="7b195-123">мемсизе</span><span class="sxs-lookup"><span data-stu-id="7b195-123">MemSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b195-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b195-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b195-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b195-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b195-126">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="7b195-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="7b195-127">Общий объем физической памяти, доступной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="7b195-127">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7b195-128">Частоты</span><span class="sxs-lookup"><span data-stu-id="7b195-128">MHz</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b195-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b195-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b195-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b195-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b195-131">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="7b195-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="7b195-132">Максимальная скорость процессора в мегагерцах.</span><span class="sxs-lookup"><span data-stu-id="7b195-132">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="7b195-133">NumberOfProcessors</span><span class="sxs-lookup"><span data-stu-id="7b195-133">NumberOfProcessors</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b195-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b195-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b195-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b195-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b195-136">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="7b195-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="7b195-137">Количество процессоров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7b195-137">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="7b195-138">PageSize</span><span class="sxs-lookup"><span data-stu-id="7b195-138">PageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b195-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b195-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b195-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b195-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b195-141">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="7b195-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="7b195-142">Размер страницы переключения в байтах.</span><span class="sxs-lookup"><span data-stu-id="7b195-142">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b195-143">Требования</span><span class="sxs-lookup"><span data-stu-id="7b195-143">Requirements</span></span>



| <span data-ttu-id="7b195-144">Требование</span><span class="sxs-lookup"><span data-stu-id="7b195-144">Requirement</span></span> | <span data-ttu-id="7b195-145">Значение</span><span class="sxs-lookup"><span data-stu-id="7b195-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="7b195-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b195-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7b195-147">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7b195-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7b195-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b195-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7b195-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7b195-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="7b195-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b195-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b195-151">**хвконфиг**</span><span class="sxs-lookup"><span data-stu-id="7b195-151">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




