---
description: MFT_MESSAGE_COMMAND_FLUSH — запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092742"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="7e88b-103">\_ \_ Очистка команды сообщения \_ MFT</span><span class="sxs-lookup"><span data-stu-id="7e88b-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="7e88b-104">Запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.</span><span class="sxs-lookup"><span data-stu-id="7e88b-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="7e88b-105">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="7e88b-105">Message Parameter</span></span>

<span data-ttu-id="7e88b-106">Нет.</span><span class="sxs-lookup"><span data-stu-id="7e88b-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e88b-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="7e88b-107">Remarks</span></span>

<span data-ttu-id="7e88b-108">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="7e88b-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="7e88b-109">После отправки сообщения MFT может принимать новые входные образцы.</span><span class="sxs-lookup"><span data-stu-id="7e88b-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="7e88b-110">Текущие типы носителей не являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="7e88b-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="7e88b-111">Реализация</span><span class="sxs-lookup"><span data-stu-id="7e88b-111">Implementation</span></span>

<span data-ttu-id="7e88b-112">Все МФТС должны реализовывать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="7e88b-112">All MFTs must implement this message.</span></span> <span data-ttu-id="7e88b-113">При получении этого сообщения MFT должно удалить все примеры мультимедиа, которые он удерживает.</span><span class="sxs-lookup"><span data-stu-id="7e88b-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="7e88b-114">[Асинхронный МФТС](asynchronous-mfts.md): MFT не отправляет другое событие [метрансформнидинпут](metransformneedinput.md) , пока оно не получит [**\_ сообщение \_ MFT \_ о \_ начале \_ потока**](mft-message-notify-start-of-stream.md) сообщения от клиента.</span><span class="sxs-lookup"><span data-stu-id="7e88b-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e88b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7e88b-115">Requirements</span></span>



| <span data-ttu-id="7e88b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7e88b-116">Requirement</span></span> | <span data-ttu-id="7e88b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7e88b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e88b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e88b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7e88b-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e88b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7e88b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e88b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7e88b-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7e88b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7e88b-122">Header</span><span class="sxs-lookup"><span data-stu-id="7e88b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e88b-123"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e88b-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e88b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7e88b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e88b-125">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="7e88b-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




