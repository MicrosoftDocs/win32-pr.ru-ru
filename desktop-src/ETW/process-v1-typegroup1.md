---
description: Этот класс является классом типа события для событий процесса. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: fc2308965de5c06a25858a138d4536763613a4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347842"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="2d754-104">\_ \_ Класс TypeGroup1 процесса v1</span><span class="sxs-lookup"><span data-stu-id="2d754-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="2d754-105">Этот класс является классом типа события для событий процесса.</span><span class="sxs-lookup"><span data-stu-id="2d754-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="2d754-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="2d754-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d754-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d754-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="2d754-108">Участники</span><span class="sxs-lookup"><span data-stu-id="2d754-108">Members</span></span>

<span data-ttu-id="2d754-109">Класс **Process \_ v1 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2d754-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="2d754-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d754-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d754-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d754-111">Properties</span></span>

<span data-ttu-id="2d754-112">Класс **Process \_ v1 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2d754-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d754-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="2d754-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d754-114">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2d754-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d754-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d754-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d754-116">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="2d754-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="2d754-117">Состояние завершения остановленного процесса.</span><span class="sxs-lookup"><span data-stu-id="2d754-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="2d754-118">имажефиленаме</span><span class="sxs-lookup"><span data-stu-id="2d754-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d754-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2d754-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d754-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d754-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d754-121">Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="2d754-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="2d754-122">Путь к исполняемому файлу процесса.</span><span class="sxs-lookup"><span data-stu-id="2d754-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="2d754-123">пажедиректорибасе</span><span class="sxs-lookup"><span data-stu-id="2d754-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d754-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d754-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d754-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d754-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d754-126">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="2d754-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2d754-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2d754-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2d754-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="2d754-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d754-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d754-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d754-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d754-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d754-131">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="2d754-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="2d754-132">Уникальный идентификатор процесса, который создает этот процесс.</span><span class="sxs-lookup"><span data-stu-id="2d754-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="2d754-133">Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса.</span><span class="sxs-lookup"><span data-stu-id="2d754-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="2d754-134">Возможно, процесс, идентифицированный Парентпроцессид, завершается, поэтому Парентпроцессид может не ссылаться на выполняющийся процесс.</span><span class="sxs-lookup"><span data-stu-id="2d754-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="2d754-135">Также возможно, что Парентпроцессид неправильно ссылается на процесс, который повторно использует идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="2d754-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="2d754-136">**Windows Server 2003:** Включает квалификатор Format ("x").</span><span class="sxs-lookup"><span data-stu-id="2d754-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="2d754-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="2d754-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d754-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d754-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d754-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d754-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d754-140">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="2d754-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2d754-141">Глобальный идентификатор процесса, который можно использовать для идентификации процесса.</span><span class="sxs-lookup"><span data-stu-id="2d754-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="2d754-142">Значение допустимо с момента создания процесса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="2d754-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="2d754-143">**Windows Server 2003:** Включает квалификатор Format ("x").</span><span class="sxs-lookup"><span data-stu-id="2d754-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="2d754-144">SessionId</span><span class="sxs-lookup"><span data-stu-id="2d754-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d754-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d754-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d754-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d754-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d754-147">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="2d754-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="2d754-148">Уникальный идентификатор, создаваемый операционной системой при создании нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="2d754-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="2d754-149">Сеанс охватывает период времени от входа до выхода из определенной системы.</span><span class="sxs-lookup"><span data-stu-id="2d754-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="2d754-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="2d754-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d754-151">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="2d754-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2d754-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d754-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d754-153">Квалификаторы: Вмидатаид (6), Extension ("sid")</span><span class="sxs-lookup"><span data-stu-id="2d754-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="2d754-154">Идентификатор безопасности (SID) для пользовательского контекста, в котором происходит событие.</span><span class="sxs-lookup"><span data-stu-id="2d754-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d754-155">Требования</span><span class="sxs-lookup"><span data-stu-id="2d754-155">Requirements</span></span>



| <span data-ttu-id="2d754-156">Требование</span><span class="sxs-lookup"><span data-stu-id="2d754-156">Requirement</span></span> | <span data-ttu-id="2d754-157">Значение</span><span class="sxs-lookup"><span data-stu-id="2d754-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d754-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d754-158">Minimum supported client</span></span><br/> | <span data-ttu-id="2d754-159">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2d754-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2d754-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d754-160">Minimum supported server</span></span><br/> | <span data-ttu-id="2d754-161">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d754-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d754-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d754-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d754-163">**Процесс \_ v1**</span><span class="sxs-lookup"><span data-stu-id="2d754-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="2d754-164">**Процесс \_ v1**</span><span class="sxs-lookup"><span data-stu-id="2d754-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




