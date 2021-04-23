---
description: Во время потоковой передачи произошла устранимая ошибка.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Событие Менонфаталеррор (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344622"
---
# <a name="menonfatalerror-event"></a><span data-ttu-id="6bcd9-103">Событие Менонфаталеррор</span><span class="sxs-lookup"><span data-stu-id="6bcd9-103">MENonFatalError event</span></span>

<span data-ttu-id="6bcd9-104">Во время потоковой передачи произошла устранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-104">A non-fatal error occurred during streaming.</span></span> <span data-ttu-id="6bcd9-105">Любой компонент Media Foundation может отправить это событие в любое время.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-105">Any Media Foundation component can send this event at any time.</span></span>

## <a name="event-values"></a><span data-ttu-id="6bcd9-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="6bcd9-106">Event values</span></span>

<span data-ttu-id="6bcd9-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6bcd9-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6bcd9-108">VARTYPE</span></span>            | <span data-ttu-id="6bcd9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6bcd9-109">Description</span></span>                                                        |
|--------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6bcd9-110">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6bcd9-110">VT\_UI4</span></span><br/> | <span data-ttu-id="6bcd9-111">Значение **HRESULT** , описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-111">**HRESULT** value that describes the error.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="6bcd9-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6bcd9-112">Attributes</span></span>

<span data-ttu-id="6bcd9-113">Для этого события не определены атрибуты.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-113">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bcd9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bcd9-114">Remarks</span></span>

<span data-ttu-id="6bcd9-115">Это событие сигнализирует о непредвиденной, но устранимой ошибке во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-115">This event signals an unexpected but recoverable error during streaming.</span></span> <span data-ttu-id="6bcd9-116">Например, источник мультимедиа может отправить это событие при удалении пакета.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-116">For example, a media source might send this event if it drops a packet.</span></span>

<span data-ttu-id="6bcd9-117">Не отправляйте это событие, чтобы сообщить о сбое асинхронного метода.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="6bcd9-118">В случае сбоя асинхронного метода код ошибки возвращается в виде обычного события для этого метода.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="6bcd9-119">Если возникает неустранимая ошибка потоковой передачи, отправьте событие [Миррор](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="6bcd9-119">If a non-recoverable streaming error occurs, send the [MEError](meerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bcd9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6bcd9-120">Requirements</span></span>



| <span data-ttu-id="6bcd9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6bcd9-121">Requirement</span></span> | <span data-ttu-id="6bcd9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6bcd9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bcd9-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bcd9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6bcd9-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6bcd9-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="6bcd9-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bcd9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6bcd9-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6bcd9-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="6bcd9-127">Header</span><span class="sxs-lookup"><span data-stu-id="6bcd9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bcd9-128"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bcd9-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bcd9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bcd9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bcd9-130">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6bcd9-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




