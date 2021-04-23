---
description: Этот класс является родительским классом для разбиения событий ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Класс Сплитио
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985081"
---
# <a name="splitio-class"></a><span data-ttu-id="019f1-104">Класс Сплитио</span><span class="sxs-lookup"><span data-stu-id="019f1-104">SplitIo class</span></span>

<span data-ttu-id="019f1-105">Этот класс является родительским классом для разбиения событий ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="019f1-105">This class is the parent class for split IO events.</span></span>

<span data-ttu-id="019f1-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="019f1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="019f1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="019f1-107">Syntax</span></span>

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="019f1-108">Участники</span><span class="sxs-lookup"><span data-stu-id="019f1-108">Members</span></span>

<span data-ttu-id="019f1-109">Класс **сплитио** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="019f1-109">The **SplitIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="019f1-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="019f1-110">Remarks</span></span>

<span data-ttu-id="019f1-111">Чтобы включить разбиение событий ввода-вывода в сеансе ведения журнала ядра NT, укажите флаг **\_ трассировки \_ \_ \_ операций разбивки на событие** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="019f1-111">To enable split IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_SPLIT\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="019f1-112">Потребители трассировки событий могут реализовать специальную обработку для разбиения событий ввода-вывода, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**сплитиогуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="019f1-112">Event trace consumers can implement special processing for split IO events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**SplitIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="019f1-113">Используйте следующий тип события для обнаружения фактического события при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="019f1-113">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="019f1-114">Тип события</span><span class="sxs-lookup"><span data-stu-id="019f1-114">Event type</span></span>           | <span data-ttu-id="019f1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="019f1-115">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019f1-116">Значение типа события, 32</span><span class="sxs-lookup"><span data-stu-id="019f1-116">Event type value, 32</span></span> | <span data-ttu-id="019f1-117">Событие разбиения на операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="019f1-117">Split IO event.</span></span> <span data-ttu-id="019f1-118">Класс [**MOF \_ info сплитио**](splitio-info.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="019f1-118">The [**SplitIo\_Info**](splitio-info.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="019f1-119">События разбиения на операции ввода-вывода указывают на то, что запросы на ввод и вывод были разделены на несколько запросов дискового ввода в связи с базовым оборудованием зеркального отображения.</span><span class="sxs-lookup"><span data-stu-id="019f1-119">Split IO events indicate that the IO requests have been split into multiple disk IO requests due to the underlying mirroring disk hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="019f1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="019f1-120">Requirements</span></span>



| <span data-ttu-id="019f1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="019f1-121">Requirement</span></span> | <span data-ttu-id="019f1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="019f1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="019f1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="019f1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="019f1-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="019f1-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="019f1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="019f1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="019f1-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="019f1-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
