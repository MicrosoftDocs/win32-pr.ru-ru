---
description: EC_ERRORABORTEX — операция прервана из-за ошибки.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3bf1e1f24f9d5b07312f542c1ce4ea671f601d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094612"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="c9a05-103">EC \_ еррорабортекс</span><span class="sxs-lookup"><span data-stu-id="c9a05-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="c9a05-104">Операция прервана из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9a05-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9a05-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9a05-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a05-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c9a05-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c9a05-107">**(HRESULT)** Код ошибки операции, которая завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c9a05-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="c9a05-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c9a05-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c9a05-109">**(BSTR)** Строка, содержащая дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c9a05-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c9a05-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c9a05-110">Default Action</span></span>

<span data-ttu-id="c9a05-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="c9a05-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a05-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="c9a05-112">Remarks</span></span>

<span data-ttu-id="c9a05-113">Устаревший фильтр [источника Windows Media](windows-media-source-filter.md) отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="c9a05-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="c9a05-114">Новые фильтры не должны отсылать это событие.</span><span class="sxs-lookup"><span data-stu-id="c9a05-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a05-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c9a05-115">Requirements</span></span>



| <span data-ttu-id="c9a05-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c9a05-116">Requirement</span></span> | <span data-ttu-id="c9a05-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c9a05-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a05-118">Header</span><span class="sxs-lookup"><span data-stu-id="c9a05-118">Header</span></span><br/> | <dl> <span data-ttu-id="c9a05-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a05-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a05-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c9a05-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a05-121">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="c9a05-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c9a05-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c9a05-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




