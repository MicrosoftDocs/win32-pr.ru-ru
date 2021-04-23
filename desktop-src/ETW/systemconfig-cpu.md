---
description: Этот класс является классом типа событий для событий конфигурации ЦП.
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: Класс SystemConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: d08d0eeac9aa2287576bbb6dfe0e8ce41f116e8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985696"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="cb93a-103">\_Класс ЦП системконфиг</span><span class="sxs-lookup"><span data-stu-id="cb93a-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="cb93a-104">Этот класс является классом типа событий для событий конфигурации ЦП.</span><span class="sxs-lookup"><span data-stu-id="cb93a-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="cb93a-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="cb93a-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb93a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb93a-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a><span data-ttu-id="cb93a-107">Участники</span><span class="sxs-lookup"><span data-stu-id="cb93a-107">Members</span></span>

<span data-ttu-id="cb93a-108">Класс **\_ ЦП системконфиг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cb93a-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="cb93a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="cb93a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb93a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="cb93a-110">Properties</span></span>

<span data-ttu-id="cb93a-111">Класс **\_ ЦП системконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cb93a-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb93a-112">**аллокатионгрануларити**</span><span class="sxs-lookup"><span data-stu-id="cb93a-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb93a-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb93a-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cb93a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-115">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="cb93a-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="cb93a-116">Степень гранулярности, с которой выделяется виртуальная память.</span><span class="sxs-lookup"><span data-stu-id="cb93a-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="cb93a-117">**ИмяКомпьютера**</span><span class="sxs-lookup"><span data-stu-id="cb93a-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb93a-118">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="cb93a-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cb93a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-120">Квалификаторы: **вмидатаид** (6), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="cb93a-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="cb93a-121">Имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="cb93a-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="cb93a-122">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="cb93a-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb93a-123">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="cb93a-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cb93a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-125">Квалификаторы: **вмидатаид** (7), **Max** (132), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="cb93a-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="cb93a-126">Имя домена, членом которого является компьютер.</span><span class="sxs-lookup"><span data-stu-id="cb93a-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="cb93a-127">**хиперсреадингфлаг**</span><span class="sxs-lookup"><span data-stu-id="cb93a-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb93a-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb93a-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cb93a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-130">Квалификаторы: **вмидатаид** (8), Pointer</span><span class="sxs-lookup"><span data-stu-id="cb93a-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cb93a-131">Указывает, включен ли параметр Hyper-Threading для процессора.</span><span class="sxs-lookup"><span data-stu-id="cb93a-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="cb93a-132">Каждый бит отражает состояние ЦП компьютера на уровне Hyper-Threading.</span><span class="sxs-lookup"><span data-stu-id="cb93a-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="cb93a-133">**мемсизе**</span><span class="sxs-lookup"><span data-stu-id="cb93a-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb93a-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb93a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cb93a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-136">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="cb93a-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="cb93a-137">Общий объем физической памяти, доступной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="cb93a-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="cb93a-138">**Частоты**</span><span class="sxs-lookup"><span data-stu-id="cb93a-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb93a-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb93a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cb93a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-141">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="cb93a-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="cb93a-142">Максимальная скорость процессора в мегагерцах.</span><span class="sxs-lookup"><span data-stu-id="cb93a-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="cb93a-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="cb93a-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb93a-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb93a-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cb93a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-146">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="cb93a-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="cb93a-147">Количество процессоров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="cb93a-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="cb93a-148">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="cb93a-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb93a-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb93a-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cb93a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb93a-151">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="cb93a-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="cb93a-152">Размер страницы переключения в байтах.</span><span class="sxs-lookup"><span data-stu-id="cb93a-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb93a-153">Требования</span><span class="sxs-lookup"><span data-stu-id="cb93a-153">Requirements</span></span>



| <span data-ttu-id="cb93a-154">Требование</span><span class="sxs-lookup"><span data-stu-id="cb93a-154">Requirement</span></span> | <span data-ttu-id="cb93a-155">Значение</span><span class="sxs-lookup"><span data-stu-id="cb93a-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb93a-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb93a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="cb93a-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb93a-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb93a-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb93a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="cb93a-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb93a-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb93a-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb93a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb93a-161">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="cb93a-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




