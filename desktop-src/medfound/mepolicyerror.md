---
description: Вызывается надежным выходом при возникновении ошибки при принудительном применении политики вывода.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Событие Меполициеррор (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711571"
---
# <a name="mepolicyerror-event"></a><span data-ttu-id="4aa82-103">Событие Меполициеррор</span><span class="sxs-lookup"><span data-stu-id="4aa82-103">MEPolicyError event</span></span>

<span data-ttu-id="4aa82-104">Вызывается надежным выходом при возникновении ошибки при принудительном применении политики вывода.</span><span class="sxs-lookup"><span data-stu-id="4aa82-104">Raised by a trusted output if an error occurs while enforcing the output policy.</span></span>

<span data-ttu-id="4aa82-105">Если сеанс мультимедиа получает это событие, он останавливает воспроизведение и перенаправляет событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="4aa82-105">If the Media Session receives this event, it stops playback and forwards the event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="4aa82-106">Значения событий</span><span class="sxs-lookup"><span data-stu-id="4aa82-106">Event values</span></span>

<span data-ttu-id="4aa82-107">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="4aa82-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4aa82-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4aa82-108">VARTYPE</span></span>              | <span data-ttu-id="4aa82-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4aa82-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4aa82-110">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="4aa82-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4aa82-111">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="4aa82-111">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4aa82-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4aa82-112">Remarks</span></span>

<span data-ttu-id="4aa82-113">Возможные значения, получаемые из [**имфмедиаевент:: Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="4aa82-113">Possible values retrieved from [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) include the following.</span></span>



| <span data-ttu-id="4aa82-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4aa82-114">Value</span></span>                      | <span data-ttu-id="4aa82-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4aa82-115">Description</span></span>                                                    |
|----------------------------|----------------------------------------------------------------|
| <span data-ttu-id="4aa82-116">\_Политика MF \_ E \_ не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4aa82-116">MF\_E\_POLICY\_UNSUPPORTED</span></span> | <span data-ttu-id="4aa82-117">Доверенный выход не поддерживает текущую политику вывода.</span><span class="sxs-lookup"><span data-stu-id="4aa82-117">The trusted output does not support the current output policy.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4aa82-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4aa82-118">Requirements</span></span>



| <span data-ttu-id="4aa82-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4aa82-119">Requirement</span></span> | <span data-ttu-id="4aa82-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4aa82-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa82-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4aa82-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa82-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4aa82-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4aa82-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4aa82-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa82-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4aa82-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4aa82-125">Header</span><span class="sxs-lookup"><span data-stu-id="4aa82-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aa82-126"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4aa82-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa82-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4aa82-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa82-128">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4aa82-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




