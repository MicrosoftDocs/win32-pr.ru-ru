---
description: Этот класс является классом типа события для событий конца потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Класс Thread_V1_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3e56590127b2317813d7431a1cc646fbe76e35a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543079"
---
# <a name="thread_v1_typegroup2-class"></a><span data-ttu-id="72e8e-104">\_ \_ Класс TypeGroup2 потока v1</span><span class="sxs-lookup"><span data-stu-id="72e8e-104">Thread\_V1\_TypeGroup2 class</span></span>

<span data-ttu-id="72e8e-105">Этот класс является классом типа события для событий конца потока.</span><span class="sxs-lookup"><span data-stu-id="72e8e-105">This class is the event type class for thread end events.</span></span>

<span data-ttu-id="72e8e-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="72e8e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e8e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72e8e-107">Syntax</span></span>

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a><span data-ttu-id="72e8e-108">Участники</span><span class="sxs-lookup"><span data-stu-id="72e8e-108">Members</span></span>

<span data-ttu-id="72e8e-109">Класс **Thread \_ v1 \_ TypeGroup2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="72e8e-109">The **Thread\_V1\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="72e8e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="72e8e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72e8e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="72e8e-111">Properties</span></span>

<span data-ttu-id="72e8e-112">Класс **Thread \_ v1 \_ TypeGroup2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="72e8e-112">The **Thread\_V1\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72e8e-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="72e8e-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e8e-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72e8e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72e8e-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72e8e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e8e-116">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="72e8e-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="72e8e-117">Идентификатор процесса потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="72e8e-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="72e8e-118">**Windows Server 2003:** Содержит квалификатор формата ("x").</span><span class="sxs-lookup"><span data-stu-id="72e8e-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="72e8e-119">тсреадид</span><span class="sxs-lookup"><span data-stu-id="72e8e-119">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e8e-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72e8e-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72e8e-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="72e8e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e8e-122">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="72e8e-122">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="72e8e-123">Идентификатор потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="72e8e-123">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="72e8e-124">**Windows Server 2003:** Содержит квалификатор формата ("x").</span><span class="sxs-lookup"><span data-stu-id="72e8e-124">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72e8e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="72e8e-125">Requirements</span></span>



| <span data-ttu-id="72e8e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="72e8e-126">Requirement</span></span> | <span data-ttu-id="72e8e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="72e8e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72e8e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72e8e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="72e8e-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="72e8e-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="72e8e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72e8e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="72e8e-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72e8e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72e8e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72e8e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e8e-133">**Поток \_ v1**</span><span class="sxs-lookup"><span data-stu-id="72e8e-133">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




