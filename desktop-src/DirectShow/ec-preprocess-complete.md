---
description: Отправляется фильтром модуля записи WM ASF при завершении предварительной обработки многопроходной кодировки.
ms.assetid: 2029afc4-419c-494a-ae52-1f84b08bcb35
title: EC_PREPROCESS_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba13938ac848ef37f1a2a2826372d97ff5a5d716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674820"
---
# <a name="ec_preprocess_complete"></a><span data-ttu-id="c335a-103">\_Предварительная обработка EC \_ завершена</span><span class="sxs-lookup"><span data-stu-id="c335a-103">EC\_PREPROCESS\_COMPLETE</span></span>

<span data-ttu-id="c335a-104">Отправляется фильтром [модуля записи WM ASF](wm-asf-writer-filter.md) при завершении предварительной обработки многопроходной кодировки.</span><span class="sxs-lookup"><span data-stu-id="c335a-104">Sent by the [WM ASF Writer](wm-asf-writer-filter.md) filter when it completes the pre-processing for multipass encoding.</span></span>

## <a name="parameters"></a><span data-ttu-id="c335a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c335a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c335a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c335a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c335a-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="c335a-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="c335a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c335a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c335a-109">(**IUnknown** \* ) Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра.</span><span class="sxs-lookup"><span data-stu-id="c335a-109">(**IUnknown**\*) Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c335a-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c335a-110">Default Action</span></span>

<span data-ttu-id="c335a-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="c335a-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c335a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c335a-112">Requirements</span></span>



| <span data-ttu-id="c335a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c335a-113">Requirement</span></span> | <span data-ttu-id="c335a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c335a-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c335a-115">Header</span><span class="sxs-lookup"><span data-stu-id="c335a-115">Header</span></span><br/> | <dl> <span data-ttu-id="c335a-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c335a-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c335a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c335a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c335a-118">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="c335a-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c335a-119">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c335a-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




