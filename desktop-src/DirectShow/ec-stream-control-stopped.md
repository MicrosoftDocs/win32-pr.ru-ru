---
description: Команда окончания управления потоком завершена.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685400"
---
# <a name="ec_stream_control_stopped"></a><span data-ttu-id="c6971-103">\_Управление ПОТОКОМ \_ EC \_ остановлено</span><span class="sxs-lookup"><span data-stu-id="c6971-103">EC\_STREAM\_CONTROL\_STOPPED</span></span>

<span data-ttu-id="c6971-104">Команда окончания управления потоком завершена.</span><span class="sxs-lookup"><span data-stu-id="c6971-104">A stream-control stop command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6971-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6971-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6971-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*псендер*</span><span class="sxs-lookup"><span data-stu-id="c6971-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="c6971-107">(**IUnknown** \* ) Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода, который остановил поток.</span><span class="sxs-lookup"><span data-stu-id="c6971-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that stopped the stream.</span></span>

</dd> <dt>

<span data-ttu-id="c6971-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*двкукие*</span><span class="sxs-lookup"><span data-stu-id="c6971-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="c6971-109">(**DWORD**) Определяемое пользователем значение.</span><span class="sxs-lookup"><span data-stu-id="c6971-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c6971-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c6971-110">Default Action</span></span>

<span data-ttu-id="c6971-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="c6971-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6971-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="c6971-112">Remarks</span></span>

<span data-ttu-id="c6971-113">Фильтры отправляют это событие в ответ на метод [**иамстреамконтрол:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="c6971-113">Filters send this event in response to the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="c6971-114">Метод **StopAt** задает время ссылки для завершения потоковой передачи ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c6971-114">The **StopAt** method specifies a reference time for a pin to stop streaming.</span></span> <span data-ttu-id="c6971-115">При остановке потоковой передачи фильтр отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="c6971-115">When streaming does halt, the filter sends this event.</span></span>

<span data-ttu-id="c6971-116">Параметр *псендер* указывает ПИН-код, который выполняет команду «Завершение».</span><span class="sxs-lookup"><span data-stu-id="c6971-116">The *pSender* parameter specifies the pin that executes the stop command.</span></span> <span data-ttu-id="c6971-117">В зависимости от реализации он может не быть ПИН-кодом, полученным при вызове [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="c6971-117">Depending on the implementation, it might not be the pin that received the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) call.</span></span>

<span data-ttu-id="c6971-118">Параметр *двкукие* задается приложением в методе [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="c6971-118">The *dwCookie* parameter is specified by the application in the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="c6971-119">Этот параметр позволяет приложению контролировать несколько вызовов метода.</span><span class="sxs-lookup"><span data-stu-id="c6971-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6971-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c6971-120">Requirements</span></span>



| <span data-ttu-id="c6971-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c6971-121">Requirement</span></span> | <span data-ttu-id="c6971-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c6971-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6971-123">Header</span><span class="sxs-lookup"><span data-stu-id="c6971-123">Header</span></span><br/> | <dl> <span data-ttu-id="c6971-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6971-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6971-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6971-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6971-126">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="c6971-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c6971-127">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c6971-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




