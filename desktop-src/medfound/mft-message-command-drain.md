---
description: MFT_MESSAGE_COMMAND_DRAIN — запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092752"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="309da-103">\_ \_ сток команды сообщения \_ MFT</span><span class="sxs-lookup"><span data-stu-id="309da-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="309da-104">Запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.</span><span class="sxs-lookup"><span data-stu-id="309da-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="309da-105">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="309da-105">Message Parameter</span></span>

<span data-ttu-id="309da-106">Нет.</span><span class="sxs-lookup"><span data-stu-id="309da-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="309da-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="309da-107">Remarks</span></span>

<span data-ttu-id="309da-108">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="309da-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="309da-109">После отправки этого сообщения указанный входной поток не принимает входные данные, пока MFT обрабатывает все данные из предыдущих вызовов [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="309da-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="309da-110">Процесс очистки незначительно различает синхронные МФТС и асинхронные МФТС:</span><span class="sxs-lookup"><span data-stu-id="309da-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="309da-111">**Синхронный МФТС**</span><span class="sxs-lookup"><span data-stu-id="309da-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="309da-112">После того как клиент отправляет это сообщение, он вызывает [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) в цикле до тех пор, пока **ProcessOutput** не вернет код ошибки **MF E для \_ \_ преобразования \_ требуется \_ больше \_ входных данных**.</span><span class="sxs-lookup"><span data-stu-id="309da-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="309da-113">Пока MFT все еще содержит данные для обработки, дальнейшие вызовы метода [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="309da-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="309da-114">MFT будет создавать выходные данные до тех пор, пока не будут использованы все хранимые данные.</span><span class="sxs-lookup"><span data-stu-id="309da-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="309da-115">Таблица MFT отклоняет все данные, которые не могут быть обработаны, в полный образец выходных данных.</span><span class="sxs-lookup"><span data-stu-id="309da-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="309da-116">(Например, он должен удалить часть видеокадра.)</span><span class="sxs-lookup"><span data-stu-id="309da-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="309da-117">**Асинхронный МФТС**</span><span class="sxs-lookup"><span data-stu-id="309da-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="309da-118">Таблица MFT продолжит отсылать события [метрансформхавеаутпут](metransformhaveoutput.md) , пока не будет больше данных для обработки.</span><span class="sxs-lookup"><span data-stu-id="309da-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="309da-119">В течение этого времени события [метрансформнидинпут](metransformneedinput.md) не отправляются.</span><span class="sxs-lookup"><span data-stu-id="309da-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="309da-120">После того как MFT отправляет Последнее событие [метрансформхавеаутпут](metransformhaveoutput.md) , оно отправляет событие [метрансформдраинкомплете](metransformdraincomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="309da-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="309da-121">После завершения очистки Таблица MFT не отправляет другое событие [метрансформнидинпут](metransformneedinput.md) , пока не получит [**\_ сообщение MFT \_ о \_ начале \_ \_ потока**](mft-message-notify-start-of-stream.md) сообщения от клиента.</span><span class="sxs-lookup"><span data-stu-id="309da-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="309da-122">После очистки MFT клиент может отправить дополнительные входные данные.</span><span class="sxs-lookup"><span data-stu-id="309da-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="309da-123">Первый пример после операции стока должен иметь атрибут небесперебойности (атрибут [**мфсампликстенсионности \_**](mfsampleextension-discontinuity-attribute.md) небесперебойности).</span><span class="sxs-lookup"><span data-stu-id="309da-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="309da-124">В более ранних версиях этой документации указано, что параметр события *улпарам* является членом перечисления [**\_ \_ \_ типа стока MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) .</span><span class="sxs-lookup"><span data-stu-id="309da-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="309da-125">Неверно.</span><span class="sxs-lookup"><span data-stu-id="309da-125">That is not correct.</span></span> <span data-ttu-id="309da-126">*Улпарам* содержит идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="309da-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="309da-127">Реализация</span><span class="sxs-lookup"><span data-stu-id="309da-127">Implementation</span></span>

<span data-ttu-id="309da-128">Асинхронная Таблица MFT всегда должна возвращать [метрансформдраинкомплете](metransformdraincomplete.md) после ее очистки.</span><span class="sxs-lookup"><span data-stu-id="309da-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="309da-129">Синхронная MFT может игнорировать это сообщение и вернуть \_ значение ОК, если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="309da-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="309da-130">MFT никогда не хранит более одного входного образца одновременно.</span><span class="sxs-lookup"><span data-stu-id="309da-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="309da-131">Каждый входной образец создает один пример вывода.</span><span class="sxs-lookup"><span data-stu-id="309da-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="309da-132">В противном случае это сообщение должно быть реализовано в синхронной таблице MFT.</span><span class="sxs-lookup"><span data-stu-id="309da-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="309da-133">Требования</span><span class="sxs-lookup"><span data-stu-id="309da-133">Requirements</span></span>



| <span data-ttu-id="309da-134">Требование</span><span class="sxs-lookup"><span data-stu-id="309da-134">Requirement</span></span> | <span data-ttu-id="309da-135">Значение</span><span class="sxs-lookup"><span data-stu-id="309da-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="309da-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="309da-136">Minimum supported client</span></span><br/> | <span data-ttu-id="309da-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="309da-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="309da-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="309da-138">Minimum supported server</span></span><br/> | <span data-ttu-id="309da-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="309da-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="309da-140">Header</span><span class="sxs-lookup"><span data-stu-id="309da-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="309da-141"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="309da-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="309da-142">См. также</span><span class="sxs-lookup"><span data-stu-id="309da-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="309da-143">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="309da-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="309da-144">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="309da-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




