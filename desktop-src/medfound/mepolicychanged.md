---
description: Вызывается компонентом конвейера при изменении выходной политики потока. Это событие применяется только к защищенному содержимому.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Событие Меполицичанжед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711573"
---
# <a name="mepolicychanged-event"></a><span data-ttu-id="c75e1-104">Событие Меполицичанжед</span><span class="sxs-lookup"><span data-stu-id="c75e1-104">MEPolicyChanged event</span></span>

<span data-ttu-id="c75e1-105">Вызывается компонентом конвейера при изменении выходной политики потока.</span><span class="sxs-lookup"><span data-stu-id="c75e1-105">Raised by a pipeline component when the output policy for the stream changes.</span></span> <span data-ttu-id="c75e1-106">Это событие применяется только к защищенному содержимому.</span><span class="sxs-lookup"><span data-stu-id="c75e1-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="c75e1-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="c75e1-107">Event values</span></span>

<span data-ttu-id="c75e1-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="c75e1-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c75e1-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c75e1-109">VARTYPE</span></span>                | <span data-ttu-id="c75e1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c75e1-110">Description</span></span>                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c75e1-111">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="c75e1-111">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="c75e1-112">Указатель на интерфейс [**имфаутпутполици**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) новой политики для потока.</span><span class="sxs-lookup"><span data-stu-id="c75e1-112">Pointer to the [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) interface of the new policy for the stream.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c75e1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c75e1-113">Remarks</span></span>

<span data-ttu-id="c75e1-114">Это событие должно быть обработано всеми доверенными выходами.</span><span class="sxs-lookup"><span data-stu-id="c75e1-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="c75e1-115">Media Foundation преобразования (МФТС) получают это событие с помощью метода [**имфтрансформ::P роцессевент**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="c75e1-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="c75e1-116">Приемники мультимедиа получают это событие с помощью метода [**имфстреамсинк::P лацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="c75e1-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="c75e1-117">Доверенный выход должен применить новую политику или вернуть \_ \_ неподдерживаемую политику с кодом ошибки MF E \_ .</span><span class="sxs-lookup"><span data-stu-id="c75e1-117">The trusted output must apply the new policy or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75e1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c75e1-118">Requirements</span></span>



| <span data-ttu-id="c75e1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c75e1-119">Requirement</span></span> | <span data-ttu-id="c75e1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c75e1-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c75e1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c75e1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c75e1-122">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="c75e1-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="c75e1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c75e1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c75e1-124">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c75e1-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="c75e1-125">Header</span><span class="sxs-lookup"><span data-stu-id="c75e1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c75e1-126"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c75e1-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75e1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c75e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75e1-128">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c75e1-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




