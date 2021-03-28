---
description: Этот класс является классом типа событий для событий потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Класс Thread_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f6fa7ae1f50e005fe8f66e918a4a8360a0e8f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984772"
---
# <a name="thread_v0_typegroup1-class"></a><span data-ttu-id="022cb-104">\_Класс Thread v0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="022cb-104">Thread\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="022cb-105">Этот класс является классом типа событий для событий потока.</span><span class="sxs-lookup"><span data-stu-id="022cb-105">This class is the event type class for thread events.</span></span>

<span data-ttu-id="022cb-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="022cb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="022cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="022cb-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="022cb-108">Участники</span><span class="sxs-lookup"><span data-stu-id="022cb-108">Members</span></span>

<span data-ttu-id="022cb-109">Класс **Thread \_ v0 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="022cb-109">The **Thread\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="022cb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="022cb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="022cb-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="022cb-111">Properties</span></span>

<span data-ttu-id="022cb-112">Класс **Thread \_ v0 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="022cb-112">The **Thread\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="022cb-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="022cb-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="022cb-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="022cb-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="022cb-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="022cb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="022cb-116">Квалификаторы: Вмидатаид (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="022cb-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="022cb-117">Идентификатор процесса потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="022cb-117">Process identifier of the thread involved in the event.</span></span>

</dd> <dt>

<span data-ttu-id="022cb-118">тсреадид</span><span class="sxs-lookup"><span data-stu-id="022cb-118">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="022cb-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="022cb-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="022cb-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="022cb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="022cb-121">Квалификаторы: Вмидатаид (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="022cb-121">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="022cb-122">Идентификатор потока, участвующего в событии.</span><span class="sxs-lookup"><span data-stu-id="022cb-122">Thread identifier of the thread involved in the event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="022cb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="022cb-123">Requirements</span></span>



| <span data-ttu-id="022cb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="022cb-124">Requirement</span></span> | <span data-ttu-id="022cb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="022cb-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="022cb-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="022cb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="022cb-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="022cb-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="022cb-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="022cb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="022cb-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="022cb-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="022cb-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="022cb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022cb-131">**\_V0 потока**</span><span class="sxs-lookup"><span data-stu-id="022cb-131">**Thread\_V0**</span></span>](thread-v0.md)
</dt> </dl>

 

 




