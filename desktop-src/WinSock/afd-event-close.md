---
description: Событие трассировки сети Winsock для операции закрытия сокета.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE событие
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809766"
---
# <a name="afd_event_close-event"></a><span data-ttu-id="53f40-103">\_ \_ Событие закрытия события АФД</span><span class="sxs-lookup"><span data-stu-id="53f40-103">AFD\_EVENT\_CLOSE event</span></span>

<span data-ttu-id="53f40-104">Событие **\_ \_ закрытия события АФД** — это событие трассировки сети Winsock для операции закрытия сокета.</span><span class="sxs-lookup"><span data-stu-id="53f40-104">The **AFD\_EVENT\_CLOSE** event is a Winsock network tracing event for socket close operation.</span></span>


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a><span data-ttu-id="53f40-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="53f40-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f40-106">*ентерексит*</span><span class="sxs-lookup"><span data-stu-id="53f40-106">*EnterExit*</span></span> 
</dt> <dd>

<span data-ttu-id="53f40-107">Сведения об этом событии.</span><span class="sxs-lookup"><span data-stu-id="53f40-107">Information on this event.</span></span>

<span data-ttu-id="53f40-108">В следующей таблице перечислены возможные значения для параметра *ентерексит* :</span><span class="sxs-lookup"><span data-stu-id="53f40-108">The following table lists the possible values for the *EnterExit* parameter:</span></span>



| <span data-ttu-id="53f40-109">Значение</span><span class="sxs-lookup"><span data-stu-id="53f40-109">Value</span></span>                                                                        | <span data-ttu-id="53f40-110">Значение</span><span class="sxs-lookup"><span data-stu-id="53f40-110">Meaning</span></span>                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="53f40-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="53f40-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="53f40-112">Начало запроса Winsock.</span><span class="sxs-lookup"><span data-stu-id="53f40-112">The start of a Winsock request.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="53f40-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="53f40-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="53f40-114">Запрос Winsock завершен.</span><span class="sxs-lookup"><span data-stu-id="53f40-114">The Winsock request completed.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="53f40-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="53f40-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="53f40-116">Драйвер Winsock АФД выполнял внутреннее действие (например, прерывание подключения).</span><span class="sxs-lookup"><span data-stu-id="53f40-116">The Winsock AFD driver took an internal action (aborting a connection, for example).</span></span><br/>      |
| <dl> <span data-ttu-id="53f40-117"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="53f40-117"><dt>3</dt></span></span> </dl> | <span data-ttu-id="53f40-118">Драйвер TCP/IP привел к возникновению этого события.</span><span class="sxs-lookup"><span data-stu-id="53f40-118">The TCP/IP driver caused this event to occur.</span></span> <span data-ttu-id="53f40-119">Обычно это указывает на уведомление об изменении данных.</span><span class="sxs-lookup"><span data-stu-id="53f40-119">This usually indicates a data notification.</span></span><br/> |
| <dl> <span data-ttu-id="53f40-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="53f40-120"><dt>4</dt></span></span> </dl> | <span data-ttu-id="53f40-121">Драйвер Winsock АФД привел к возникновению этого события (например, при настройке параметра сокета).</span><span class="sxs-lookup"><span data-stu-id="53f40-121">The Winsock AFD driver caused this event to occur (setting a socket option, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53f40-122">*Расположение*</span><span class="sxs-lookup"><span data-stu-id="53f40-122">*Location*</span></span> 
</dt> <dd>

<span data-ttu-id="53f40-123">Закрытое поле, используемое внутри.</span><span class="sxs-lookup"><span data-stu-id="53f40-123">A private field used internally.</span></span>

</dd> <dt>

<span data-ttu-id="53f40-124">*Процесс*</span><span class="sxs-lookup"><span data-stu-id="53f40-124">*Process*</span></span> 
</dt> <dd>

<span data-ttu-id="53f40-125">[Епроцесс](/windows-hardware/drivers/kernel/eprocess) адрес процесса, которому принадлежит связанный сокет.</span><span class="sxs-lookup"><span data-stu-id="53f40-125">The [EPROCESS](/windows-hardware/drivers/kernel/eprocess) address of the process that owns the related socket.</span></span> <span data-ttu-id="53f40-126">Это непрозрачная структура, которая служит объектом процесса для процесса.</span><span class="sxs-lookup"><span data-stu-id="53f40-126">This is an opaque structure that serves as the process object for a process.</span></span> <span data-ttu-id="53f40-127">Дополнительные сведения см. в документации по пакету драйверов Windows для структуры [епроцесс](/windows-hardware/drivers/kernel/eprocess) .</span><span class="sxs-lookup"><span data-stu-id="53f40-127">For more information, see the Windows Driver Kit documentation for the [EPROCESS](/windows-hardware/drivers/kernel/eprocess) structure.</span></span>

</dd> <dt>

<span data-ttu-id="53f40-128">*Конечная точка*</span><span class="sxs-lookup"><span data-stu-id="53f40-128">*Endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="53f40-129">\_Адрес конечной точки АФД сокета.</span><span class="sxs-lookup"><span data-stu-id="53f40-129">The AFD\_ENDPOINT address of the socket.</span></span>

</dd> <dt>

<span data-ttu-id="53f40-130">*Состояние*</span><span class="sxs-lookup"><span data-stu-id="53f40-130">*Status*</span></span> 
</dt> <dd>

<span data-ttu-id="53f40-131">Код NTSTATUS для операции.</span><span class="sxs-lookup"><span data-stu-id="53f40-131">The NTSTATUS code for the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53f40-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53f40-132">Remarks</span></span>

<span data-ttu-id="53f40-133">Событие **\_ \_ закрытия события АФД** отслеживается для операции сети Winsock, чтобы закрыть сокет.</span><span class="sxs-lookup"><span data-stu-id="53f40-133">The **AFD\_EVENT\_CLOSE** event is traced for a Winsock network operation to close a socket.</span></span> <span data-ttu-id="53f40-134">Канал для этого события — Winsock-АФД.</span><span class="sxs-lookup"><span data-stu-id="53f40-134">The channel for this event is Winsock-AFD.</span></span> <span data-ttu-id="53f40-135">Уровень этого события является информационным.</span><span class="sxs-lookup"><span data-stu-id="53f40-135">The level for this event is informational.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f40-136">Требования</span><span class="sxs-lookup"><span data-stu-id="53f40-136">Requirements</span></span>



| <span data-ttu-id="53f40-137">Требование</span><span class="sxs-lookup"><span data-stu-id="53f40-137">Requirement</span></span> | <span data-ttu-id="53f40-138">Значение</span><span class="sxs-lookup"><span data-stu-id="53f40-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="53f40-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53f40-139">Minimum supported client</span></span><br/> | <span data-ttu-id="53f40-140">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="53f40-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="53f40-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53f40-141">Minimum supported server</span></span><br/> | <span data-ttu-id="53f40-142">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="53f40-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53f40-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53f40-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f40-144">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="53f40-144">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="53f40-145">**\_дескриптор события**</span><span class="sxs-lookup"><span data-stu-id="53f40-145">**EVENT\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[<span data-ttu-id="53f40-146">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="53f40-146">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="53f40-147">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="53f40-147">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="53f40-148">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="53f40-148">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

