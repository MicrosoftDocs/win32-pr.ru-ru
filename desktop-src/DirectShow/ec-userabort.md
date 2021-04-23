---
description: Пользователь завершил воспроизведение.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675548"
---
# <a name="ec_userabort"></a><span data-ttu-id="d0a11-103">EC \_ усераборт</span><span class="sxs-lookup"><span data-stu-id="d0a11-103">EC\_USERABORT</span></span>

<span data-ttu-id="d0a11-104">Пользователь завершил воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="d0a11-104">The user has terminated playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0a11-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0a11-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a11-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d0a11-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d0a11-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="d0a11-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="d0a11-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d0a11-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d0a11-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="d0a11-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="d0a11-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d0a11-110">Default Action</span></span>

<span data-ttu-id="d0a11-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="d0a11-111">None.</span></span> <span data-ttu-id="d0a11-112">Приложение должно решить, следует ли прерывать граф.</span><span class="sxs-lookup"><span data-stu-id="d0a11-112">The application must decide whether to stop the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a11-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0a11-113">Remarks</span></span>

<span data-ttu-id="d0a11-114">Этот код события сигнализирует, что пользователь прервал воспроизведение нормального графа.</span><span class="sxs-lookup"><span data-stu-id="d0a11-114">This event code signals that the user has terminated normal graph playback.</span></span> <span data-ttu-id="d0a11-115">Например, модули подготовки видео отправляют это событие, если пользователь закрывает окно видео.</span><span class="sxs-lookup"><span data-stu-id="d0a11-115">For example, video renderers send this event if the user closes the video window.</span></span>

<span data-ttu-id="d0a11-116">После отправки этого события фильтр должен отклонить все выборки и не отправлять [**события \_ перерисовки EC**](ec-repaint.md) , пока фильтр не остановится и не будет сброшен.</span><span class="sxs-lookup"><span data-stu-id="d0a11-116">After sending this event, the filter should reject all samples and not send any [**EC\_REPAINT**](ec-repaint.md) events, until the filter stops and is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a11-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d0a11-117">Requirements</span></span>



| <span data-ttu-id="d0a11-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d0a11-118">Requirement</span></span> | <span data-ttu-id="d0a11-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d0a11-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a11-120">Header</span><span class="sxs-lookup"><span data-stu-id="d0a11-120">Header</span></span><br/> | <dl> <span data-ttu-id="d0a11-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a11-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a11-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0a11-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a11-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="d0a11-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d0a11-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="d0a11-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




