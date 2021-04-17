---
description: Граф фильтра завершает работу до уничтожения.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 471b746df3980afd96bbfc122a164ccd30561846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651827"
---
# <a name="ec_shutting_down"></a><span data-ttu-id="28221-103">EC \_ Завершение работы \_</span><span class="sxs-lookup"><span data-stu-id="28221-103">EC\_SHUTTING\_DOWN</span></span>

<span data-ttu-id="28221-104">Граф фильтра завершает работу до уничтожения.</span><span class="sxs-lookup"><span data-stu-id="28221-104">The filter graph is shutting down, prior to being destroyed.</span></span>

## <a name="parameters"></a><span data-ttu-id="28221-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="28221-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28221-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="28221-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="28221-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="28221-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="28221-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="28221-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="28221-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="28221-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="28221-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="28221-110">Default Action</span></span>

<span data-ttu-id="28221-111">Это событие не отправляется в приложение.</span><span class="sxs-lookup"><span data-stu-id="28221-111">This event is not sent to the application.</span></span> <span data-ttu-id="28221-112">Диспетчер графов фильтров отправляет его распространителям подключаемых модулей, чтобы уведомить их о завершении работы графа.</span><span class="sxs-lookup"><span data-stu-id="28221-112">The filter graph manager sends it to plug-in distributors, to notify them that the graph is shutting down.</span></span> <span data-ttu-id="28221-113">Приложения не могут переопределить действие по умолчанию для этого события.</span><span class="sxs-lookup"><span data-stu-id="28221-113">Applications cannot override the default action of this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="28221-114">Требования</span><span class="sxs-lookup"><span data-stu-id="28221-114">Requirements</span></span>



| <span data-ttu-id="28221-115">Требование</span><span class="sxs-lookup"><span data-stu-id="28221-115">Requirement</span></span> | <span data-ttu-id="28221-116">Значение</span><span class="sxs-lookup"><span data-stu-id="28221-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28221-117">Header</span><span class="sxs-lookup"><span data-stu-id="28221-117">Header</span></span><br/> | <dl> <span data-ttu-id="28221-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="28221-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28221-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28221-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28221-120">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="28221-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="28221-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="28221-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




