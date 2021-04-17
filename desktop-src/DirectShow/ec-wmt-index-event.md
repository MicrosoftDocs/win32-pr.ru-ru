---
description: Отправляется, когда приложение использует фильтр модуля записи WM ASF для индексирования видеофайлов Windows Media.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675443"
---
# <a name="ec_wmt_index_event-dshowh"></a><span data-ttu-id="1a14a-103">EC_WMT_INDEX_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="1a14a-103">EC_WMT_INDEX_EVENT (Dshow.h)</span></span>

<span data-ttu-id="1a14a-104">Отправляется, когда приложение использует фильтр [модуля записи WM ASF](wm-asf-writer-filter.md) для индексирования видеофайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1a14a-104">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) filter to index Windows Media Video files.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a14a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a14a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a14a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1a14a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1a14a-107">Может быть одним из следующих сообщений **\_ о состоянии ВМТ** .</span><span class="sxs-lookup"><span data-stu-id="1a14a-107">Can be one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="1a14a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1a14a-108">Value</span></span>                | <span data-ttu-id="1a14a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1a14a-109">Description</span></span>              |
|----------------------|--------------------------|
| <span data-ttu-id="1a14a-110">ВМТ \_ запущен</span><span class="sxs-lookup"><span data-stu-id="1a14a-110">WMT\_STARTED</span></span>         | <span data-ttu-id="1a14a-111">Индексирование начато.</span><span class="sxs-lookup"><span data-stu-id="1a14a-111">Indexing has begun.</span></span>      |
| <span data-ttu-id="1a14a-112">ВМТ \_ закрыт</span><span class="sxs-lookup"><span data-stu-id="1a14a-112">WMT\_CLOSED</span></span>          | <span data-ttu-id="1a14a-113">Индексирование завершено.</span><span class="sxs-lookup"><span data-stu-id="1a14a-113">Indexing has completed.</span></span>  |
| <span data-ttu-id="1a14a-114">\_ \_ ход выполнения индекса ВМТ</span><span class="sxs-lookup"><span data-stu-id="1a14a-114">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="1a14a-115">Выполняется индексирование.</span><span class="sxs-lookup"><span data-stu-id="1a14a-115">Indexing is in progress.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1a14a-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1a14a-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1a14a-117">Если *LPARAM1* ВМТ \_ Closed или ВМТ \_ Started, то *lParam2* равен нулю.</span><span class="sxs-lookup"><span data-stu-id="1a14a-117">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="1a14a-118">Если *lParam1* является ВМТ \_ \_ ходом выполнения индекса, то *lParam2* — это **DWORD** , который указывает текущий ход выполнения в процентах от общего размера загрузки.</span><span class="sxs-lookup"><span data-stu-id="1a14a-118">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that specifies the current progress as a percentage of the total download size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a14a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1a14a-119">Requirements</span></span>



| <span data-ttu-id="1a14a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1a14a-120">Requirement</span></span> | <span data-ttu-id="1a14a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1a14a-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a14a-122">Header</span><span class="sxs-lookup"><span data-stu-id="1a14a-122">Header</span></span><br/> | <dl> <span data-ttu-id="1a14a-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a14a-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a14a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a14a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a14a-125">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="1a14a-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1a14a-126">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="1a14a-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




