---
description: Применена команда запуска управления потоком.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651726"
---
# <a name="ec_stream_control_started"></a><span data-ttu-id="013c7-103">\_Управление ПОТОКОМ \_ EC \_ запущено</span><span class="sxs-lookup"><span data-stu-id="013c7-103">EC\_STREAM\_CONTROL\_STARTED</span></span>

<span data-ttu-id="013c7-104">Применена команда запуска управления потоком.</span><span class="sxs-lookup"><span data-stu-id="013c7-104">A stream-control start command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="013c7-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="013c7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="013c7-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*псендер*</span><span class="sxs-lookup"><span data-stu-id="013c7-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="013c7-107">(**IUnknown** \* ) Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода, который запустил поток.</span><span class="sxs-lookup"><span data-stu-id="013c7-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that started the stream.</span></span>

</dd> <dt>

<span data-ttu-id="013c7-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*двкукие*</span><span class="sxs-lookup"><span data-stu-id="013c7-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="013c7-109">(**DWORD**) Определяемое пользователем значение.</span><span class="sxs-lookup"><span data-stu-id="013c7-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="013c7-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="013c7-110">Default Action</span></span>

<span data-ttu-id="013c7-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="013c7-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="013c7-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="013c7-112">Remarks</span></span>

<span data-ttu-id="013c7-113">Фильтры отправляют это событие в ответ на метод [**иамстреамконтрол:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="013c7-113">Filters send this event in response to the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="013c7-114">Этот метод задает время ссылки для начала потоковой передачи ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="013c7-114">This method specifies a reference time for a pin to begin streaming.</span></span> <span data-ttu-id="013c7-115">При начале потоковой передачи фильтр отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="013c7-115">When streaming does begin, the filter sends this event.</span></span>

<span data-ttu-id="013c7-116">Параметр *псендер* указывает ПИН-код, который выполняет команду Start.</span><span class="sxs-lookup"><span data-stu-id="013c7-116">The *pSender* parameter specifies the pin that executes the start command.</span></span> <span data-ttu-id="013c7-117">В зависимости от реализации это может быть не ПИН-код, получивший вызов [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="013c7-117">Depending on the implementation, it might not be the pin that received the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) call.</span></span>

<span data-ttu-id="013c7-118">Параметр *двкукие* задается приложением в методе [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="013c7-118">The *dwCookie* parameter is specified by the application in the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="013c7-119">Этот параметр позволяет приложению контролировать несколько вызовов метода.</span><span class="sxs-lookup"><span data-stu-id="013c7-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="013c7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="013c7-120">Requirements</span></span>



| <span data-ttu-id="013c7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="013c7-121">Requirement</span></span> | <span data-ttu-id="013c7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="013c7-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="013c7-123">Header</span><span class="sxs-lookup"><span data-stu-id="013c7-123">Header</span></span><br/> | <dl> <span data-ttu-id="013c7-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="013c7-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="013c7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="013c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="013c7-126">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="013c7-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="013c7-127">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="013c7-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




