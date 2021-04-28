---
description: Process_V2_TypeGroup1 класс — этот класс является классом типа события для событий процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Класс Process_V2_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: b587a07f33b066cfd7dbeebc44d7277b33c6bee8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106312"
---
# <a name="process_v2_typegroup1-class"></a><span data-ttu-id="c2527-104">\_ \_ Класс TypeGroup1 процесса v2</span><span class="sxs-lookup"><span data-stu-id="c2527-104">Process\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="c2527-105">Этот класс является классом типа события для событий процесса.</span><span class="sxs-lookup"><span data-stu-id="c2527-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="c2527-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="c2527-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2527-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2527-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="c2527-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c2527-108">Members</span></span>

<span data-ttu-id="c2527-109">Класс **Process \_ v2 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c2527-109">The **Process\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="c2527-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2527-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2527-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="c2527-111">Properties</span></span>

<span data-ttu-id="c2527-112">Класс **Process \_ v2 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c2527-112">The **Process\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2527-113">Командная строка</span><span class="sxs-lookup"><span data-stu-id="c2527-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2527-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c2527-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2527-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2527-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2527-116">Квалификаторы: Вмидатаид (8), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="c2527-116">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c2527-117">Полная командная строка процесса.</span><span class="sxs-lookup"><span data-stu-id="c2527-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="c2527-118">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="c2527-118">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2527-119">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c2527-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2527-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2527-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2527-121">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="c2527-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="c2527-122">Состояние завершения остановленного процесса.</span><span class="sxs-lookup"><span data-stu-id="c2527-122">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="c2527-123">имажефиленаме</span><span class="sxs-lookup"><span data-stu-id="c2527-123">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2527-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c2527-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2527-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2527-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2527-126">Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="c2527-126">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="c2527-127">Путь к исполняемому файлу процесса.</span><span class="sxs-lookup"><span data-stu-id="c2527-127">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="c2527-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="c2527-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2527-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2527-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2527-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2527-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2527-131">Квалификаторы: Вмидатаид (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="c2527-131">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c2527-132">Уникальный идентификатор процесса, который создает этот процесс.</span><span class="sxs-lookup"><span data-stu-id="c2527-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="c2527-133">Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса.</span><span class="sxs-lookup"><span data-stu-id="c2527-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="c2527-134">Возможно, процесс, идентифицированный Парентпроцессид, завершается, поэтому Парентпроцессид может не ссылаться на выполняющийся процесс.</span><span class="sxs-lookup"><span data-stu-id="c2527-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="c2527-135">Также возможно, что Парентпроцессид неправильно ссылается на процесс, который повторно использует идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="c2527-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c2527-136">ProcessId</span><span class="sxs-lookup"><span data-stu-id="c2527-136">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2527-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2527-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2527-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2527-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2527-139">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="c2527-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="c2527-140">Глобальный идентификатор процесса, который можно использовать для идентификации процесса.</span><span class="sxs-lookup"><span data-stu-id="c2527-140">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="c2527-141">Значение допустимо с момента создания процесса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="c2527-141">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="c2527-142">SessionId</span><span class="sxs-lookup"><span data-stu-id="c2527-142">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2527-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2527-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2527-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2527-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2527-145">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="c2527-145">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c2527-146">Уникальный идентификатор, создаваемый операционной системой при создании нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="c2527-146">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="c2527-147">Сеанс охватывает период времени от входа до выхода из определенной системы.</span><span class="sxs-lookup"><span data-stu-id="c2527-147">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="c2527-148">уникуепроцесскэй</span><span class="sxs-lookup"><span data-stu-id="c2527-148">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2527-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2527-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2527-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2527-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2527-151">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="c2527-151">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c2527-152">Адрес объекта процесса в ядре.</span><span class="sxs-lookup"><span data-stu-id="c2527-152">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="c2527-153">UserSID</span><span class="sxs-lookup"><span data-stu-id="c2527-153">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2527-154">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="c2527-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c2527-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2527-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2527-156">Квалификаторы: Вмидатаид (6), Extension ("sid")</span><span class="sxs-lookup"><span data-stu-id="c2527-156">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="c2527-157">Идентификатор безопасности (SID) для пользовательского контекста, в котором происходит событие.</span><span class="sxs-lookup"><span data-stu-id="c2527-157">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2527-158">Remarks</span><span class="sxs-lookup"><span data-stu-id="c2527-158">Remarks</span></span>

<span data-ttu-id="c2527-159">Типы событий Дкстарт и Дценд перечисляют процесс, выполняемый в данный момент, включая бездействующий и системный процессы, на момент запуска и завершения сеанса ядра соответственно.</span><span class="sxs-lookup"><span data-stu-id="c2527-159">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2527-160">Требования</span><span class="sxs-lookup"><span data-stu-id="c2527-160">Requirements</span></span>



| <span data-ttu-id="c2527-161">Требование</span><span class="sxs-lookup"><span data-stu-id="c2527-161">Requirement</span></span> | <span data-ttu-id="c2527-162">Значение</span><span class="sxs-lookup"><span data-stu-id="c2527-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c2527-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2527-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c2527-164">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c2527-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2527-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2527-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c2527-166">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c2527-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c2527-167">См. также</span><span class="sxs-lookup"><span data-stu-id="c2527-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2527-168">**Процесс \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="c2527-168">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




