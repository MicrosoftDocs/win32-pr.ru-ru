---
description: Этот класс является классом типа события для событий процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Класс Process_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ad2ebcd9a3e1563f6e2f4c82d90dd4d2c80112f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897825"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="fdb57-104">Process \_ TypeGroup1, класс</span><span class="sxs-lookup"><span data-stu-id="fdb57-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="fdb57-105">Этот класс является классом типа события для событий процесса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="fdb57-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="fdb57-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb57-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdb57-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="fdb57-108">Участники</span><span class="sxs-lookup"><span data-stu-id="fdb57-108">Members</span></span>

<span data-ttu-id="fdb57-109">Класс **Process \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fdb57-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="fdb57-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fdb57-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fdb57-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="fdb57-111">Properties</span></span>

<span data-ttu-id="fdb57-112">Класс **Process \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fdb57-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fdb57-113">Командная строка</span><span class="sxs-lookup"><span data-stu-id="fdb57-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fdb57-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-116">Квалификаторы: Вмидатаид (9), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="fdb57-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-117">Полная командная строка процесса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="fdb57-118">директоритаблебасе</span><span class="sxs-lookup"><span data-stu-id="fdb57-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fdb57-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-121">Квалификаторы: Вмидатаид (6), Pointer</span><span class="sxs-lookup"><span data-stu-id="fdb57-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-122">Физический адрес таблицы страницы процесса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="fdb57-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="fdb57-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-124">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fdb57-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-126">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="fdb57-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-127">Состояние завершения остановленного процесса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="fdb57-128">имажефиленаме</span><span class="sxs-lookup"><span data-stu-id="fdb57-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fdb57-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-131">Квалификаторы: Вмидатаид (8), Стрингтерминатион ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="fdb57-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-132">Путь к исполняемому файлу процесса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="fdb57-133">ParentId</span><span class="sxs-lookup"><span data-stu-id="fdb57-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fdb57-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-136">Квалификаторы: Вмидатаид (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="fdb57-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-137">Уникальный идентификатор процесса, который создает этот процесс.</span><span class="sxs-lookup"><span data-stu-id="fdb57-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="fdb57-138">Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="fdb57-139">Возможно, процесс, идентифицированный Парентпроцессид, завершается, поэтому Парентпроцессид может не ссылаться на выполняющийся процесс.</span><span class="sxs-lookup"><span data-stu-id="fdb57-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="fdb57-140">Также возможно, что Парентпроцессид неправильно ссылается на процесс, который повторно использует идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="fdb57-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="fdb57-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fdb57-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-144">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="fdb57-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-145">Глобальный идентификатор процесса, который можно использовать для идентификации процесса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="fdb57-146">Значение допустимо с момента создания процесса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="fdb57-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="fdb57-147">SessionId</span><span class="sxs-lookup"><span data-stu-id="fdb57-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fdb57-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-150">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="fdb57-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-151">Уникальный идентификатор, создаваемый операционной системой при создании нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="fdb57-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="fdb57-152">Сеанс охватывает период времени от входа до выхода из определенной системы.</span><span class="sxs-lookup"><span data-stu-id="fdb57-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="fdb57-153">уникуепроцесскэй</span><span class="sxs-lookup"><span data-stu-id="fdb57-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-154">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fdb57-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-156">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="fdb57-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-157">Адрес объекта процесса в ядре.</span><span class="sxs-lookup"><span data-stu-id="fdb57-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="fdb57-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="fdb57-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdb57-159">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="fdb57-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fdb57-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdb57-161">Квалификаторы: Вмидатаид (7), Extension ("sid")</span><span class="sxs-lookup"><span data-stu-id="fdb57-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="fdb57-162">Идентификатор безопасности (SID) для пользовательского контекста, в котором происходит событие.</span><span class="sxs-lookup"><span data-stu-id="fdb57-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdb57-163">Примечания</span><span class="sxs-lookup"><span data-stu-id="fdb57-163">Remarks</span></span>

<span data-ttu-id="fdb57-164">Типы событий Дкстарт и Дценд перечисляют процесс, выполняемый в данный момент, включая бездействующий и системный процессы, на момент запуска и завершения сеанса ядра соответственно.</span><span class="sxs-lookup"><span data-stu-id="fdb57-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb57-165">Требования</span><span class="sxs-lookup"><span data-stu-id="fdb57-165">Requirements</span></span>



| <span data-ttu-id="fdb57-166">Требование</span><span class="sxs-lookup"><span data-stu-id="fdb57-166">Requirement</span></span> | <span data-ttu-id="fdb57-167">Значение</span><span class="sxs-lookup"><span data-stu-id="fdb57-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fdb57-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdb57-168">Minimum supported client</span></span><br/> | <span data-ttu-id="fdb57-169">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fdb57-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fdb57-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdb57-170">Minimum supported server</span></span><br/> | <span data-ttu-id="fdb57-171">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fdb57-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fdb57-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdb57-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb57-173">**Процесс**</span><span class="sxs-lookup"><span data-stu-id="fdb57-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




