---
description: Process_V1_TypeGroup1 класс — этот класс является классом типа события для событий процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Класс Process_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7f4426f34a97ff79dc41806f1e0070013528d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106332"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="e5193-104">\_ \_ Класс TypeGroup1 процесса v1</span><span class="sxs-lookup"><span data-stu-id="e5193-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="e5193-105">Этот класс является классом типа события для событий процесса.</span><span class="sxs-lookup"><span data-stu-id="e5193-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="e5193-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="e5193-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5193-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5193-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="e5193-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e5193-108">Members</span></span>

<span data-ttu-id="e5193-109">Класс **Process \_ v1 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e5193-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="e5193-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5193-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5193-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="e5193-111">Properties</span></span>

<span data-ttu-id="e5193-112">Класс **Process \_ v1 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e5193-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5193-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="e5193-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5193-114">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5193-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5193-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5193-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5193-116">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="e5193-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="e5193-117">Состояние завершения остановленного процесса.</span><span class="sxs-lookup"><span data-stu-id="e5193-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="e5193-118">имажефиленаме</span><span class="sxs-lookup"><span data-stu-id="e5193-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5193-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5193-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5193-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5193-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5193-121">Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="e5193-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="e5193-122">Путь к исполняемому файлу процесса.</span><span class="sxs-lookup"><span data-stu-id="e5193-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="e5193-123">пажедиректорибасе</span><span class="sxs-lookup"><span data-stu-id="e5193-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5193-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5193-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5193-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5193-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5193-126">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="e5193-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e5193-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e5193-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e5193-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="e5193-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5193-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5193-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5193-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5193-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5193-131">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="e5193-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e5193-132">Уникальный идентификатор процесса, который создает этот процесс.</span><span class="sxs-lookup"><span data-stu-id="e5193-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="e5193-133">Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса.</span><span class="sxs-lookup"><span data-stu-id="e5193-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="e5193-134">Возможно, процесс, идентифицированный Парентпроцессид, завершается, поэтому Парентпроцессид может не ссылаться на выполняющийся процесс.</span><span class="sxs-lookup"><span data-stu-id="e5193-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="e5193-135">Также возможно, что Парентпроцессид неправильно ссылается на процесс, который повторно использует идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="e5193-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="e5193-136">**Windows Server 2003:** Включает квалификатор Format ("x").</span><span class="sxs-lookup"><span data-stu-id="e5193-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="e5193-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="e5193-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5193-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5193-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5193-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5193-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5193-140">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="e5193-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e5193-141">Глобальный идентификатор процесса, который можно использовать для идентификации процесса.</span><span class="sxs-lookup"><span data-stu-id="e5193-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="e5193-142">Значение допустимо с момента создания процесса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="e5193-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="e5193-143">**Windows Server 2003:** Включает квалификатор Format ("x").</span><span class="sxs-lookup"><span data-stu-id="e5193-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="e5193-144">SessionId</span><span class="sxs-lookup"><span data-stu-id="e5193-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5193-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5193-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5193-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5193-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5193-147">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="e5193-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e5193-148">Уникальный идентификатор, создаваемый операционной системой при создании нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="e5193-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="e5193-149">Сеанс охватывает период времени от входа до выхода из определенной системы.</span><span class="sxs-lookup"><span data-stu-id="e5193-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="e5193-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="e5193-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5193-151">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="e5193-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e5193-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5193-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5193-153">Квалификаторы: Вмидатаид (6), Extension ("sid")</span><span class="sxs-lookup"><span data-stu-id="e5193-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="e5193-154">Идентификатор безопасности (SID) для пользовательского контекста, в котором происходит событие.</span><span class="sxs-lookup"><span data-stu-id="e5193-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5193-155">Требования</span><span class="sxs-lookup"><span data-stu-id="e5193-155">Requirements</span></span>



| <span data-ttu-id="e5193-156">Требование</span><span class="sxs-lookup"><span data-stu-id="e5193-156">Requirement</span></span> | <span data-ttu-id="e5193-157">Значение</span><span class="sxs-lookup"><span data-stu-id="e5193-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5193-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5193-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e5193-159">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e5193-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e5193-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5193-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e5193-161">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5193-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5193-162">См. также</span><span class="sxs-lookup"><span data-stu-id="e5193-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5193-163">**Процесс \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e5193-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="e5193-164">**Процесс \_ v1**</span><span class="sxs-lookup"><span data-stu-id="e5193-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




