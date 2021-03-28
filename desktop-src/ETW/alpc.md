---
description: Этот класс является родительским классом для дополнительных событий вызова локальной процедуры. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: ALPC, класс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984524"
---
# <a name="alpc-class"></a><span data-ttu-id="9af13-104">ALPC, класс</span><span class="sxs-lookup"><span data-stu-id="9af13-104">ALPC class</span></span>

<span data-ttu-id="9af13-105">Этот класс является родительским классом для дополнительных событий вызова локальной процедуры.</span><span class="sxs-lookup"><span data-stu-id="9af13-105">This class is the parent class for advanced local procedure call events.</span></span>

<span data-ttu-id="9af13-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="9af13-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af13-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9af13-107">Syntax</span></span>

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="9af13-108">Участники</span><span class="sxs-lookup"><span data-stu-id="9af13-108">Members</span></span>

<span data-ttu-id="9af13-109">Класс **ALPC** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="9af13-109">The **ALPC** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="9af13-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="9af13-110">Remarks</span></span>

<span data-ttu-id="9af13-111">Чтобы включить дополнительные события локального вызова процедур в сеансе ведения журнала ядра NT, укажите **флаг \_ трассировки \_ событий \_ ALPC** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="9af13-111">To enable advanced local procedure call events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_ALPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="9af13-112">Потребители трассировки событий могут реализовать специальную обработку событий ALPC, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**алпкгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="9af13-112">Event trace consumers can implement special processing for ALPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ALPCGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="9af13-113">Используйте следующие типы событий для обнаружения фактического события ALPC при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="9af13-113">Use the following event types to identify the actual ALPC event when consuming events.</span></span>



| <span data-ttu-id="9af13-114">Тип события</span><span class="sxs-lookup"><span data-stu-id="9af13-114">Event type</span></span>           | <span data-ttu-id="9af13-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9af13-115">Description</span></span>                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af13-116">Значение типа события, 33</span><span class="sxs-lookup"><span data-stu-id="9af13-116">Event type value, 33</span></span> | <span data-ttu-id="9af13-117">Событие отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9af13-117">Send message event.</span></span> <span data-ttu-id="9af13-118">Класс MOF для [**\_ \_ сообщения Send**](alpc-send-message.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9af13-118">The [**ALPC\_Send\_Message**](alpc-send-message.md) MOF class defines the event data for this event.</span></span>                           |
| <span data-ttu-id="9af13-119">Значение типа события, 34</span><span class="sxs-lookup"><span data-stu-id="9af13-119">Event type value, 34</span></span> | <span data-ttu-id="9af13-120">Событие получения сообщения.</span><span class="sxs-lookup"><span data-stu-id="9af13-120">Receive message event.</span></span> <span data-ttu-id="9af13-121">Класс [**MOF \_ получения \_ сообщения ALPC**](alpc-receive-message.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9af13-121">The [**ALPC\_Receive\_Message**](alpc-receive-message.md) MOF class defines the event data for this event.</span></span>                  |
| <span data-ttu-id="9af13-122">Значение типа события, 35</span><span class="sxs-lookup"><span data-stu-id="9af13-122">Event type value, 35</span></span> | <span data-ttu-id="9af13-123">Ожидание события ответа.</span><span class="sxs-lookup"><span data-stu-id="9af13-123">Wait for reply event.</span></span> <span data-ttu-id="9af13-124">Класс [**, \_ ожидающий \_ \_ ответа**](alpc-wait-for-reply.md) класса MOF, определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9af13-124">The [**ALPC\_Wait\_For\_Reply**](alpc-wait-for-reply.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="9af13-125">Значение типа события, 36</span><span class="sxs-lookup"><span data-stu-id="9af13-125">Event type value, 36</span></span> | <span data-ttu-id="9af13-126">Ожидание события нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="9af13-126">Wait for new message event.</span></span> <span data-ttu-id="9af13-127">В [**ALPC. \_ Ожидание \_ нового класса \_ \_ сообщения**](alpc-wait-for-new-message.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9af13-127">The [**ALPC\_Wait\_For\_New\_Message**](alpc-wait-for-new-message.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="9af13-128">Значение типа события, 37</span><span class="sxs-lookup"><span data-stu-id="9af13-128">Event type value, 37</span></span> | <span data-ttu-id="9af13-129">Прерывать событие ожидания.</span><span class="sxs-lookup"><span data-stu-id="9af13-129">Stop waiting event.</span></span> <span data-ttu-id="9af13-130">Класс [**MOF \_ unwait**](alpc-unwait.md) , который определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="9af13-130">The [**ALPC\_Unwait**](alpc-unwait.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="9af13-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9af13-131">Requirements</span></span>



| <span data-ttu-id="9af13-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9af13-132">Requirement</span></span> | <span data-ttu-id="9af13-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9af13-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9af13-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9af13-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9af13-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9af13-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9af13-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9af13-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9af13-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9af13-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

