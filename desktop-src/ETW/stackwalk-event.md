---
description: Этот класс является классом типа события для событий трассировки стека.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: Класс StackWalk_Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985701"
---
# <a name="stackwalk_event-class"></a><span data-ttu-id="6d2ad-103">\_Класс событий стакквалк</span><span class="sxs-lookup"><span data-stu-id="6d2ad-103">StackWalk\_Event class</span></span>

<span data-ttu-id="6d2ad-104">Этот класс является классом типа события для событий трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-104">This class is the event type class for stack tracing events.</span></span>

<span data-ttu-id="6d2ad-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2ad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d2ad-106">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a><span data-ttu-id="6d2ad-107">Участники</span><span class="sxs-lookup"><span data-stu-id="6d2ad-107">Members</span></span>

<span data-ttu-id="6d2ad-108">Класс **\_ событий стакквалк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6d2ad-108">The **StackWalk\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="6d2ad-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d2ad-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d2ad-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d2ad-110">Properties</span></span>

<span data-ttu-id="6d2ad-111">Класс **\_ событий стакквалк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-111">The **StackWalk\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d2ad-112">**EventTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-112">**EventTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2ad-113">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2ad-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-115">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="6d2ad-115">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="6d2ad-116">Метка времени исходного события из заголовка события.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-116">Original event time stamp from the event header.</span></span> <span data-ttu-id="6d2ad-117">Используйте эту отметку времени, чтобы сопоставить стек с событием.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-117">Use this time stamp to match the stack to an event.</span></span>

</dd> <dt>

<span data-ttu-id="6d2ad-118">**Stack1**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-118">**Stack1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2ad-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2ad-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-121">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="6d2ad-121">Qualifiers: WmiDataId(4), pointer</span></span>
</dt> </dl>

<span data-ttu-id="6d2ad-122">Адрес вызова.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-122">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="6d2ad-123">**Stack192**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-123">**Stack192**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2ad-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2ad-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-126">Квалификаторы: Вмидатаид (195), Pointer</span><span class="sxs-lookup"><span data-stu-id="6d2ad-126">Qualifiers: WmiDataId(195), pointer</span></span>
</dt> </dl>

<span data-ttu-id="6d2ad-127">Адрес вызова.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-127">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="6d2ad-128">**стаккпроцесс**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-128">**StackProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2ad-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2ad-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-131">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="6d2ad-131">Qualifiers: WmiDataId(2), format("x")</span></span>
</dt> </dl>

<span data-ttu-id="6d2ad-132">Идентификатор процесса исходного события.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-132">The process identifier of the original event.</span></span>

</dd> <dt>

<span data-ttu-id="6d2ad-133">**стакксреад**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-133">**StackThread**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2ad-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d2ad-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2ad-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d2ad-136">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="6d2ad-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6d2ad-137">Идентификатор потока исходного события.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-137">The thread identifier of the original event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d2ad-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d2ad-138">Remarks</span></span>

<span data-ttu-id="6d2ad-139">Обратите внимание, что в классе не отображаются все свойства \*\*Stack \* n\*\*\*, существующие между **Stack1** и **Stack192**.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-139">Note that the class does not show all of the **Stack\*n**\* properties that exist between **Stack1** and **Stack192**.</span></span> <span data-ttu-id="6d2ad-140">Используйте размер события, чтобы определить, сколько свойств **Stack \* n**\* содержит допустимые адреса.</span><span class="sxs-lookup"><span data-stu-id="6d2ad-140">Use the size of the event to determine how many **Stack\*n**\* properties contain valid addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2ad-141">Требования</span><span class="sxs-lookup"><span data-stu-id="6d2ad-141">Requirements</span></span>



| <span data-ttu-id="6d2ad-142">Требование</span><span class="sxs-lookup"><span data-stu-id="6d2ad-142">Requirement</span></span> | <span data-ttu-id="6d2ad-143">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2ad-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6d2ad-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d2ad-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2ad-145">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6d2ad-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6d2ad-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d2ad-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2ad-147">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d2ad-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




