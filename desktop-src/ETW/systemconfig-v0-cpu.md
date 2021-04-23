---
description: Этот класс является классом типа событий для событий конфигурации ЦП.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: Класс SystemConfig_V0_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6963201f76afa40e9b1741dc2936fa2ab4433a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999336"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="0acd3-103">\_ \_ Класс ЦП системконфиг v0</span><span class="sxs-lookup"><span data-stu-id="0acd3-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="0acd3-104">Этот класс является классом типа событий для событий конфигурации ЦП.</span><span class="sxs-lookup"><span data-stu-id="0acd3-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="0acd3-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="0acd3-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0acd3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0acd3-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a><span data-ttu-id="0acd3-107">Участники</span><span class="sxs-lookup"><span data-stu-id="0acd3-107">Members</span></span>

<span data-ttu-id="0acd3-108">Класс **\_ \_ ЦП системконфиг v0** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0acd3-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="0acd3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0acd3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0acd3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0acd3-110">Properties</span></span>

<span data-ttu-id="0acd3-111">Класс **\_ \_ ЦП системконфиг v0** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0acd3-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0acd3-112">**аллокатионгрануларити**</span><span class="sxs-lookup"><span data-stu-id="0acd3-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0acd3-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0acd3-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0acd3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-115">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="0acd3-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="0acd3-116">Степень гранулярности, с которой выделяется виртуальная память.</span><span class="sxs-lookup"><span data-stu-id="0acd3-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="0acd3-117">**ИмяКомпьютера**</span><span class="sxs-lookup"><span data-stu-id="0acd3-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0acd3-118">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="0acd3-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0acd3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-120">Квалификаторы: **вмидатаид** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="0acd3-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="0acd3-121">Имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="0acd3-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="0acd3-122">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="0acd3-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0acd3-123">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="0acd3-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0acd3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-125">Квалификаторы: **вмидатаид** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="0acd3-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="0acd3-126">Имя домена, членом которого является компьютер.</span><span class="sxs-lookup"><span data-stu-id="0acd3-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="0acd3-127">**мемсизе**</span><span class="sxs-lookup"><span data-stu-id="0acd3-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0acd3-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0acd3-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0acd3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-130">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="0acd3-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="0acd3-131">Общий объем физической памяти, доступной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="0acd3-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="0acd3-132">**Частоты**</span><span class="sxs-lookup"><span data-stu-id="0acd3-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0acd3-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0acd3-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0acd3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-135">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="0acd3-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="0acd3-136">Максимальная скорость процессора в мегагерцах.</span><span class="sxs-lookup"><span data-stu-id="0acd3-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="0acd3-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="0acd3-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0acd3-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0acd3-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0acd3-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-140">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="0acd3-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="0acd3-141">Количество процессоров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0acd3-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="0acd3-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="0acd3-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0acd3-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0acd3-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0acd3-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0acd3-145">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="0acd3-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="0acd3-146">Размер страницы переключения в байтах.</span><span class="sxs-lookup"><span data-stu-id="0acd3-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0acd3-147">Требования</span><span class="sxs-lookup"><span data-stu-id="0acd3-147">Requirements</span></span>



| <span data-ttu-id="0acd3-148">Требование</span><span class="sxs-lookup"><span data-stu-id="0acd3-148">Requirement</span></span> | <span data-ttu-id="0acd3-149">Значение</span><span class="sxs-lookup"><span data-stu-id="0acd3-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0acd3-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0acd3-150">Minimum supported client</span></span><br/> | <span data-ttu-id="0acd3-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0acd3-151">None supported</span></span><br/>                            |
| <span data-ttu-id="0acd3-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0acd3-152">Minimum supported server</span></span><br/> | <span data-ttu-id="0acd3-153">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0acd3-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0acd3-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0acd3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0acd3-155">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="0acd3-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




