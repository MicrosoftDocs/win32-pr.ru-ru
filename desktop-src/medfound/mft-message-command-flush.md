---
description: Запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811614"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="8eba9-103">\_ \_ Очистка команды сообщения \_ MFT</span><span class="sxs-lookup"><span data-stu-id="8eba9-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="8eba9-104">Запрашивает преобразование Media Foundation (MFT) для сброса всех хранящихся данных.</span><span class="sxs-lookup"><span data-stu-id="8eba9-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="8eba9-105">Параметр сообщения</span><span class="sxs-lookup"><span data-stu-id="8eba9-105">Message Parameter</span></span>

<span data-ttu-id="8eba9-106">Нет.</span><span class="sxs-lookup"><span data-stu-id="8eba9-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eba9-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="8eba9-107">Remarks</span></span>

<span data-ttu-id="8eba9-108">Чтобы отправить это сообщение, вызовите [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="8eba9-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="8eba9-109">После отправки сообщения MFT может принимать новые входные образцы.</span><span class="sxs-lookup"><span data-stu-id="8eba9-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="8eba9-110">Текущие типы носителей не являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="8eba9-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="8eba9-111">Реализация</span><span class="sxs-lookup"><span data-stu-id="8eba9-111">Implementation</span></span>

<span data-ttu-id="8eba9-112">Все МФТС должны реализовывать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="8eba9-112">All MFTs must implement this message.</span></span> <span data-ttu-id="8eba9-113">При получении этого сообщения MFT должно удалить все примеры мультимедиа, которые он удерживает.</span><span class="sxs-lookup"><span data-stu-id="8eba9-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="8eba9-114">[Асинхронный МФТС](asynchronous-mfts.md): MFT не отправляет другое событие [метрансформнидинпут](metransformneedinput.md) , пока оно не получит [**\_ сообщение \_ MFT \_ о \_ начале \_ потока**](mft-message-notify-start-of-stream.md) сообщения от клиента.</span><span class="sxs-lookup"><span data-stu-id="8eba9-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eba9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8eba9-115">Requirements</span></span>



| <span data-ttu-id="8eba9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8eba9-116">Requirement</span></span> | <span data-ttu-id="8eba9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8eba9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eba9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8eba9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8eba9-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8eba9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8eba9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8eba9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8eba9-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8eba9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8eba9-122">Header</span><span class="sxs-lookup"><span data-stu-id="8eba9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eba9-123"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eba9-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eba9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8eba9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eba9-125">**\_тип сообщения \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="8eba9-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




