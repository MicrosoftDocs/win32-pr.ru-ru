---
description: Фильтр не получает достаточно данных.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651628"
---
# <a name="ec_starvation"></a><span data-ttu-id="6c26e-103">нехватка ресурсов EC \_</span><span class="sxs-lookup"><span data-stu-id="6c26e-103">EC\_STARVATION</span></span>

<span data-ttu-id="6c26e-104">Фильтр не получает достаточно данных.</span><span class="sxs-lookup"><span data-stu-id="6c26e-104">A filter is not receiving enough data.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c26e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c26e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c26e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6c26e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6c26e-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="6c26e-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="6c26e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6c26e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6c26e-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="6c26e-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="6c26e-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6c26e-110">Default Action</span></span>

<span data-ttu-id="6c26e-111">Событие не отправляется в приложение.</span><span class="sxs-lookup"><span data-stu-id="6c26e-111">The event is not sent to the application.</span></span> <span data-ttu-id="6c26e-112">Если граф фильтра выполняется, диспетчер графа фильтров приостанавливает граф и ждет завершения паузы.</span><span class="sxs-lookup"><span data-stu-id="6c26e-112">If the filter graph is running, the filter graph manager pauses the graph and waits for the pause to complete.</span></span> <span data-ttu-id="6c26e-113">Затем он снова запускает граф.</span><span class="sxs-lookup"><span data-stu-id="6c26e-113">Then it runs the graph again.</span></span> <span data-ttu-id="6c26e-114">Фильтр, отправляющий событие, не должен завершать его работу до тех пор, пока не пойдет достаточно данных для возобновления.</span><span class="sxs-lookup"><span data-stu-id="6c26e-114">The filter sending the event should not complete its transition to paused until it has enough data to resume.</span></span> <span data-ttu-id="6c26e-115">Если граф фильтра не работает, диспетчер графа фильтров игнорирует это событие.</span><span class="sxs-lookup"><span data-stu-id="6c26e-115">If the filter graph is not running, the filter graph manager ignores this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c26e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c26e-116">Remarks</span></span>

<span data-ttu-id="6c26e-117">Средство синтаксического анализа или фильтр источников может отправить это событие, если поступают слишком мало данных.</span><span class="sxs-lookup"><span data-stu-id="6c26e-117">A parser or source filter can send this event if too little data is arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c26e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6c26e-118">Requirements</span></span>



| <span data-ttu-id="6c26e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6c26e-119">Requirement</span></span> | <span data-ttu-id="6c26e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6c26e-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c26e-121">Header</span><span class="sxs-lookup"><span data-stu-id="6c26e-121">Header</span></span><br/> | <dl> <span data-ttu-id="6c26e-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c26e-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c26e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c26e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c26e-124">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="6c26e-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6c26e-125">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="6c26e-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




