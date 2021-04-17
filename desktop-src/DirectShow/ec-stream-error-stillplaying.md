---
description: Произошла ошибка в потоке, но поток по-прежнему воспроизводится.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675351"
---
# <a name="ec_stream_error_stillplaying"></a><span data-ttu-id="093de-103">EC \_ Stream \_ Error \_ стиллплайинг</span><span class="sxs-lookup"><span data-stu-id="093de-103">EC\_STREAM\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="093de-104">Произошла ошибка в потоке, но поток по-прежнему воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="093de-104">An error occurred in a stream, but the stream is still playing.</span></span>

## <a name="parameters"></a><span data-ttu-id="093de-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="093de-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="093de-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="093de-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="093de-107">(**HRESULT**) Код ошибки операции, которая завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="093de-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="093de-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="093de-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="093de-109">(**DWORD**) Код незначительной ошибки.</span><span class="sxs-lookup"><span data-stu-id="093de-109">(**DWORD**) Minor error code.</span></span> <span data-ttu-id="093de-110">Обычно это значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="093de-110">This value is usually zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="093de-111">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="093de-111">Default Action</span></span>

<span data-ttu-id="093de-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="093de-112">None.</span></span> <span data-ttu-id="093de-113">Приложение должно решить, следует ли прерывать граф.</span><span class="sxs-lookup"><span data-stu-id="093de-113">The application must decide whether to stop the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="093de-114">Требования</span><span class="sxs-lookup"><span data-stu-id="093de-114">Requirements</span></span>



| <span data-ttu-id="093de-115">Требование</span><span class="sxs-lookup"><span data-stu-id="093de-115">Requirement</span></span> | <span data-ttu-id="093de-116">Значение</span><span class="sxs-lookup"><span data-stu-id="093de-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="093de-117">Header</span><span class="sxs-lookup"><span data-stu-id="093de-117">Header</span></span><br/> | <dl> <span data-ttu-id="093de-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="093de-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="093de-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="093de-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="093de-120">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="093de-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="093de-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="093de-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




