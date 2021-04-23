---
description: 'Вызывается выходным центром доверия (OTA), когда метод Имфаутпуттрустаусорити:: Сетполици завершается асинхронно.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Событие Меполицисет (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711570"
---
# <a name="mepolicyset-event"></a><span data-ttu-id="bd26e-103">Событие Меполицисет</span><span class="sxs-lookup"><span data-stu-id="bd26e-103">MEPolicySet event</span></span>

<span data-ttu-id="bd26e-104">Вызывается выходным центром доверия (OTA), когда метод [**имфаутпуттрустаусорити:: сетполици**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) завершается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="bd26e-104">Raised by an output trust authority (OTA) when the [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="bd26e-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="bd26e-105">Event values</span></span>

<span data-ttu-id="bd26e-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="bd26e-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bd26e-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bd26e-107">VARTYPE</span></span>              | <span data-ttu-id="bd26e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bd26e-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="bd26e-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="bd26e-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="bd26e-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="bd26e-110">No event data.</span></span><br/> <br/> |
| <span data-ttu-id="bd26e-111">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="bd26e-111">VT\_UI4</span></span><br/> | <span data-ttu-id="bd26e-112">Идентификатор, который можно задать для [имфаутпутполици](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) с помощью атрибута [MF_POLICY_ID](mf-policy-id.md) .</span><span class="sxs-lookup"><span data-stu-id="bd26e-112">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) through the [MF_POLICY_ID](mf-policy-id.md) attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="bd26e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bd26e-113">Requirements</span></span>



| <span data-ttu-id="bd26e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bd26e-114">Requirement</span></span> | <span data-ttu-id="bd26e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bd26e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd26e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd26e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bd26e-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd26e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bd26e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd26e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bd26e-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd26e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd26e-120">Header</span><span class="sxs-lookup"><span data-stu-id="bd26e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd26e-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd26e-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd26e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd26e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd26e-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd26e-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




