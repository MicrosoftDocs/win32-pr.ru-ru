---
description: Запрашивает новый входной пример из расширенного фильтра модуля подготовки видео (Евр).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da73d02604e128fdf94edb8f84d1526cfcdb586e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674815"
---
# <a name="ec_sample_needed"></a><span data-ttu-id="cb692-103">\_требуется образец \_ EC</span><span class="sxs-lookup"><span data-stu-id="cb692-103">EC\_SAMPLE\_NEEDED</span></span>

<span data-ttu-id="cb692-104">Запрашивает новый входной пример из [**расширенного фильтра модуля подготовки видео**](enhanced-video-renderer-filter.md) (Евр).</span><span class="sxs-lookup"><span data-stu-id="cb692-104">Requests a new input sample from the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb692-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb692-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb692-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cb692-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cb692-107">Идентификатор входного потока, которому требуются новые входные данные.</span><span class="sxs-lookup"><span data-stu-id="cb692-107">Identifier of the input stream that needs new input.</span></span>

</dd> <dt>

<span data-ttu-id="cb692-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cb692-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cb692-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="cb692-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="cb692-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cb692-110">Default Action</span></span>

<span data-ttu-id="cb692-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb692-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb692-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="cb692-112">Remarks</span></span>

<span data-ttu-id="cb692-113">Микшер для фильтра Евр отправляет это сообщение, когда ему нужен новый входной пример.</span><span class="sxs-lookup"><span data-stu-id="cb692-113">The mixer for the EVR filter sends this message when it needs a new input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb692-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cb692-114">Requirements</span></span>



| <span data-ttu-id="cb692-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cb692-115">Requirement</span></span> | <span data-ttu-id="cb692-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cb692-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb692-117">Header</span><span class="sxs-lookup"><span data-stu-id="cb692-117">Header</span></span><br/> | <dl> <span data-ttu-id="cb692-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb692-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb692-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb692-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb692-120">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="cb692-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




