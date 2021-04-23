---
description: Фильтр запрашивает перезапуск графа.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674824"
---
# <a name="ec_need_restart"></a><span data-ttu-id="228cd-103">EC \_ требуется \_ Перезагрузка</span><span class="sxs-lookup"><span data-stu-id="228cd-103">EC\_NEED\_RESTART</span></span>

<span data-ttu-id="228cd-104">Фильтр запрашивает перезапуск графа.</span><span class="sxs-lookup"><span data-stu-id="228cd-104">A filter is requesting that the graph be restarted.</span></span>

## <a name="parameters"></a><span data-ttu-id="228cd-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="228cd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="228cd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="228cd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="228cd-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="228cd-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="228cd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="228cd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="228cd-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="228cd-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="228cd-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="228cd-110">Default Action</span></span>

<span data-ttu-id="228cd-111">Диспетчер графов фильтров приостанавливает и перезапускает граф.</span><span class="sxs-lookup"><span data-stu-id="228cd-111">The filter graph manager pauses and restarts the graph.</span></span> <span data-ttu-id="228cd-112">Он не передает событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="228cd-112">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="228cd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="228cd-113">Remarks</span></span>

<span data-ttu-id="228cd-114">Если фильтр отклоняет выборку в середине потока, восходящий ПИН-код перестанет предоставлять образцы.</span><span class="sxs-lookup"><span data-stu-id="228cd-114">If a filter rejects a sample in the middle of a stream, the upstream pin will stop delivering samples.</span></span> <span data-ttu-id="228cd-115">Фильтр может перезапустить поток, отправив это событие.</span><span class="sxs-lookup"><span data-stu-id="228cd-115">The filter can restart the stream by sending this event.</span></span> <span data-ttu-id="228cd-116">Например, модуль подготовки звука может потерять доступ к звуковому устройству, так как в окне видео теряется фокус.</span><span class="sxs-lookup"><span data-stu-id="228cd-116">For example, the audio renderer might lose access to the sound device, because a video window has lost focus.</span></span> <span data-ttu-id="228cd-117">На этом этапе модуль подготовки звука начинает отклонять образцы.</span><span class="sxs-lookup"><span data-stu-id="228cd-117">At that point, the audio renderer starts rejecting samples.</span></span> <span data-ttu-id="228cd-118">Когда он восстанавливает доступ к звуковому устройству, он отправляет это событие для перезапуска аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="228cd-118">When it regains access to the sound device, it sends this event to restart the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="228cd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="228cd-119">Requirements</span></span>



| <span data-ttu-id="228cd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="228cd-120">Requirement</span></span> | <span data-ttu-id="228cd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="228cd-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="228cd-122">Header</span><span class="sxs-lookup"><span data-stu-id="228cd-122">Header</span></span><br/> | <dl> <span data-ttu-id="228cd-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="228cd-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="228cd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="228cd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="228cd-125">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="228cd-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="228cd-126">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="228cd-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




