---
description: Вызывается компонентом конвейера при изменении конфигурации одной из схем выходной защиты. Это событие применяется только к защищенному содержимому.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Событие Меконтентпротектионмессаже (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811038"
---
# <a name="mecontentprotectionmessage-event"></a><span data-ttu-id="5b57f-104">Событие Меконтентпротектионмессаже</span><span class="sxs-lookup"><span data-stu-id="5b57f-104">MEContentProtectionMessage event</span></span>

<span data-ttu-id="5b57f-105">Вызывается компонентом конвейера при изменении конфигурации одной из схем выходной защиты.</span><span class="sxs-lookup"><span data-stu-id="5b57f-105">Raised by a pipeline component when the configuration changes for one of the output protection schemes.</span></span> <span data-ttu-id="5b57f-106">Это событие применяется только к защищенному содержимому.</span><span class="sxs-lookup"><span data-stu-id="5b57f-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="5b57f-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="5b57f-107">Event values</span></span>

<span data-ttu-id="5b57f-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="5b57f-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5b57f-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5b57f-109">VARTYPE</span></span>              | <span data-ttu-id="5b57f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5b57f-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5b57f-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="5b57f-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5b57f-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="5b57f-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5b57f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b57f-113">Remarks</span></span>

<span data-ttu-id="5b57f-114">Это событие должно быть обработано всеми доверенными выходами.</span><span class="sxs-lookup"><span data-stu-id="5b57f-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="5b57f-115">Media Foundation преобразования (МФТС) получают это событие с помощью метода [**имфтрансформ::P роцессевент**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="5b57f-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="5b57f-116">Приемники мультимедиа получают это событие с помощью метода [**имфстреамсинк::P лацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="5b57f-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="5b57f-117">Доверенный выход должен применить изменения политики или вернуть \_ \_ неподдерживаемую политику с кодом ошибки MF E \_ .</span><span class="sxs-lookup"><span data-stu-id="5b57f-117">The trusted output must apply the policy changes or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

<span data-ttu-id="5b57f-118">Данные и атрибуты события зависят от используемой системы защиты содержимого.</span><span class="sxs-lookup"><span data-stu-id="5b57f-118">The event data and attributes depend on the content protection system in use.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b57f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5b57f-119">Requirements</span></span>



| <span data-ttu-id="5b57f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5b57f-120">Requirement</span></span> | <span data-ttu-id="5b57f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5b57f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b57f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b57f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b57f-123">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="5b57f-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="5b57f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b57f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b57f-125">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="5b57f-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="5b57f-126">Header</span><span class="sxs-lookup"><span data-stu-id="5b57f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b57f-127"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b57f-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b57f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b57f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b57f-129">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b57f-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




