---
description: Задает отметку времени для последнего шага кадра.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675755"
---
# <a name="ec_scrub_time"></a><span data-ttu-id="aab72-103">\_время очистки \_ EC</span><span class="sxs-lookup"><span data-stu-id="aab72-103">EC\_SCRUB\_TIME</span></span>

<span data-ttu-id="aab72-104">Задает отметку времени для последнего шага кадра.</span><span class="sxs-lookup"><span data-stu-id="aab72-104">Specifies the time stamp for the most recent frame step.</span></span>

## <a name="parameters"></a><span data-ttu-id="aab72-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="aab72-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab72-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="aab72-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="aab72-107">(**DWORD**) Нижний 32 бит метки времени.</span><span class="sxs-lookup"><span data-stu-id="aab72-107">(**DWORD**) Lower 32 bits of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="aab72-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="aab72-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="aab72-109">(**DWORD**) Верхний 32 бит метки времени.</span><span class="sxs-lookup"><span data-stu-id="aab72-109">(**DWORD**) Upper 32 bits of the time stamp.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="aab72-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="aab72-110">Default Action</span></span>

<span data-ttu-id="aab72-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="aab72-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="aab72-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="aab72-112">Remarks</span></span>

<span data-ttu-id="aab72-113">Выступающий для фильтра " [**Улучшенный обработчик видео**](enhanced-video-renderer-filter.md) " (Евр) отправляет это сообщение в Евр при завершении шага кадра.</span><span class="sxs-lookup"><span data-stu-id="aab72-113">The presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter sends this message to the EVR when it completes a frame step.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab72-114">Требования</span><span class="sxs-lookup"><span data-stu-id="aab72-114">Requirements</span></span>



| <span data-ttu-id="aab72-115">Требование</span><span class="sxs-lookup"><span data-stu-id="aab72-115">Requirement</span></span> | <span data-ttu-id="aab72-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aab72-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aab72-117">Header</span><span class="sxs-lookup"><span data-stu-id="aab72-117">Header</span></span><br/> | <dl> <span data-ttu-id="aab72-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="aab72-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab72-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aab72-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab72-120">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="aab72-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




