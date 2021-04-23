---
description: Посылается асинхронным Media Foundation преобразованием (MFT), когда новые выходные данные доступны из MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Событие Метрансформхавеаутпут (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673343"
---
# <a name="metransformhaveoutput-event"></a><span data-ttu-id="847ac-103">Событие Метрансформхавеаутпут</span><span class="sxs-lookup"><span data-stu-id="847ac-103">METransformHaveOutput event</span></span>

<span data-ttu-id="847ac-104">Посылается асинхронным Media Foundation преобразованием (MFT), когда новые выходные данные доступны из MFT.</span><span class="sxs-lookup"><span data-stu-id="847ac-104">Sent by an asynchronous Media Foundation transform (MFT) when new output data is available from the MFT.</span></span>

## <a name="event-values"></a><span data-ttu-id="847ac-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="847ac-105">Event values</span></span>

<span data-ttu-id="847ac-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="847ac-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="847ac-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="847ac-107">VARTYPE</span></span>              | <span data-ttu-id="847ac-108">Описание</span><span class="sxs-lookup"><span data-stu-id="847ac-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="847ac-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="847ac-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="847ac-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="847ac-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="847ac-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="847ac-111">Attributes</span></span>

<span data-ttu-id="847ac-112">Для этого события не определены атрибуты.</span><span class="sxs-lookup"><span data-stu-id="847ac-112">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="847ac-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="847ac-113">Remarks</span></span>

<span data-ttu-id="847ac-114">Асинхронный МФТС отправляет это событие через интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="847ac-114">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="847ac-115">Синхронное МФТС никогда не отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="847ac-115">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="847ac-116">Когда клиент MFT получает это событие, он должен вызвать [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , чтобы получить выходные данные.</span><span class="sxs-lookup"><span data-stu-id="847ac-116">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get the output.</span></span>

## <a name="requirements"></a><span data-ttu-id="847ac-117">Требования</span><span class="sxs-lookup"><span data-stu-id="847ac-117">Requirements</span></span>



| <span data-ttu-id="847ac-118">Требование</span><span class="sxs-lookup"><span data-stu-id="847ac-118">Requirement</span></span> | <span data-ttu-id="847ac-119">Значение</span><span class="sxs-lookup"><span data-stu-id="847ac-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="847ac-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="847ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="847ac-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="847ac-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="847ac-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="847ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="847ac-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="847ac-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="847ac-124">Header</span><span class="sxs-lookup"><span data-stu-id="847ac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="847ac-125"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="847ac-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="847ac-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="847ac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="847ac-127">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="847ac-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="847ac-128">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="847ac-128">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




