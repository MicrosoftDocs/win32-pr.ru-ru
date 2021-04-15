---
description: Этот класс является классом типа события для событий процесса. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: 01da5a8254627d6378c9f99aa2ba36dc6714e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985864"
---
# <a name="process_v2_typegroup1-class"></a><span data-ttu-id="641b9-104">\_ \_ Класс TypeGroup1 процесса v2</span><span class="sxs-lookup"><span data-stu-id="641b9-104">Process\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="641b9-105">Этот класс является классом типа события для событий процесса.</span><span class="sxs-lookup"><span data-stu-id="641b9-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="641b9-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="641b9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="641b9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="641b9-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="641b9-108">Участники</span><span class="sxs-lookup"><span data-stu-id="641b9-108">Members</span></span>

<span data-ttu-id="641b9-109">Класс **Process \_ v2 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="641b9-109">The **Process\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="641b9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="641b9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="641b9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="641b9-111">Properties</span></span>

<span data-ttu-id="641b9-112">Класс **Process \_ v2 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="641b9-112">The **Process\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="641b9-113">Командная строка</span><span class="sxs-lookup"><span data-stu-id="641b9-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="641b9-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="641b9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="641b9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="641b9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="641b9-116">Квалификаторы: Вмидатаид (8), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="641b9-116">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="641b9-117">Полная командная строка процесса.</span><span class="sxs-lookup"><span data-stu-id="641b9-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="641b9-118">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="641b9-118">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="641b9-119">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="641b9-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="641b9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="641b9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="641b9-121">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="641b9-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="641b9-122">Состояние завершения остановленного процесса.</span><span class="sxs-lookup"><span data-stu-id="641b9-122">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="641b9-123">имажефиленаме</span><span class="sxs-lookup"><span data-stu-id="641b9-123">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="641b9-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="641b9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="641b9-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="641b9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="641b9-126">Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="641b9-126">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="641b9-127">Путь к исполняемому файлу процесса.</span><span class="sxs-lookup"><span data-stu-id="641b9-127">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="641b9-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="641b9-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="641b9-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="641b9-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="641b9-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="641b9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="641b9-131">Квалификаторы: Вмидатаид (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="641b9-131">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="641b9-132">Уникальный идентификатор процесса, который создает этот процесс.</span><span class="sxs-lookup"><span data-stu-id="641b9-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="641b9-133">Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса.</span><span class="sxs-lookup"><span data-stu-id="641b9-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="641b9-134">Возможно, процесс, идентифицированный Парентпроцессид, завершается, поэтому Парентпроцессид может не ссылаться на выполняющийся процесс.</span><span class="sxs-lookup"><span data-stu-id="641b9-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="641b9-135">Также возможно, что Парентпроцессид неправильно ссылается на процесс, который повторно использует идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="641b9-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="641b9-136">ProcessId</span><span class="sxs-lookup"><span data-stu-id="641b9-136">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="641b9-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="641b9-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="641b9-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="641b9-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="641b9-139">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="641b9-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="641b9-140">Глобальный идентификатор процесса, который можно использовать для идентификации процесса.</span><span class="sxs-lookup"><span data-stu-id="641b9-140">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="641b9-141">Значение допустимо с момента создания процесса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="641b9-141">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="641b9-142">SessionId</span><span class="sxs-lookup"><span data-stu-id="641b9-142">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="641b9-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="641b9-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="641b9-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="641b9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="641b9-145">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="641b9-145">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="641b9-146">Уникальный идентификатор, создаваемый операционной системой при создании нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="641b9-146">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="641b9-147">Сеанс охватывает период времени от входа до выхода из определенной системы.</span><span class="sxs-lookup"><span data-stu-id="641b9-147">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="641b9-148">уникуепроцесскэй</span><span class="sxs-lookup"><span data-stu-id="641b9-148">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="641b9-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="641b9-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="641b9-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="641b9-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="641b9-151">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="641b9-151">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="641b9-152">Адрес объекта процесса в ядре.</span><span class="sxs-lookup"><span data-stu-id="641b9-152">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="641b9-153">UserSID</span><span class="sxs-lookup"><span data-stu-id="641b9-153">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="641b9-154">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="641b9-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="641b9-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="641b9-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="641b9-156">Квалификаторы: Вмидатаид (6), Extension ("sid")</span><span class="sxs-lookup"><span data-stu-id="641b9-156">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="641b9-157">Идентификатор безопасности (SID) для пользовательского контекста, в котором происходит событие.</span><span class="sxs-lookup"><span data-stu-id="641b9-157">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="641b9-158">Примечания</span><span class="sxs-lookup"><span data-stu-id="641b9-158">Remarks</span></span>

<span data-ttu-id="641b9-159">Типы событий Дкстарт и Дценд перечисляют процесс, выполняемый в данный момент, включая бездействующий и системный процессы, на момент запуска и завершения сеанса ядра соответственно.</span><span class="sxs-lookup"><span data-stu-id="641b9-159">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="641b9-160">Требования</span><span class="sxs-lookup"><span data-stu-id="641b9-160">Requirements</span></span>



| <span data-ttu-id="641b9-161">Требование</span><span class="sxs-lookup"><span data-stu-id="641b9-161">Requirement</span></span> | <span data-ttu-id="641b9-162">Значение</span><span class="sxs-lookup"><span data-stu-id="641b9-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="641b9-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="641b9-163">Minimum supported client</span></span><br/> | <span data-ttu-id="641b9-164">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="641b9-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="641b9-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="641b9-165">Minimum supported server</span></span><br/> | <span data-ttu-id="641b9-166">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="641b9-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="641b9-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="641b9-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="641b9-168">**Процесс \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="641b9-168">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




