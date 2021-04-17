---
description: Уведомляет Media Foundation преобразование (MFT) о завершении входного потока.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711696"
---
# <a name="mft_message_notify_end_of_stream"></a><span data-ttu-id="9f658-103">\_уведомление об \_ \_ окончании \_ \_ потока в сообщении MFT</span><span class="sxs-lookup"><span data-stu-id="9f658-103">MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM</span></span>

<span data-ttu-id="9f658-104">Уведомляет Media Foundation преобразование (MFT) о завершении входного потока.</span><span class="sxs-lookup"><span data-stu-id="9f658-104">Notifies a Media Foundation transform (MFT) that an input stream has ended.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="9f658-105">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="9f658-105">Message Parameter</span></span>

<span data-ttu-id="9f658-106">Параметр *улпарам* содержит идентификатор входного потока, указанного в виде значения **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="9f658-106">The *ulParam* parameter contains the identifier of the input stream, specified as a **DWORD** value.</span></span> <span data-ttu-id="9f658-107">В 64-разрядных приложениях поместите это значение в младшие 32-разряды типа **ulong \_**.</span><span class="sxs-lookup"><span data-stu-id="9f658-107">In 64-bit applications, place this value in the lower 32-bits of the **ULONG\_PTR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f658-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f658-108">Remarks</span></span>

<span data-ttu-id="9f658-109">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="9f658-109">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="9f658-110">Клиенту не требуется отсылать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="9f658-110">The client is not required to send this message.</span></span>

<span data-ttu-id="9f658-111">После завершения потока клиент может снова вызвать [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , чтобы отправить новые данные для этого потока.</span><span class="sxs-lookup"><span data-stu-id="9f658-111">After a stream ends, the client may call [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) again to send new data for that stream.</span></span> <span data-ttu-id="9f658-112">В этом случае клиент должен задать атрибут небесперебойности (атрибут [**мфсампликстенсионности \_ небесперебойности**](mfsampleextension-discontinuity-attribute.md) ) для первого входного примера после завершения потока.</span><span class="sxs-lookup"><span data-stu-id="9f658-112">If so, the client must set the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute) on the first input sample after the stream ends.</span></span> <span data-ttu-id="9f658-113">(Клиент всегда должен устанавливать этот атрибут в первом новом примере после завершения потока, независимо от того, отправил ли клиент сообщение MFT об **\_ \_ \_ окончании \_ \_ потока** сообщения.</span><span class="sxs-lookup"><span data-stu-id="9f658-113">(The client should always set this attribute on the first new sample after a stream ends, regardless of whether the client sent the **MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM** message.</span></span> <span data-ttu-id="9f658-114">Дополнительные сведения об обработке прекращений см. в разделе [Базовая модель обработки MFT](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="9f658-114">For more information about handling discontinuities, see [Basic MFT Processing Model](basic-mft-processing-model.md).)</span></span>

<span data-ttu-id="9f658-115">После отправки этого сообщения для каждого входного потока клиент обычно отправляет команду **\_ \_ \_ очистки сообщения MFT** , а затем выполняет сбор оставшихся выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9f658-115">After sending this message for every input stream, the client typically sends an **MFT\_MESSAGE\_COMMAND\_DRAIN** command and then collects the remaining output.</span></span> <span data-ttu-id="9f658-116">Однако клиент не обязан выполнять сток MFT.</span><span class="sxs-lookup"><span data-stu-id="9f658-116">However, the client is not required to drain the MFT.</span></span> <span data-ttu-id="9f658-117">Если клиент не выполняет сток MFT, то MFT, как правило, отменяет любые необработанные данные при следующем вызове метода [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), когда обнаруживает небесперебойность потока.</span><span class="sxs-lookup"><span data-stu-id="9f658-117">If the client does not drain the MFT, the MFT will typically discard any unprocessed data on the next call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), when it detects the stream discontinuity.</span></span> <span data-ttu-id="9f658-118">Кроме того, клиент может очистить MFT перед вызовом **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="9f658-118">Alternatively, the client might flush the MFT before calling **ProcessInput**.</span></span>

<span data-ttu-id="9f658-119">Это сообщение не удаляет входной поток или не сбрасывает тип носителя.</span><span class="sxs-lookup"><span data-stu-id="9f658-119">This message does not remove the input stream or reset the media type.</span></span>

### <a name="implementation"></a><span data-ttu-id="9f658-120">Реализация</span><span class="sxs-lookup"><span data-stu-id="9f658-120">Implementation</span></span>

<span data-ttu-id="9f658-121">MFT не требуется для ответа на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="9f658-121">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f658-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9f658-122">Requirements</span></span>



| <span data-ttu-id="9f658-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9f658-123">Requirement</span></span> | <span data-ttu-id="9f658-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9f658-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f658-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f658-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9f658-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f658-126">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9f658-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f658-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9f658-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f658-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9f658-129">Header</span><span class="sxs-lookup"><span data-stu-id="9f658-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f658-130"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f658-130"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f658-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f658-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f658-132">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="9f658-132">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




