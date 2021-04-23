---
description: Этот класс является классом типа события для событий процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Класс Process_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984512"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="c857b-104">\_Класс Process v0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="c857b-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="c857b-105">Этот класс является классом типа события для событий процесса.</span><span class="sxs-lookup"><span data-stu-id="c857b-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="c857b-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="c857b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c857b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c857b-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="c857b-108">Участники</span><span class="sxs-lookup"><span data-stu-id="c857b-108">Members</span></span>

<span data-ttu-id="c857b-109">Класс **Process \_ v0 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c857b-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="c857b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c857b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c857b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c857b-111">Properties</span></span>

<span data-ttu-id="c857b-112">Класс **Process \_ v0 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c857b-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c857b-113">имажефиленаме</span><span class="sxs-lookup"><span data-stu-id="c857b-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c857b-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c857b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c857b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c857b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c857b-116">Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="c857b-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="c857b-117">Путь к исполняемому файлу процесса.</span><span class="sxs-lookup"><span data-stu-id="c857b-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="c857b-118">ParentId</span><span class="sxs-lookup"><span data-stu-id="c857b-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c857b-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c857b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c857b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c857b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c857b-121">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="c857b-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c857b-122">Уникальный идентификатор процесса, который создает процесс.</span><span class="sxs-lookup"><span data-stu-id="c857b-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="c857b-123">Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса.</span><span class="sxs-lookup"><span data-stu-id="c857b-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="c857b-124">Возможно, процесс, идентифицированный Парентпроцессид, завершается, поэтому Парентпроцессид может не ссылаться на выполняющийся процесс.</span><span class="sxs-lookup"><span data-stu-id="c857b-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="c857b-125">Также возможно, что Парентпроцессид неправильно ссылается на процесс, который повторно использует идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="c857b-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c857b-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="c857b-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c857b-127">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c857b-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c857b-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c857b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c857b-129">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="c857b-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c857b-130">Глобальный идентификатор процесса, который можно использовать для идентификации процесса.</span><span class="sxs-lookup"><span data-stu-id="c857b-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="c857b-131">Значение допустимо с момента создания процесса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="c857b-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="c857b-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="c857b-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c857b-133">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="c857b-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c857b-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c857b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c857b-135">Квалификаторы: Вмидатаид (3), Extension ("sid")</span><span class="sxs-lookup"><span data-stu-id="c857b-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="c857b-136">Идентификатор безопасности (SID) для пользовательского контекста, в котором происходит событие.</span><span class="sxs-lookup"><span data-stu-id="c857b-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c857b-137">Требования</span><span class="sxs-lookup"><span data-stu-id="c857b-137">Requirements</span></span>



| <span data-ttu-id="c857b-138">Требование</span><span class="sxs-lookup"><span data-stu-id="c857b-138">Requirement</span></span> | <span data-ttu-id="c857b-139">Значение</span><span class="sxs-lookup"><span data-stu-id="c857b-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c857b-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c857b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c857b-141">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c857b-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c857b-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c857b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c857b-143">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c857b-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c857b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c857b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c857b-145">**Обработка \_ v0**</span><span class="sxs-lookup"><span data-stu-id="c857b-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




