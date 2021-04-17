---
description: Помечает точку в потоке. Это сообщение относится только к асинхронному МФТС.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711697"
---
# <a name="mft_message_command_marker"></a><span data-ttu-id="aa694-104">\_ \_ маркер команды сообщения \_ MFT</span><span class="sxs-lookup"><span data-stu-id="aa694-104">MFT\_MESSAGE\_COMMAND\_MARKER</span></span>

<span data-ttu-id="aa694-105">Помечает точку в потоке.</span><span class="sxs-lookup"><span data-stu-id="aa694-105">Marks a point in the stream.</span></span> <span data-ttu-id="aa694-106">Это сообщение относится только к [асинхронному МФТС](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="aa694-106">This message applies only to [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="aa694-107">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="aa694-107">Message Parameter</span></span>

<span data-ttu-id="aa694-108">Произвольное значение.</span><span class="sxs-lookup"><span data-stu-id="aa694-108">An arbitrary value.</span></span> <span data-ttu-id="aa694-109">MFT возвращает значение клиенту в событии [метрансформмаркер](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="aa694-109">The MFT returns the value to the client in the [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa694-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa694-110">Remarks</span></span>

<span data-ttu-id="aa694-111">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="aa694-111">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="aa694-112">MFT реагирует на этот мессажеас:</span><span class="sxs-lookup"><span data-stu-id="aa694-112">The MFT responds to this messageas follows:</span></span>

1.  <span data-ttu-id="aa694-113">MFT создает столько выходных образцов, сколько можно из существующих входных данных, отправляя событие [метрансформхавеаутпут](metransformhaveoutput.md) для каждого выходного примера.</span><span class="sxs-lookup"><span data-stu-id="aa694-113">The MFT generates as many output samples as it can from the existing input data, sending an [METransformHaveOutput](metransformhaveoutput.md) event for each output sample.</span></span>
2.  <span data-ttu-id="aa694-114">После создания всех выходных данных MFT отправляет событие [метрансформмаркер](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="aa694-114">After all of the output is generated, the MFT sends an [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="aa694-115">Это событие должно быть отправлено после всех событий [метрансформхавеаутпут](metransformhaveoutput.md) .</span><span class="sxs-lookup"><span data-stu-id="aa694-115">This event must be sent after all of the [METransformHaveOutput](metransformhaveoutput.md) events.</span></span>

<span data-ttu-id="aa694-116">Клиент не обязан отправить это сообщение и должен отправить это сообщение только в асинхронный МФТС.</span><span class="sxs-lookup"><span data-stu-id="aa694-116">The client is not required to send this message, and should send this message only to asynchronous MFTs.</span></span> <span data-ttu-id="aa694-117">Синхронная Таблица MFT не будет отсылать событие [метрансформмаркер](metransformmarker.md) в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="aa694-117">A synchronous MFT will not send an [METransformMarker](metransformmarker.md) event in response to this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="aa694-118">Реализация</span><span class="sxs-lookup"><span data-stu-id="aa694-118">Implementation</span></span>

<span data-ttu-id="aa694-119">Асинхронный МФТС должен отвечать на это сообщение, как описано.</span><span class="sxs-lookup"><span data-stu-id="aa694-119">Asynchronous MFTs must respond to this message as described.</span></span> <span data-ttu-id="aa694-120">Синхронное МФТС должно игнорировать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="aa694-120">Synchronous MFTs should ignore this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa694-121">Требования</span><span class="sxs-lookup"><span data-stu-id="aa694-121">Requirements</span></span>



| <span data-ttu-id="aa694-122">Требование</span><span class="sxs-lookup"><span data-stu-id="aa694-122">Requirement</span></span> | <span data-ttu-id="aa694-123">Значение</span><span class="sxs-lookup"><span data-stu-id="aa694-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa694-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa694-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa694-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="aa694-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aa694-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa694-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa694-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa694-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa694-128">Header</span><span class="sxs-lookup"><span data-stu-id="aa694-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa694-129"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa694-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa694-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa694-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa694-131">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="aa694-131">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




