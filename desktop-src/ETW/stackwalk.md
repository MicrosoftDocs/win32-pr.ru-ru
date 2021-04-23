---
description: Этот класс является родительским для событий трассировки стека.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Класс Стакквалк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984472"
---
# <a name="stackwalk-class"></a><span data-ttu-id="4a716-103">Класс Стакквалк</span><span class="sxs-lookup"><span data-stu-id="4a716-103">StackWalk class</span></span>

<span data-ttu-id="4a716-104">Этот класс является родительским для событий трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="4a716-104">This class is the parent class for stack tracing events.</span></span>

<span data-ttu-id="4a716-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4a716-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a716-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a716-106">Syntax</span></span>

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="4a716-107">Участники</span><span class="sxs-lookup"><span data-stu-id="4a716-107">Members</span></span>

<span data-ttu-id="4a716-108">Класс **стакквалк** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="4a716-108">The **StackWalk** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a716-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a716-109">Remarks</span></span>

<span data-ttu-id="4a716-110">Чтобы включить трассировку стека событий ядра, вызовите функцию [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) и укажите события и типы ядра, для которых необходимо записать трассировку стека.</span><span class="sxs-lookup"><span data-stu-id="4a716-110">To enable stack tracing of kernel events, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function and specify the kernel events and types for which you want to capture the stack trace.</span></span> <span data-ttu-id="4a716-111">Чтобы включить трассировку стека для других событий, установите для элемента **енаблепроперти** в [**\_ \_ параметре включить**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) трассировку **\_ \_ \_ стека \_ свойства значение включено**.</span><span class="sxs-lookup"><span data-stu-id="4a716-111">To enable stack tracing for other events, set the **EnableProperty** member of [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) to **EVENT\_ENABLE\_PROPERTY\_STACK\_TRACE**.</span></span>

<span data-ttu-id="4a716-112">Используйте следующий тип события для обнаружения фактического события при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="4a716-112">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="4a716-113">Тип события</span><span class="sxs-lookup"><span data-stu-id="4a716-113">Event type</span></span>           | <span data-ttu-id="4a716-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4a716-114">Description</span></span>                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a716-115">Значение типа события, 32</span><span class="sxs-lookup"><span data-stu-id="4a716-115">Event type value, 32</span></span> | <span data-ttu-id="4a716-116">Событие трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="4a716-116">Stack tracing event.</span></span> <span data-ttu-id="4a716-117">Класс [**MOF \_ события стакквалк**](stackwalk-event.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="4a716-117">The [**StackWalk\_Event**](stackwalk-event.md) MOF class defines the event data for this event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4a716-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4a716-118">Requirements</span></span>



| <span data-ttu-id="4a716-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4a716-119">Requirement</span></span> | <span data-ttu-id="4a716-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4a716-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4a716-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a716-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4a716-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4a716-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4a716-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a716-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4a716-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a716-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 
